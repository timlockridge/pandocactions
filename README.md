# 📄 Pandoc Publish Template

This repository is a GitHub Template that uses **Pandoc** and **GitHub Actions** to convert Markdown files into:

- 📘 A professional PDF (with cover and table of contents)
- 🌐 A responsive HTML website
- 📖 An EPUB ebook with cover and metadata
- 🚀 Automatic deployment to GitHub Pages

---

## ✅ How to Use

1. Click the green **Use this template** button on GitHub.
2. Clone your new repository.
3. Replace files in `src/` with your own Markdown files.
4. Commit and push changes to the `main` branch.

GitHub Actions will:
- Generate a PDF (`output/document.pdf`)
- Generate an EPUB (`output/document.epub`)
- Generate an HTML site (`output/index.html`)
- Deploy the HTML site to GitHub Pages

---

## 🔐 GitHub Actions Permissions for Pages Deployment

To allow GitHub Actions to publish your HTML site to GitHub Pages, make sure to:

1. Go to **Settings → Actions → General**
2. Scroll down to **Workflow permissions**
3. Select ✅ "**Read and write permissions**"
4. Click **Save**

---

## 📖 EPUB Generation Instructions

The workflow automatically creates an EPUB file (`document.epub`) in the `output/` folder. To customize the EPUB:

1. Add a cover image named `cover.jpg` to the `assets/` folder.
2. Include metadata in `metadata.yaml` like this:

```yaml
title: "Your Document Title"
author: "Carlos Evia"
date: "2025-05-05"
lang: "en"
identifier: "urn:isbn:1234567890"
```

The EPUB will include:
- ✅ Cover image
- ✅ Navigable table of contents
- ✅ Metadata (title, author, language, identifier)

You can download the EPUB from the GitHub Actions artifacts or include it in your GitHub Pages site if desired.

---

## 🌍 Enable GitHub Pages

1. Go to **Settings → Pages**
2. Set the source to the `gh-pages` branch and root (`/`) folder
3. Visit your live site at: `https://<your-username>.github.io/<your-repo-name>/`

---

## 📁 Folder Structure

```
pandoc-publish/
├── .github/workflows/    # GitHub Actions workflow
├── src/                  # Your Markdown source files
├── assets/               # Custom LaTeX cover, CSS, and EPUB cover
├── output/               # Generated files (PDF, EPUB, HTML)
├── metadata.yaml         # Title, author, and metadata
└── README.md
```

---

## 🛠 Requirements

No local dependencies required! All processing happens via GitHub Actions with:

- `pandoc`
- `xelatex` (via TeX Live)
- `peaceiris/actions-gh-pages`

---

Created by Carlos Evia with help from your uncle ChatGPT | 🧠 Structured Authoring + Markdown + GitHub Automation
