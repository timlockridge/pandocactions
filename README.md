# 📄 Pandoc Publish Template

This repository is a GitHub Template that uses **Pandoc** and **GitHub Actions** to convert Markdown files into:

- 📘 A professional PDF (with cover and table of contents)
- 🌐 A responsive HTML website
- 🚀 Automatic deployment to GitHub Pages

---

## ✅ How to Use

1. Click the green **Use this template** button on GitHub.
2. Clone your new repository.
3. Replace files in `src/` with your own Markdown files.
4. Commit and push changes to the `main` branch.

GitHub Actions will:
- Generate a PDF (`output/document.pdf`)
- Generate an HTML website (`output/index.html`)
- Deploy the website to GitHub Pages

---

## 🌍 Live Site

To enable GitHub Pages:

1. Go to **Settings → Pages**
2. Set the source to the `gh-pages` branch and root (`/`) folder
3. Visit: `https://<your-username>.github.io/<your-repo-name>/`

---

## 📁 Folder Structure

```
pandoc-publish/
├── .github/workflows/    # GitHub Actions workflow
├── src/                  # Your Markdown source files
├── assets/               # Custom LaTeX cover and CSS
├── output/               # Generated files (PDF + HTML)
├── metadata.yaml         # Title, author, and date
└── README.md
```

---

## 🛠 Requirements

No local dependencies required! All processing happens via GitHub Actions with:

- `pandoc`
- `xelatex` (via TeX Live)
- `peaceiris/actions-gh-pages`

---

Created by Carlos Evia | 🧠 Structured Authoring + Markdown + GitHub Automation
