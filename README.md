# 寶鴻防水防熱材料 — Website

Static site. Deploy on GitHub Pages.

## Deploy

1. Create a new GitHub repo (e.g. `baohong-site`).
2. Upload the contents of this folder to the repo root (index.html, support.js, assets/, .nojekyll).
3. Repo → Settings → Pages → Source: "Deploy from a branch", Branch: `main`, Folder: `/ (root)` → Save.
4. Site goes live at `https://<user>.github.io/<repo>/` in a minute or two.

Or via command line:

```bash
git init
git add .
git commit -m "site"
git branch -M main
git remote add origin https://github.com/<user>/<repo>.git
git push -u origin main
```

## Notes

- `.nojekyll` must stay — it stops GitHub from filtering files.
- React is loaded from unpkg at runtime, so the site needs an internet connection (normal for a public website).
- Asset paths are relative, so the site works from a subdirectory URL.
- Missing images (product-*.jpg, service-*.jpg, blog-*.jpg) still render as placeholders; drop real photos into `assets/` with those filenames to fill them.
