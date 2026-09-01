# DevArt Video for Joomla

Modern video management package for Joomla 6, designed for news portals, magazines, video libraries, media organizations, educational websites, businesses and high-traffic websites.

![Joomla](https://img.shields.io/badge/Joomla-6.x-blue)
![PHP](https://img.shields.io/badge/PHP-8.3.0%2B-green)
![Release](https://img.shields.io/badge/Version-1.1.2-orange)
![License](https://img.shields.io/badge/License-GPLv3-red)

---

## Overview

DevArt Video is a modern Joomla 6 video platform designed from the ground up for performance, security, stability and scalability.

It allows administrators to create and manage professional video libraries with categories, featured videos, YouTube integration, local videos, responsive playback and structured video information while remaining lightweight and easy to maintain.

The package includes an administrator component, a frontend module, and a scheduled task plugin. All extensions update together through the package.

---

## Features

### Video Library

Create and manage:

- Video library
- Categories with unlimited hierarchy
- Featured videos
- Video thumbnails
- Poster images
- Video descriptions
- YouTube videos
- Local videos
- Publication controls
- Ordering
- Search and filtering

---

### Video Sources

Supports multiple video sources.

Features:

- YouTube
- Self-hosted MP4 videos
- Self-hosted WEBM videos
- Scheduled source synchronization

---

### Responsive Video Player

Built-in responsive HTML5 video player.

Features:

- Responsive layout
- Poster image support
- HTML5 playback
- Mobile friendly
- Lightweight frontend
- Browser-native controls
- Embed support with constrained CSP and no-store cache headers

---

### Frontend

Included frontend views:

- Video Listing
- Video Detail
- Category Listing

Features:

- Responsive layouts
- SEO-friendly URLs
- Category filtering with subcategory support
- Featured videos
- Video search with FULLTEXT prefix matching for Latin queries
- HTTP 404 for missing or unpublished single videos

---

### Image Upload Optimization

Built-in image optimization during upload.

Features:

- Automatic resize
- Configurable maximum width
- Configurable maximum height
- Optional WEBP conversion
- JPEG quality control
- WEBP quality control
- Automatic safe filename generation
- Aspect ratio preservation
- No upscaling
- Existing Media Manager images remain untouched

---

### Import / Export

Portable video library management.

Features:

- Complete JSON backup
- Complete JSON restore
- Video-specific JSON catalog backup in Tools
- Safe validation
- Portable configuration

---

### Maintenance Tools

Built-in administrator tools.

Features:

- Cache management
- Cache cleanup
- Video maintenance
- Category rebuild
- Default category installer
- Default category removal
- Scheduled task plugin for sync and maintenance

---

### Native DevArt Integration

Integrates with other DevArt extensions.

Supported integrations:

- DevArt Slider
- DevArt Widgets

Videos can be displayed using the native rendering engines of both extensions without additional plugins.

---

### Joomla Native Updates

Supports Joomla native package updates via GitHub.

Update Server:

https://raw.githubusercontent.com/devartgr/joomla-devart-video/main/update.xml

Important:

- Updates are advertised for **`pkg_devartvideo`** only
- Update type: **`package`**
- Client: **`site`**
- Component, module, and task plugin always update together

---

## Included Extensions

This package installs:

- `com_devartvideo` — administrator component
- `mod_devartvideo` — site module
- `plg_task_devartvideo` — scheduled task plugin

Always install and update the **package ZIP**, not the child extensions separately.

---

## Requirements

- Joomla 6.0+
- PHP 8.3.0+

---

## Performance

Designed for production environments.

Features:

- Joomla native MVC architecture
- Optimized database queries
- Cache-first rendering
- Cloudflare friendly
- CDN friendly
- Large video library ready
- Low frontend overhead

Suitable for:

- News portals
- Video libraries
- Magazine websites
- Educational websites
- Business websites
- Media organizations
- High-traffic Joomla websites

---

## SEO

Built with search engines in mind.

Features:

- SEO-friendly URLs
- Video structured data (Schema.org VideoObject)
- Open Graph metadata
- Social sharing metadata
- Clean HTML output

---

## Security Highlights

- Joomla ACL support
- CSRF protection
- Prepared SQL statements
- Secure JSON import/export
- Safe file upload validation
- Safe output escaping
- Public access, language, and publish window enforcement
- Local media and thumbnail paths contained under the site root
- Joomla native architecture

---

## Languages

Shipped frontend and administrator languages include:

- English (en-GB)
- French (fr-FR)
- German (de-DE)
- Spanish (es-ES)
- Italian (it-IT)
- Portuguese (pt-PT)

---

## Compatibility

Supported:

- Joomla 6.x
- PHP 8.3.0+
- Joomla native package updates
- Modern Joomla MVC architecture

Not Supported:

- Joomla 3
- Joomla 4
- Joomla 5
- PHP 7.x
- PHP 8.0–8.2

---

## Current Version

1.1.2

---

## What's New in 1.1.2

Stability release for large video libraries in the administrator.

### Fixes

- Removed the **All** list-limit option; page size is capped at **200** on the videos list and other administrator lists
- Trash, restore, and delete process selected IDs in safe chunks
- Restore from trash republishes videos instead of leaving them unpublished
- YouTube imports without a source default category fall back to the **Default** category

### Additions

- Install and update ensure a published **Default** category under ROOT
- Existing uncategorized videos are **not** mass-reassigned on install/update (safe for large libraries)

---

## What's New in 1.1.1

Administrator UI polish and language expansion on top of the package-only update channel from 1.1.0.

### Settings & Options

- Settings tabs use bordered option groups for List, Detail, Categories, Media, and Embed
- Component Options Permissions tab restored
- General options grouped: Menus, Cache & Batches, Automatic Sync, Local Video, Debug

### Administrator hubs

- Dashboard and Tools use Article Tools-style action cards
- Tools split into Settings, Options, Backup/Cache, Maintenance, and Diagnostics

### Languages

- Expanded to 15 locales with key and sprintf parity against en-GB
- Added: cs-CZ, nl-NL, pl-PL, ru-RU, uk-UA, ja-JP, tr-TR, zh-CN
- Task plugin languages ship with the package even when the site language pack is missing

### Fix

- Admin settings watch-link placeholder resolves from administrator language files

---

## What's New in 1.1.0

Production-ready cumulative release since 1.0.0.

### Updates & Infrastructure

- Joomla native updates now target the package only (`pkg_devartvideo`, site client)
- Public `update.xml` no longer advertises the component as a separate update channel
- PHP minimum aligned to 8.3.0

### Fixes

- Missing or unpublished single videos return HTTP 404
- Category listings honour Include subcategories
- Category descriptions use safe HTML and Joomla content prepare
- Listing tag and featured filters honour filter visibility
- Administrator custom fields use WebAssetManager inline scripts
- External cron accepts GET only

### Security & Stability

- Public queries enforce access, language, and publish window visibility
- Embed responses use private no-store cache headers and constrained CSP
- Installer fails fast on schema errors
- Local media and thumbnail paths stay contained under the site root

### Additions

- Frontend, administrator, plugin, package, and module languages for fr-FR, de-DE, es-ES, it-IT, and pt-PT
- Video-specific JSON catalog backup in Tools
- Latin FULLTEXT BOOLEAN prefix search on frontend listings

---

## What's New in 1.0.0

### Added

- Initial public release
- Video library management
- Video categories
- YouTube support
- Local video support
- Featured videos
- Responsive HTML5 player
- Complete JSON backup and restore
- Maintenance tools
- Automatic image optimization
- Optional WEBP conversion
- GitHub update server support
- Native integration with DevArt Slider
- Native integration with DevArt Widgets

### Improved

- Administrator workflow
- Video thumbnail handling
- Large library performance
- Joomla 6 native architecture
- Cache-first rendering

---

## Author

Kostas Stathopoulos  
DevArt

https://devart.gr

GitHub Repository:

https://github.com/devartgr/joomla-devart-video

---

## License

GNU General Public License v3.0 (GPLv3)

---

## Disclaimer / Limitation of Liability

This software is provided "as is", without warranty of any kind.

DevArt shall not be held liable for any damages, data loss, downtime, security incidents, business interruption, loss of profits, or other consequences arising from the use or inability to use this software.

Always test updates in a staging environment before deploying to production systems.
