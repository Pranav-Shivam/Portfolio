# Pranav Shivam — Portfolio

A single-file portfolio site framed around a build pipeline (Ingest → Design → Build → Validate → Ship → Deploy → Scale → Share) — built as a straight HTML/CSS/JS file with no build step, no framework, and no dependencies beyond two Google Fonts.

**Live site:** _add your deployed URL here once published_

## Features

- **Pipeline-driven layout** — each section is a numbered stage on a dotted rail, echoing how a forward-deployed engineer actually moves work from a client whiteboard to production.
- **Light / dark mode** — a toggle in the nav that respects the visitor's system preference on first load, remembers their choice after that, and degrades gracefully if local storage is unavailable.
- **Fully responsive** — collapses to a mobile hamburger menu below 760px; every grid reflows down to a single column on small screens.
- **Scroll-reveal animation** — sections fade in via `IntersectionObserver`, and the whole thing respects `prefers-reduced-motion`.
- **Zero build step** — open `index.html` directly in a browser, or drop it on any static host.

## Sections

| Stage | Section | Content |
|---|---|---|
| 00 | Now | Current engagement, studies, and next credential |
| 01 | Systems | Production platforms and agents shipped for clients |
| 02 | Lab | Independent side projects, linked to GitHub repos |
| 03 | Impact | Quantified outcomes and metrics |
| 04 | Stack | Tools and technologies used |
| 05 | Journey | Career timeline |
| 06 | Growth | 1-year and 3-year goals |
| 07 | Writing | Long-form articles on Medium |
| — | Connect | Contact links (email, LinkedIn, GitHub, Medium) |

## Tech

Plain HTML, CSS (custom properties for theming), and vanilla JavaScript. Fonts: [Space Grotesk](https://fonts.google.com/specimen/Space+Grotesk) (display), [IBM Plex Sans](https://fonts.google.com/specimen/IBM+Plex+Sans) (body), [IBM Plex Mono](https://fonts.google.com/specimen/IBM+Plex+Mono) (labels/data).

## Running locally

No install needed — just open the file:

```bash
open index.html        # macOS
start index.html       # Windows
xdg-open index.html    # Linux
```

Or serve it if you prefer a local server:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploying to GitHub Pages

1. Rename the file to `index.html` if it isn't already.
2. Push it to the root of this repo (or a `docs/` folder — your choice).
3. In the repo, go to **Settings → Pages**, set the source branch to `main` and the folder to `/ (root)` (or `/docs`).
4. Your site will be live at `https://<your-username>.github.io/<repo-name>/` within a few minutes.

If you want it at the bare `https://<your-username>.github.io` root instead, name the repo exactly `<your-username>.github.io` and Pages will serve it automatically from `main`.

## Customizing

All content lives directly in the HTML — no CMS, no data files. To update:

- **Projects / Lab items** — edit the `.card` and `.lab-item` blocks inside `#systems` and `#lab`.
- **Metrics** — edit the `.ledger-row` blocks inside `#impact`.
- **Writing** — add a new `.tl-item` block inside `#writing` for each new article.
- **Colors** — all theme colors are CSS custom properties at the top of the `<style>` block (`:root` for light mode, `html[data-theme="dark"]` for dark mode).

## License

Personal portfolio — feel free to fork the structure for your own site, but please swap out the content, projects, and metrics for your own.
