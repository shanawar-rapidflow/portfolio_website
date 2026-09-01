# Malaika Maqsood — Portfolio Website

Interaction design portfolio built with plain HTML, CSS and JavaScript, deployable via GitHub Pages.

## Structure

```
Portfolio-website/
├── index.html              # Home page (served at the site root)
├── assets/
│   ├── css/
│   │   ├── base.css        # Design tokens, reset, typography, shared utilities
│   │   ├── components.css  # Navbar, footer — shared across every page
│   │   └── home.css        # Home page specific styles
│   ├── js/
│   │   └── main.js         # Sticky nav, mobile menu, scroll-reveal animations
│   └── images/              # Real images go here, replacing the placeholder blocks
└── pages/                   # Future pages (about, work, project detail, etc.)
    └── <page-name>/
        ├── index.html
        └── index.css
```

Each additional page gets its own folder under `pages/` with its own HTML and CSS
file, and reuses `assets/css/base.css` + `assets/css/components.css` for shared
styling.

## Design system

- **Colors:** `#0D0F12` background, `#F5F3EF` text, `#C9D6CC` sage, `#A65E4D` rust, `#3B5A6B` blue accents.
- **Fonts:** Playfair Display (headings), Inter (body) — loaded from Google Fonts.
- **Motion:** scroll-triggered fade/slide-up reveals via `IntersectionObserver`, respecting `prefers-reduced-motion`.

## Local preview

Open `index.html` directly in a browser, or serve the folder with any static
server (e.g. `npx serve .`) for correct relative paths.

## Deploying to GitHub Pages

1. Push this repo to GitHub.
2. In the repo settings, enable **Pages** → deploy from the `main` branch, root folder.
3. The site will be live at `https://<username>.github.io/<repo-name>/`.
