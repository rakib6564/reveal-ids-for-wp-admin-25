# Reveal IDs for WP Admin 2.5+

[![PHP Lint](https://github.com/rakib6564/reveal-ids-for-wp-admin-25/actions/workflows/lint.yml/badge.svg)](https://github.com/rakib6564/reveal-ids-for-wp-admin-25/actions/workflows/lint.yml)
[![WordPress Coding Standards](https://github.com/rakib6564/reveal-ids-for-wp-admin-25/actions/workflows/phpcs.yml/badge.svg)](https://github.com/rakib6564/reveal-ids-for-wp-admin-25/actions/workflows/phpcs.yml)
[![Release](https://github.com/rakib6564/reveal-ids-for-wp-admin-25/actions/workflows/release.yml/badge.svg)](https://github.com/rakib6564/reveal-ids-for-wp-admin-25/actions/workflows/release.yml)

**Restores the entry-ID columns that WordPress removed from admin list tables in version 2.5.**

| | |
|---|---|
| **Version** | 1.6.3 |
| **Author** | Oliver Schlöbe |
| **Author URI** | https://www.schloebe.de/ |
| **Plugin URI** | https://www.schloebe.de/wordpress/reveal-ids-for-wp-admin-25-plugin/ |
| **License** | GPL-2.0-or-later |
| **Requires at least** | WordPress 3.0 |
| **Tested up to** | WordPress 7.1 |
| **Requires PHP** | 7.4+ |

This is the official, unmodified public WordPress.org plugin. It is included in this repository as the exact copy deployed on this site, for version control and change tracking.

## What it does

Prior to WordPress 2.5, every admin list screen showed each item's database ID. 2.5 removed those columns for a cleaner UI — this plugin adds them back, for developers and power users who need the ID at a glance (for template tags, shortcodes, or debugging) without opening each item individually.

Adds a sortable **ID** column to:

- Posts and pages (and any custom post type, discovered dynamically via `get_post_types()`)
- Media Library
- Users (including the network users list on Multisite)
- Comments
- Link Manager & Link Categories
- All taxonomies (discovered dynamically via `get_taxonomies()`)
- Multisite's network Sites list

Implemented purely through WordPress's standard `manage_*_columns` / `manage_*_custom_column` filter and action pairs — no AJAX, no custom database tables, no settings to configure. Columns are read-only and, where WordPress supports it, sortable.

## Installation

1. Upload the plugin folder to `/wp-content/plugins/reveal-ids-for-wp-admin-25/`.
2. Activate it from the **Plugins** screen.
3. No configuration needed — the ID column appears immediately on every supported admin list screen.

## Uninstall behavior

On uninstall, the plugin removes its one stored option (`ridwpa_version`) via `uninstall.php` — no other data is written, so there is nothing else to clean up.

## Localization

Ships with translations for English, German, Brazilian Portuguese, Italian, Spanish, Russian, Belarusian, Dutch, European Portuguese, Polish, Romanian, Georgian, Swedish, and Ukrainian (see `readme.txt` for full credits).

## License

GPL-2.0-or-later. See [`LICENSE`](LICENSE) and `readme.txt`.
