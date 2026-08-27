# Excel Explained

Interactive, single-file explainers for how Excel really works. Live at
`https://<your-username>.github.io/excel-explained/` once GitHub Pages is enabled.

## Structure

```
excel-explained/
├── index.html          Landing page listing every explainer
├── offset/
│   └── index.html      OFFSET(): walk a reference around a live grid
└── README.md
```

Each explainer is one self-contained `index.html` (no build step, no dependencies),
served at the folder's URL, e.g. `/excel-explained/offset/`.

## One-time setup

1. Create a new **public** repo on GitHub named `excel-explained` (don't initialize
   it with a README, since this folder already has one).
2. From this folder, push it:

   ```
   git init
   git add .
   git commit -m "Excel Explained: landing page and OFFSET explainer"
   git branch -M main
   git remote add origin https://github.com/<your-username>/excel-explained.git
   git push -u origin main
   ```

3. On GitHub: **Settings → Pages → Build and deployment**, set Source to
   **Deploy from a branch**, choose `main` and `/ (root)`, and save.
4. Wait a minute or two. The site appears at
   `https://<your-username>.github.io/excel-explained/`.

Every later `git push` updates the live site automatically.

## Adding a new explainer

1. Make a new folder named after the function, lowercase: `xlookup/`, `sumifs/`.
2. Put the finished page in it as `index.html`.
3. In the root `index.html`, copy the existing `<li>` block in the explainer list,
   point its `href` at the new folder, and update the name and blurb.
4. Commit and push.
