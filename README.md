# Hiralix — Making Education Interactive

A responsive, colorful, child-friendly educational website built with plain HTML, CSS, and JavaScript — no frameworks, no build step, ready for GitHub Pages.

## Folder structure

```
hiralix/
├── index.html
├── css/
│   └── style.css
├── js/
│   └── script.js
├── images/
│   └── favicon.svg
└── assets/
```

## Running locally

Just open `index.html` in a browser, or serve the folder with any static server, e.g.:

```
npx serve .
```

## Deploying to GitHub Pages

1. Create a new GitHub repository (e.g. `hiralix`).
2. Push the contents of this folder to the repository's default branch (`main`).
3. In the repo, go to **Settings → Pages**.
4. Under "Build and deployment", set **Source** to `Deploy from a branch`, branch `main`, folder `/ (root)`.
5. Save — your site will publish at `https://<your-username>.github.io/hiralix/`.

## Customizing

- **Colors & fonts**: all defined as CSS custom properties at the top of `css/style.css` (see `:root`), so you can re-theme the whole site from one place.
- **Logo / mascot / hero art / game thumbnails**: currently built as inline SVG placeholders directly in `index.html` so the site looks complete out of the box. Swap any of them for your own artwork by dropping files into `images/` and replacing the relevant `<svg>...</svg>` block with an `<img src="images/your-file.svg" alt="...">` tag.
- **Games**: each game card currently links to `#`. Point the "Play Now" buttons to your actual game pages/files once they exist.
- **YouTube videos**: replace the placeholder boxes in the YouTube section with real `<iframe>` embeds when videos are ready.
- **Forms**: the newsletter and contact forms are front-end only (they confirm submission locally via `js/script.js`). Connect them to a real backend or a form service such as Formspree, and update the `<form>` `action`/`method` attributes plus the JS as needed.

## Accessibility & performance notes

- Semantic landmarks (`header`, `nav`, `main`, `section`, `footer`) and a "Skip to main content" link are included.
- All interactive elements have visible keyboard focus states.
- Animations respect `prefers-reduced-motion`.
- No external JS frameworks; Google Fonts is the only external resource (optional — remove the `<link>` tags in `<head>` to run fully offline, the design falls back to system fonts gracefully).
