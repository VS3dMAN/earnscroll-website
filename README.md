# EarnScroll — Marketing & Legal Site

Static marketing landing page + legal documents for **EarnScroll: Screen-Time Gym**.
Zero build step, zero framework, zero backend — just HTML, CSS, and a sprinkle of vanilla JS.

## Pages

| URL | File |
|-----|------|
| `/` | `index.html` |
| `/privacy-policy/` | `privacy-policy/index.html` |
| `/terms-of-service/` | `terms-of-service/index.html` |
| `/support/` | `support/index.html` |
| `404` | `404.html` |

The legal pages are plain pre-rendered HTML and work with JavaScript disabled — safe to submit
as the Privacy Policy / Terms URLs in Google Play Console.

## Local preview

Any static server works. From this `website/` folder:

```bash
npx serve .
# or
python -m http.server 8080
```

Then open http://localhost:8080

## Deploy

The directory-based structure gives clean URLs (`/privacy-policy/`) out of the box on all three hosts.

- **Vercel** — set the project root to this `website/` folder (or import and set "Output Directory" = `website`). No build command.
- **Netlify** — set "Publish directory" to `website`. No build command.
- **GitHub Pages** — push the contents of `website/` to the `gh-pages` branch (or `/docs`).

## Assets

- `images/dashboard.png`, `workout.png`, `ai-detection.png`, `blocker.png` — app screenshots.
- `images/og-image.png` — 1200×630 social share card (regenerate with `../_og-src` template if needed).
- `images/favicon.png` — app icon.

## Editing

- Colors, spacing, and the whole design system live in CSS custom properties at the top of `css/style.css`.
- Copy is inline in each HTML file. Update the Play Store URL (`com.earnscroll.app`) everywhere once the listing is live.
