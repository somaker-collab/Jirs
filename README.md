# HimalAI Ventures Landing Site

Bilingual AI startup landing page (English + Nepali), designed for a Nepal-first, global-ready narrative.

## Files that should exist in your GitHub repo

- `index.html`
- `styles.css`
- `script.js`
- `.github/workflows/deploy-gh-pages.yml`
- `README.md`

If these files are not visible on GitHub, the local commits have not been pushed yet.

## Run locally

```bash
python3 -m http.server 8080
```

Then open: `http://localhost:8080`

## Push everything to GitHub

Run these commands from this repository root:

```bash
git status
git log --oneline -n 5
git remote -v
git push -u origin work
```

If your GitHub default branch is `main`, merge or push the same commits to `main` as well:

```bash
git checkout main
git merge work
git push origin main
```

## Host it (GitHub Pages)

This repo includes a GitHub Actions workflow at `.github/workflows/deploy-gh-pages.yml`.

### Steps

1. Push this branch to your GitHub repository.
2. In GitHub, go to **Settings → Pages**.
3. Under **Build and deployment**, select **Source: GitHub Actions**.
4. Push to your default branch (`main` or `master`) or manually run the workflow from **Actions**.
5. Your site will be available at:
   - `https://<your-github-username>.github.io/<repo-name>/`

## Deploy alternatives

### Netlify
- Drag-and-drop this project folder in Netlify, or connect the repo.
- Build command: *(none)*
- Publish directory: `.`

### Vercel
- Import the repository as a static site.
- Framework preset: **Other**
- Build command: *(none)*
- Output directory: `.`
