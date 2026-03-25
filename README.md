# HimalAI Ventures Landing Site

Bilingual AI startup landing page (English + Nepali), designed for a Nepal-first, global-ready narrative.

## Files in this repo

- `index.html`
- `styles.css`
- `script.js`
- `wrangler.toml`
- `.github/workflows/deploy-cloudflare-pages.yml`
- `.github/workflows/deploy-gh-pages.yml`
- `README.md`

## Run locally

```bash
python3 -m http.server 8080
```

Then open: `http://localhost:8080`

## Host with Cloudflare Pages (Recommended)

This repo includes a Cloudflare deployment workflow at `.github/workflows/deploy-cloudflare-pages.yml`.

### 1) Create Cloudflare Pages project

1. Go to Cloudflare Dashboard → **Workers & Pages** → **Create application** → **Pages**.
2. Create a project named **`himalai-ventures-site`** (or update the workflow `projectName` to match your project).

### 2) Create API token

Create a Cloudflare API token with permissions:
- **Account → Cloudflare Pages:Edit**
- **Zone → Zone:Read** (if needed by your account policy)

### 3) Add GitHub repository secrets

In GitHub: **Settings → Secrets and variables → Actions**, add:

- `CLOUDFLARE_API_TOKEN`
- `CLOUDFLARE_ACCOUNT_ID`

### 4) Push and deploy

```bash
git push -u origin work
```

Then either:
- merge to `main` and push, or
- run workflow manually in **GitHub Actions**.

Your Cloudflare Pages URL will look like:

- `https://himalai-ventures-site.pages.dev`

## Optional: GitHub Pages fallback

You can still use `.github/workflows/deploy-gh-pages.yml` if you want GitHub Pages as a backup host.
