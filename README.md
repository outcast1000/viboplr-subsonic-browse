# Viboplr — Subsonic Browse

Search, stream, and download across multiple Subsonic/Navidrome servers live — no indexing. A discovery layer for servers you visit, separate from your indexed Library.

Externalized from [Viboplr](https://viboplr.com)'s built-in plugins — same code, now shipped as a standalone gallery plugin (id `subsonic-browse`).

## Layout
- `manifest.json` — plugin metadata and contributions.
- `index.js` — the plugin code (ES5, executed via `new Function("api", code)`).
- `scripts/` — `bump.sh` (version + changelog) and `package.sh` (build `subsonic-browse.zip` + `update.json`).

## Releasing
See [RELEASING.md](./RELEASING.md): `scripts/bump.sh <patch|minor|major>`, fill the changelog, commit, then push a `vX.Y.Z` tag — CI builds `subsonic-browse.zip` + `update.json` and publishes the release.
