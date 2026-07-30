# gerebanhaihao.github.io

A lightweight, responsive single-page portfolio site with dark/light theme switching and bilingual (Chinese/English) support. Built with vanilla HTML, CSS, and JavaScript. Zero framework or build step is required.

## Tech Stack

- **HTML** — Semantic structure with `data-theme` for theme control and `lang` for i18n routing
- **CSS** — Custom properties (design tokens) for light/dark themes, CSS Grid for project cards, Flexbox for skill badges, `IntersectionObserver`-driven scroll-reveal animations
- **JavaScript** — ES6+ dynamic content rendering, client-side i18n, theme persistence via `localStorage`, no dependencies
- **Icons** — Font Awesome 6 (CDN) + inline SVG for the Xiaohongshu icon
- **Font** — System font stack (`-apple-system`, `Segoe UI`, etc.)

## Project Structure

```
├── index.html              # Chinese entry point
├── en.html                 # English entry point
├── project.html            # Chinese project detail page
├── project-en.html         # English project detail page
├── assets/
│   ├── css/
│   │   └── style.css       # All styles (tokens, layout, components, responsive)
│   └── js/
│       └── main.js         # Theme toggle, content rendering, scroll animation
└── README.md
```

All project data, experience entries, and skill definitions live in `main.js` as plain JavaScript objects — no backend, no API calls.

## Local Development

No build step. Open the file directly or serve locally:

```bash
# Python 3
python -m http.server 8080

# Node.js (http-server)
npx http-server -p 8080

# VS Code
# Install "Live Server" → right-click index.html → Open with Live Server
```

## Deployment

Push to the `main` branch. GitHub Pages auto-deploys at:

```
https://gerebanhaihao.github.io
```

## Customisation

- **Theme colours** — Edit CSS custom properties under `:root` (light) and `[data-theme="dark"]` in `style.css`
- **Content** — Modify project/experience/skill data arrays in `main.js`
- **Language** — All visible text is rendered from JS data; add or edit entries in the `zh`/`en` objects
- **Images** — Replace files in `assets/images/` (keep filenames to avoid HTML changes)