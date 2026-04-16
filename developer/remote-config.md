---
title: Remote Config
parent: Developer
nav_order: 2
---

# Remote Config API

`AMG_Remote_Config` (in AMG Suite) fetches shared credentials and configuration from a private GitHub repo (`AbstraktMG/amg-config`) using the site's `AMG_GITHUB_TOKEN`. Values are encrypted with `wp_salt('auth')` and cached in `wp_options`, refreshed daily via cron.

## Getting a value

```php
if (class_exists('AMG_Remote_Config')) {
    $api_key = AMG_Remote_Config::get('semrush_api_key');
    if ($api_key) {
        // use it
    }
}
```

## Available keys

Configured in `AbstraktMG/amg-config/config.json`:

| Key | Type | Description |
|-----|------|-------------|
| `google_service_account` | array | Service account JSON (for GDocs Importer) |
| `semrush_api_key` | string | SEMrush API key |
| `gtmetrix_api_key` | string | GTmetrix API key |
| `teams_webhook_url` | string | MS Teams incoming webhook URL |
| `plugin_versions` | map | Slug → latest version number for dashboard version badges |

Add new keys by editing `config.json` and committing.

## Credential priority in child plugins

Follow this order when authenticating:

```php
// 1. wp-config.php constant (dev/testing escape hatch)
if (defined('MY_PLUGIN_API_KEY')) {
    $key = MY_PLUGIN_API_KEY;
}
// 2. AMG Suite remote config (production)
elseif (class_exists('AMG_Remote_Config')) {
    $key = AMG_Remote_Config::get('my_service_key');
}
// 3. DB-stored plugin setting (fallback)
else {
    $key = get_option('my_plugin_api_key');
}
```

This pattern lets devs override for testing while defaulting to the central config on production sites.

## Checking freshness

```php
$status = AMG_Remote_Config::get_status();
// [
//   'version'    => 2,
//   'updated'    => '2026-04-14 14:00:00',
//   'is_stale'   => false,   // true if > 48h since last fetch
//   'has_token'  => true,
//   'has_config' => true,
// ]
```

## Manual refresh

`AMG_Remote_Config::fetch()` hits the GitHub API, downloads `config.json`, encrypts, and caches. Called:

- Daily via `amg_suite_config_refresh` cron hook
- On first plugin activation
- When an admin clicks **Refresh Now** on the AMG Suite dashboard

## Encryption

Uses the same AES-256-CBC + `wp_salt('auth')` pattern as GDocs Importer credential storage. Stored as `amg_suite_remote_config` in `wp_options` (encrypted).

## Graceful fallback

If `AMG_GITHUB_TOKEN` isn't defined or the fetch fails:

- `AMG_Remote_Config::get($key)` returns `null`
- Child plugins fall back to their local settings UI (step 3 above)
- No crash, no admin notice spam

## Security notes

- Credentials never appear in the admin UI (just a "Configured via remote config" status badge)
- `config.json` lives in a private repo
- Token scoped to read-only Contents on that repo only
- `wp-config.php` constants take priority — use this as the escape hatch for dev environments
