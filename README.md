# static.manho.name.my

Centralized static asset repository for Manho's websites and web applications.

All production assets are served through:

https://static.manho.name.my/

## Structure

```text
static.manho.name.my/
├── global/
│   ├── favicon/
│   ├── icons/
│   ├── fonts/
│   └── images/
├── blog/
│   └── images/
├── portfolio/
│   └── images/
├── cms/
│   ├── images/
│   └── icons/
└── README.md
```

## Naming

Use lowercase kebab-case for all filenames.

Good:

```text
human-physiology.webp
manho-avatar.webp
github-icon.svg
favicon-32x32.png
```

Avoid spaces, uppercase letters, and unclear filenames.

## File Formats

Use modern and optimized formats whenever possible.

- Images: WebP / AVIF
- Icons: SVG
- Fonts: WOFF2
- Favicons: PNG / ICO

Optimize images before uploading.

## Versioning

Published assets should preferably be immutable.

When an asset changes, create a new version instead of replacing the existing file.

```text
logo-v1.svg
logo-v2.svg

avatar-v1.webp
avatar-v2.webp
```

## URLs

Always use the custom static domain for production assets.

Example:

```text
https://static.manho.name.my/blog/images/example-v1.webp
```

Do not use GitHub Raw URLs directly in production websites.

## Caching

Static assets should use long-term browser and CDN caching.

Recommended:

```http
Cache-Control: public, max-age=31536000, immutable
```

Versioned filenames should be used when an asset is updated.

## Rules

- Keep this repository for static assets only.
- Do not store secrets or private files.
- Keep filenames simple and consistent.
- Optimize assets before uploading.
- Do not unnecessarily overwrite published assets.
- Use `static.manho.name.my` for production asset URLs.
- Keep the directory structure organized and predictable.

## Goal

This repository provides a stable and centralized asset layer for all Manho web projects.

The underlying hosting or CDN provider may change in the future, but production websites should continue using:

```text
https://static.manho.name.my/
```
