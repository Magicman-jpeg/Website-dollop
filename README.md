# Jay Clifferson P. Arevalo — Portfolio

A responsive personal portfolio highlighting my Information Technology education, cloud and systems projects, technical skills, and student-community leadership.

## Live Site

[View the portfolio on GitHub Pages](https://magicman-jpeg.github.io/Website-dollop/)

## Features

- Responsive, mobile-friendly layout
- Light and dark themes with saved user preference
- Fixed ASCII-art background with scroll-based parallax
- Animated project cards, section reveals, and typing effect
- Reduced-motion support for accessibility
- Downloadable curriculum vitae

## Technologies

- HTML5
- Tailwind CSS 3
- Vanilla JavaScript
- GSAP and ScrollTrigger
- Remix Icon

## Project Structure

```text
.
├── .kiro/
│   └── skills/
│       └── design-reference-toolkit/  # Reference-informed design workflow
├── assets/
│   ├── css/
│   │   └── tailwind.css       # Compiled stylesheet used by GitHub Pages
│   ├── docs/
│   │   └── jay-arevalo-cv.pdf
│   └── js/
│       └── main.js            # Theme, navigation, and animation behavior
├── src/
│   └── input.css              # Tailwind and custom CSS source
├── index.html                 # Website entry point
├── KIRO_NEXT_SESSION_HANDOFF.md
├── package.json               # Build commands and development dependency
├── package-lock.json          # Reproducible dependency versions
└── tailwind.config.js         # Tailwind theme and content configuration
```

## Local Setup

Requirements: Node.js 18 or newer and npm.

```bash
npm ci
npm run build:css
```

Open `index.html` directly, or serve the repository with any static web server. For example:

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.

During CSS development, run:

```bash
npm run watch:css
```

## Deployment

The repository is prepared for GitHub Pages as a plain static site. In the GitHub repository settings:

1. Open **Settings → Branches** and change the default branch to `main`.
2. Open **Settings → Pages**.
3. Choose **Deploy from a branch**.
4. Select `main`, directory `/ (root)`, then save.

The generated `assets/css/tailwind.css` file is intentionally committed because this Pages configuration does not run the npm build automatically. `.nojekyll` keeps publication on the plain static-file path.

The site loads Google Fonts, Remix Icon, GSAP, and ScrollTrigger from public CDNs, so an internet connection is required for the complete visual experience.
