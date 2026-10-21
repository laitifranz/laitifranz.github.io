# laitifranz.github.io

This repository is the GitHub Pages **user site** for [laitifranz](https://github.com/laitifranz). It redirects all visitors from `laitifranz.github.io` to the new site at **[laitifranz.pages.dev](https://laitifranz.pages.dev)**, preserving the full path, query string, and hash fragment.

## Why the site moved

My site's source code lives in a private repository. GitHub Pages only deploys from private repos on paid plans (Pro, Team, or Enterprise). When my GitHub Pro subscription lapsed, the deployment stopped and the site went offline—hosting depended on keeping a paid plan active. Cloudflare Pages builds from private repos on its free tier, so the site no longer depends on a GitHub subscription. This repo stays public only to keep old `laitifranz.github.io` links working.

## Where the real site lives

The actual website is in a private repository ([laitifranz/personal-website](https://github.com/laitifranz/personal-website)) and deployed via Cloudflare Pages at [laitifranz.pages.dev](https://laitifranz.pages.dev).

## How it works

- `index.html` handles requests to the root.
- `404.html` handles all other paths (GitHub Pages serves this for unknown routes, enabling deep-link redirects).
- Both files use JavaScript `location.replace()` to redirect while preserving path, query, and hash. A `<meta http-equiv="refresh">` fallback redirects to the base URL if JavaScript is disabled.

## Changing the target URL

Edit the `TARGET_BASE` constant at the top of each file (`index.html` and `404.html`).

## GitHub Pages setup

To serve this redirect site, enable GitHub Pages in **Settings → Pages**:

- **Source**: Deploy from a branch
- **Branch**: `main`
- **Folder**: `/ (root)`

## Project pages

Other public repositories of this user (e.g., [MemCoach](https://github.com/laitifranz/MemCoach)) serve their own project pages at `laitifranz.github.io/<repo>/`. Those are handled by their respective repositories and are **not affected** by this user site redirect.
