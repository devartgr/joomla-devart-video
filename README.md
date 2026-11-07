# DevArt Video

DevArt Video is a Joomla 6 video platform package for managing, synchronizing,
and presenting YouTube and local videos.

## Requirements

- Joomla 6+
- PHP 8.3+

## Package

Version `1.2.1` contains:

- `com_devartvideo`
- `mod_devartvideo`
- `plg_task_devartvideo`
- `plg_content_devartvideocomments` (thin DevArt Comments host)

The component provides the administrator dashboard, videos, categories, tags,
sources, advertising, sync history, tools, settings, and embed management, plus
the frontend video views and players. The site module displays curated video
lists or a player. The task plugin runs scheduled source synchronization. The
content plugin optionally mounts the DevArt Comments panel on video detail when
`com_devartcomments` is installed and Comments Settings `enable_video` is On.

## Development

`source/` is the only development source. Generated packages belong under
`builds/`.

Validate and build with:

```shell
php scripts/validate.php
php scripts/build.php
```

The build script follows `source/package/pkg_*.xml`, creates only the inner ZIPs
declared by that manifest, and writes an outer package plus its SHA-256 file.

## Verification

Repository validation and package generation do not constitute Joomla runtime
verification. Complete `qa/checklist.md` in a real Joomla installation before
recording the baseline as verified.
