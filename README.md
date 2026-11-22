# Tekromancy Glyphrig Bookmarks

A data-only bookmark directory managed by **[Glyphrig](https://github.com/Glyphrig/Glyphrig)** — two-way browser-to-Git bookmark sync & static directory generator.

## Structure

- `bookmarks/**/README.md` — Your synced bookmark folders in Markdown
- `glyphrig.config.yaml` — Site title, theme accent, enrichment, and optional PWA Quick Add

## Publishing

1. Push this repository to GitHub (`main` branch).
2. Open **Settings -> Pages -> Build and deployment -> Source** and select **GitHub Actions**.
3. [`deploy.yml`](./.github/workflows/deploy.yml) builds and publishes your site automatically whenever `bookmarks/**` or `glyphrig.config.yaml` changes.

## Connecting the Browser Extension

1. Create a dedicated folder in Chrome or Firefox (for example `Bookmarks Bar/Public Bookmarks`).
2. Open **Glyphrig Settings**, configure this repository (`bookmarks` folder on `main`), authenticate via GitHub Device Flow or a scoped Personal Access Token, select your folder, and confirm the initial dry-run preview.

## Local Preview & Validation

```bash
npx --yes @glyphrig/cli@0 validate
npx --yes @glyphrig/cli@0 dev
```

---

Powered by **[Glyphrig](https://github.com/Glyphrig/Glyphrig)** (`npx @glyphrig/cli@0 init`).
