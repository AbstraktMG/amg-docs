---
title: Setup
parent: GDocs Importer
grand_parent: Plugins
nav_order: 2
---

# Setup

## Requirements

- WordPress 5.0+
- **AMG Suite** plugin active
- **Google Cloud project** with Drive and Docs APIs enabled
- **Service account** with JSON key
- A **Google Drive folder** shared with the service account

## Google Cloud setup

### 1. Create a service account

1. Go to [Google Cloud Console](https://console.cloud.google.com/)
2. Create or select a project
3. Enable **Google Drive API** and **Google Docs API**
4. Go to **Service Accounts** → Create Service Account
5. Name it (e.g., "amg-importer") → Create
6. Go to **Keys** tab → Add Key → Create new key → **JSON**
7. Save the downloaded JSON file securely

### 2. Share a Drive folder

1. Create a Google Drive folder for your content
2. Share it with the service account email (the `client_email` from the JSON)
3. Give it **Editor** access
4. Copy the **Folder ID** from the URL: `drive.google.com/drive/folders/{THIS_PART}`

## Plugin configuration

### Option A: AMG Suite Remote Config (recommended for multi-site)

If AMG Suite has remote config set up (`AMG_GITHUB_TOKEN` + `amg-config` repo), the Google service account JSON is automatically pulled from the central config. No per-site setup needed.

### Option B: Plugin settings UI

1. Go to **AMG → GDocs Importer → Settings**
2. Paste the full service account JSON into the textarea
3. Enter the Google Drive Folder ID
4. Click **Save Settings**
5. Click **Test Connection** — should show the folder name

### Option C: wp-config.php constant

```php
define('AIM_GOOGLE_SERVICE_ACCOUNT', file_get_contents('/path/to/service-account.json'));
```

### Credential priority

The plugin checks in order:
1. `AIM_GOOGLE_SERVICE_ACCOUNT` constant (wp-config.php)
2. AMG Suite Remote Config (`google_service_account` key)
3. Encrypted database setting (pasted in Settings UI)

## Folder ID

Enter the Folder ID in the Settings tab. This is the ID from the Google Drive folder URL — the part after `/folders/`.

Only documents in this folder (and its subfolders) are accessible.
