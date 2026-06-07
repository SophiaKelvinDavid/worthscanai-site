# WorthScan AI — Website

A lightweight, static website for **WorthScan AI**, an umbrella brand for
AI-powered educational field-check apps. It hosts the Google Play readiness,
support, and legal pages for the current app, **Stone Worth AI**.

No backend, no login, no payment, no newsletter, no analytics. Static HTML/CSS
only.

## Pages & routes

| Route | File |
| --- | --- |
| `/` | `index.html` |
| `/stone-worth-ai` | `stone-worth-ai/index.html` |
| `/privacy/stone-worth-ai` | `privacy/stone-worth-ai/index.html` |
| `/terms/stone-worth-ai` | `terms/stone-worth-ai/index.html` |
| `/disclaimer/stone-worth-ai` | `disclaimer/stone-worth-ai/index.html` |
| `/support` | `support/index.html` |
| (404) | `404.html` |

Shared styles live in `styles.css`. Each route uses a directory with an
`index.html` so clean URLs work on common static hosts without extra config.

## Run locally

Any static file server works. Pick one:

```powershell
# Python 3
python -m http.server 8000

# Node (no install)
npx serve .
```

Then open <http://localhost:8000>.

> Note: opening the files directly with `file://` works too, but the absolute
> `/styles.css` and `/route` links resolve correctly only when served from the
> project root, so a local server is recommended.

## Deploy

The site is plain static files — deploy the project root to any static host.

- **Netlify / Cloudflare Pages:** drag-and-drop the folder, or connect the repo.
  Build command: _none_. Publish directory: project root.
- **Vercel:** import the repo; framework preset "Other"; output = root.
- **GitHub Pages:** push to a repo and enable Pages on the branch root.

The directory-based `index.html` structure gives clean URLs
(`/stone-worth-ai`, `/privacy/stone-worth-ai`, etc.) on all of the above.

## Contact

stoneworthai.support@gmail.com
