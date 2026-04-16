# Borderless Email Signature Builder

Self-hosted signature builder for the Borderless team.

Open the site in a browser, upload a profile photo, edit the phone number, and click Copy signature. Paste into Gmail: Settings → See all settings → General → Signature → Create new → paste.

## Local preview

Open `index.html` in any browser. Everything runs client-side.

## Deploy (Railway)

Caddy-served static site. Nixpacks installs Caddy and serves `index.html` on the port Railway assigns.

- `Caddyfile` serves the root with CSP that permits inline styles/scripts and `data:` URIs for uploaded photos.
- `nixpacks.toml` pins Caddy as the runtime.
