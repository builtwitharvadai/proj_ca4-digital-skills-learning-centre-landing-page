# Digital Skills Learning Centre Landing Page

A modern, accessible, and responsive landing page for the Digital Skills Learning Centre. This is a static, browser-ready website built with vanilla web technologies and designed to be served directly via GitHub Pages without any build step.

## Project Overview

The Digital Skills Learning Centre Landing Page is a single-page website that introduces the centre, showcases its programs, and provides clear pathways for prospective learners to get in touch and enrol. The project emphasises performance, accessibility, and maintainability through a clean modular file structure.

Key goals:

- Fast first-paint and minimal payload (no frameworks, no bundlers)
- Strong accessibility baseline (WCAG 2.1 AA)
- Easy local development — open `index.html` and you are done
- Zero-config deployment to GitHub Pages

## Technology Stack

- **HTML5** — semantic markup for structure and accessibility
- **CSS3** — modern styling with custom properties, Flexbox, and Grid
- **Vanilla JavaScript (ES6+)** — progressive enhancement, no frameworks or build tools

There is no Node.js, npm, bundler, or transpiler involved. All files are written to run directly in the browser.

## File Structure

```
.
├── index.html              # Main entry point for the landing page
├── styles/                 # All stylesheets, split by concern
│   ├── base.css            # Reset, typography, design tokens
│   ├── components.css      # Reusable UI components
│   ├── animations.css      # Motion and transitions
│   └── browser-fixes.css   # Cross-browser compatibility tweaks
├── scripts/                # All JavaScript modules
│   ├── main.js             # Application entry point
│   ├── interactions.js     # UI interaction handlers
│   ├── animations.js       # Scroll and motion effects
│   ├── lazy-loading.js     # Image and asset lazy loading
│   ├── accessibility.js    # A11y enhancements (focus, ARIA, keyboard)
│   └── polyfills.js        # Fallbacks for older browsers
├── assets/                 # Images, icons, fonts, and other media
├── .gitignore              # Files excluded from version control
└── README.md               # This file
```

### Directory Explanations

- **`styles/`** — Modular CSS organised by responsibility. `base.css` defines design tokens and global resets, `components.css` holds component-level rules, `animations.css` isolates motion, and `browser-fixes.css` contains vendor-specific overrides.
- **`scripts/`** — Vanilla JavaScript split into focused modules. Each script handles one concern so that features can be enabled, disabled, or replaced without touching the rest.
- **`assets/`** — Static media including images, icons, and fonts referenced from HTML and CSS.

## Local Development

No build step is required. To run the site locally:

1. Clone the repository:

   ```bash
   git clone https://github.com/builtwitharvadai/digital-skills-learning-centre-landing-page.git
   cd digital-skills-learning-centre-landing-page
   ```

2. Open `index.html` directly in your browser:

   - **macOS:** `open index.html`
   - **Linux:** `xdg-open index.html`
   - **Windows:** `start index.html`

   Or simply double-click `index.html` in your file explorer.

### Optional: Serve via a Local HTTP Server

Some browser features (such as `fetch` against local files and certain security policies) work better when files are served over HTTP rather than the `file://` protocol. Any of the following will work:

```bash
# Python 3
python3 -m http.server 8000

# PHP
php -S localhost:8000

# Node.js (if installed)
npx serve .
```

Then visit `http://localhost:8000` in your browser.

## GitHub Pages Deployment

The site is designed to be deployed directly via GitHub Pages with no build configuration.

1. Push your changes to the `main` branch of the repository.
2. On GitHub, navigate to **Settings → Pages**.
3. Under **Source**, select the `main` branch and the `/ (root)` folder.
4. Click **Save**.
5. GitHub will publish the site at `https://<username>.github.io/<repository-name>/` within a few minutes.

To use a custom domain:

1. Add a `CNAME` file to the repository root containing your domain name.
2. Configure the DNS records for your domain to point to GitHub Pages.
3. Enable **Enforce HTTPS** in the Pages settings once the certificate is issued.

## Browser Compatibility

The landing page is tested and supported on the latest two stable versions of the following browsers:

- Google Chrome
- Mozilla Firefox
- Apple Safari
- Microsoft Edge

Older browsers receive a functional baseline experience through progressive enhancement and the polyfills loaded from `scripts/polyfills.js`.

## Accessibility Standards

This project targets **WCAG 2.1 Level AA** conformance. Key practices include:

- Semantic HTML5 landmarks (`<header>`, `<nav>`, `<main>`, `<footer>`)
- Sufficient colour contrast for text and interactive elements
- Visible focus indicators on all interactive controls
- Full keyboard navigability with logical tab order
- Descriptive `alt` text on meaningful images and ARIA attributes where needed
- Respect for the `prefers-reduced-motion` media query
- Screen reader-friendly form labels and error messages

Please report any accessibility issues you encounter so they can be addressed promptly.

## Contributing

Contributions are welcome. To propose a change:

1. Fork the repository.
2. Create a feature branch: `git checkout -b feature/my-improvement`.
3. Make your changes, keeping the modular file structure intact.
4. Test the page locally in at least one of the supported browsers.
5. Verify keyboard navigation and basic screen reader behaviour for any UI changes.
6. Open a pull request describing the change and the rationale.

Please keep pull requests focused and small. Large refactors should be discussed in an issue first.

## Contact

For questions, feedback, or collaboration enquiries related to the Digital Skills Learning Centre Landing Page, please open an issue on the repository. For matters relating to the Digital Skills Learning Centre itself, refer to the contact information published on the live site.

## License

Unless stated otherwise within individual files, the contents of this repository are intended for use by the Digital Skills Learning Centre and its partners. Refer to the repository owner for licensing details before reuse.
