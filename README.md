# E2ALERT

A static landing page for E2ALERT — instant eBay leads for high-ROI arbitrage. Plain HTML/CSS/JS, no build step, ready for GitHub Pages.

## File structure

```
.
├── index.html
├── styles.css
├── script.js
└── assets/
    ├── logo-blue.png        (header logo, light backgrounds)
    ├── logo-white.png       (footer logo, dark backgrounds)
    ├── hero.jpg
    ├── faq-illustration.png
    └── favicon-32.png, favicon-192.png
```

## Before you publish

- Replace the `https://t.me/e2alert` placeholder links (there are 3 — header, "Join Now" CTA, footer, final banner) with your real Telegram channel URL.
- Update the FAQ answers if you want different wording — items 2–5 were written to match the tone of item 1 since only the first was visible in the original source screenshot.

## Deploy with GitHub Pages

1. Create a new repository on GitHub (e.g. `e2alert-site`) and push these files to the `main` branch:

   ```bash
   git init
   git add .
   git commit -m "Initial site"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<your-repo>.git
   git push -u origin main
   ```

2. On GitHub, go to **Settings → Pages**.
3. Under **Build and deployment → Source**, choose **Deploy from a branch**.
4. Pick **Branch: main**, folder **/(root)**, then **Save**.
5. Your site will be live in a minute or two at:
   `https://<your-username>.github.io/<your-repo>/`

If you'd rather use a custom domain, add a `CNAME` file with your domain name at the repo root and point your DNS at GitHub Pages.

## Local preview

No build tools needed — just serve the folder:

```bash
python3 -m http.server 8000
```

Then open `http://localhost:8000`.
