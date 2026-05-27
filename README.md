# Pixel2Catch — Project Page

Static project page for **Pixel2Catch: Multi-Agent Sim-to-Real Transfer for Agile Manipulation with a Single RGB Camera** (IEEE RA-L 2026).

Adapted from the [Nerfies](https://github.com/nerfies/nerfies.github.io) template (Bulma CSS).

## Structure

```
project-page/
├── index.html               ← main page
├── static/
│   ├── css/style.css        ← custom styling
│   └── images/              ← figures (JPEG, web-optimized)
│       ├── teaser.jpg
│       ├── system_overview.jpg
│       ├── pixel_features.jpg
│       ├── training_curves.jpg
│       └── real_valid.jpg
└── README.md
```

## Placeholders to fill in

Before publishing, replace the following tokens in `index.html`:

| Token | Where | Example |
|---|---|---|
| `[PAPER-PDF-URL]` | Paper button | `https://ras.papercept.net/.../26-0594.pdf` |
| `[ARXIV-URL]` | arXiv button | `https://arxiv.org/abs/2511.XXXXX` |
| `[GITHUB-URL]` | Code button | `https://github.com/<org>/Pixel2Catch` |
| `[VIDEO-URL]` | Video button (external) | `https://youtu.be/<id>` |
| `[VIDEO-ID]` | YouTube embed in `#video` section | `<id>` only |
| `[FUNDING ORGANIZATION / GRANT NUMBER]` | Footer acknowledgments | actual grant info |

Quick find with:
```bash
grep -nE '\[(PAPER-PDF-URL|ARXIV-URL|GITHUB-URL|VIDEO-URL|VIDEO-ID|FUNDING.*)\]' index.html
```

## Deploying on GitHub Pages

Two common layouts:

### A. Dedicated repo (`<user>.github.io/<repo>`)
Copy the contents of this folder to the repo root:
```bash
# inside an empty repo
cp -r <path-to>/project-page/* .
git add .
git commit -m "Add project page"
git push
```
Then in **Settings → Pages**, select the branch (usually `main`) and `/ (root)`.

### B. `docs/` folder of your code repo
```bash
mkdir -p docs
cp -r <path-to>/project-page/* docs/
git add docs && git commit -m "Add project page" && git push
```
Then in **Settings → Pages**, select branch `main` and `/docs`.

## Local preview

Just open `index.html` in a browser:

```bash
xdg-open index.html       # Linux
open index.html           # macOS
explorer.exe index.html   # Windows (WSL)
```

For relative-path correctness (e.g. on Safari), serve via a tiny HTTP server:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Updating figures

Source PDFs live in `final_version/figures/`. To re-render at higher resolution
or after revising a figure, regenerate the JPEG (web-sized) versions:

```bash
# Example using the project's PDF→PNG flow (document_parse) plus Pillow:
# (see project-page generation script / Feynman session log for details)
```

Final JPEGs should be ≤ ~400 KB each and ≤ 1600 px wide.

## License / Attribution

- Page template adapted from [Nerfies](https://github.com/nerfies/nerfies.github.io)
  (MIT-style attribution-friendly).
- Content © the authors.
