# EarnScroll — Marketing & Legal Site

Static marketing landing page + legal documents for **EarnScroll: Screen-Time Gym**.
Zero build step, zero framework, zero backend — just HTML, CSS, and a sprinkle of vanilla JS.

## Pages

| URL | File |
|-----|------|
| `/` | `index.html` |
| `/privacy` | `privacy.html` |
| `/terms` | `terms.html` |
| `/delete-account` | `delete-account.html` |
| `/support` | `support.html` |
| `404` | `404.html` |

Clean URLs (no `.html`, no trailing slash) are configured via `vercel.json` (`cleanUrls: true`,
`trailingSlash: false`). `/privacy-policy` and `/terms-of-service` 301-redirect to the new paths.

The canonical URLs `/privacy`, `/terms`, and `/delete-account` match `WEB_LEGAL_URLS` in the app's
`constants/legal.ts` and are the ones submitted to Google Play Console. The legal pages are plain
pre-rendered HTML and work with JavaScript disabled.

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
