# Epstein Filter

Epstein Filter is a frontend-only web app for hiding faces in images by placing movable and resizable black boxes, then downloading the edited image.

## Features

- Upload an image from your device
- Add multiple black boxes
- Drag boxes to position them
- Resize boxes with a corner handle
- Delete selected box with button or keyboard (`Delete`/`Backspace`)
- Download final image as PNG
- Mobile-first UI

## Tech Stack

- Plain HTML, CSS, and JavaScript
- No backend
- Static hosting ready
- Docker support for Fly.io deployment

## Project Files

- `index.html` - Main app UI and logic
- `Dockerfile` - Container image definition
- `fly.toml` - Fly.io app configuration
- `robots.txt` - Crawler rules
- `sitemap.xml` - Sitemap
- `og.jpeg` - Social preview image

## Run Locally

Open `index.html` directly in a browser.

Or run a static server:

```bash
python3 -m http.server 8080
```

Then open `http://localhost:8080`.

## Deploy to Fly.io

1. Install and log in to Fly CLI:

```bash
fly auth login
```

2. If app does not exist yet:

```bash
fly apps create epstein-filter
```

3. Deploy:

```bash
fly deploy
```

## SEO

SEO and social metadata are in `index.html`, including:

- Canonical URL
- Open Graph tags
- Twitter Card tags
- JSON-LD (`WebApplication`)

Crawler files:

- `robots.txt`
- `sitemap.xml`

## Notes

- Image processing happens in the browser.
- On iPhone, websites cannot save directly to Photos without user action; use Share or Save flow.
