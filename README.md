# What's Your Net Worth

A free, private, single-page net worth card maker. Enter your numbers, get a rank and a shareable image card. Everything runs in the browser, so nothing is uploaded or saved.

## Project structure

```
public/
  index.html   # the whole app (HTML + CSS + JS)
  robots.txt
render.yaml    # Render Static Site config
```

## Run locally

No build step. Either open `public/index.html` in a browser, or serve it:

```bash
cd public && python3 -m http.server 8000
# open http://localhost:8000
```

## Deploy to GitHub

```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/<your-username>/net-worth-card.git
git push -u origin main
```

## Deploy to Render

**Option A: Blueprint (uses `render.yaml`)**
1. Render Dashboard → **New** → **Blueprint**.
2. Connect your GitHub repo and click **Apply**.

**Option B: Manual**
1. Render Dashboard → **New** → **Static Site**.
2. Connect the repo, then set:
   - **Build Command:** *(leave empty)*
   - **Publish Directory:** `public`
3. Click **Create Static Site**.

Every push to `main` redeploys automatically.

## Before going live

- Optionally add `og:url`, `og:image` and a `<link rel="canonical">` once you know your Render URL (or custom domain).
