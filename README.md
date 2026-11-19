# cabaana.com

Static single-page site for Cabaana Inc. (Heto + Provero). Replaces the Wix site.

- `index.html`: the whole page (inline CSS/JS)
- `assets/`: logos
- `products/`, `about/`, `contact/`: redirect the old Wix URLs to the matching section
- `.nojekyll`: serve files as-is on GitHub Pages

The contact form opens the visitor's email app with a pre-filled message to info@cabaana.com, or provero@cabaana.com when "Provero" is selected.

## Hosting

GitHub Pages from the `main` branch of `ganpy/cabaana-site` (same setup as provero.dev). To publish a change, push to `main`. It goes live in about a minute.

Preview locally with `npx serve -l 8760 .`, or the `cabaana-site` entry in `Provero/.claude/launch.json`.

## Domain

cabaana.com is registered at Hover. At Hover, DNS needs:

| Type | Host | Value |
|---|---|---|
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |
| CNAME | www | ganpy.github.io |
| MX | @ | smtp.google.com (priority 1), for Google Workspace email |
