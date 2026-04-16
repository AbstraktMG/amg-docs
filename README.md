# AMG Suite Docs

Documentation for the [AMG Suite](https://github.com/AbstraktMG/amg-suite) of WordPress plugins.

## Browse

Public site: **[abstraktmg.github.io/amg-docs](https://abstraktmg.github.io/amg-docs)**

## Contributing

All docs are Markdown files. Edit directly on GitHub or clone and submit a PR.

### Structure

```
plugins/
  <plugin-slug>/
    overview.md       # What it does, when to use it
    setup.md          # Install and configure
    usage.md          # Step-by-step walkthroughs
    faq.md            # Quick answers
    troubleshooting.md
    changelog.md

developer/
  architecture.md
  remote-config.md
  creating-a-plugin.md
  hooks-filters.md
  contributing.md
```

### Front-matter

Each file starts with Jekyll front-matter for navigation:

```yaml
---
title: Setup
parent: Post Migration
grand_parent: Plugins
nav_order: 2
---
```

### Local preview

```bash
bundle install
bundle exec jekyll serve
# → http://localhost:4000/amg-docs/
```

## License

Internal documentation for Abstrakt Marketing Group.
