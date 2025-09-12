# 📄 Pandoc Multi-Format Site Template

This template uses **Pandoc** and **GitHub Actions** to turn simple Markdown files into a polished documentation site with:

- 📘 PDF output (with cover page and table of contents)
- 🌐 Responsive multi-page HTML website with dynamic navigation
- 📖 EPUB ebook with metadata and optional cover image
- 🚀 Automatic deployment to GitHub Pages

---

## 🚀 Getting Started

1. **Use this template** to create your own repository on GitHub.
2. Clone your new repo and go to the `src/` folder.
3. Add your Markdown files using the naming convention:
   ```
   index.md
   01-intro.md
   02-topic.md
   03-more.md
   ```
4. Push your changes to the `main` branch.
5. GitHub Actions will automatically:
   - Build your PDF, EPUB, and HTML deliverables
   - Create a dynamic navigation menu based on your content
   - Publish your site to GitHub Pages

---

## ✍️ Writing Your Markdown Files

- Each file **must begin with a YAML metadata block**.
- Required field:

```yaml
navtitle: "Title to Show in Navigation Menu"
```

- Example:

```markdown
---
navtitle: "Structured Authoring"
---

# Structured Authoring

Write your content here using regular Markdown.
```

- File names like `01-intro.md`, `02-chapter.md` define the order in the menu.
- `index.md` is always listed first and becomes the landing page.

---

## 🎨 Customizing the Look and Feel

Modify the following files in the `assets/` folder to style your site:

- `style.css`: Main stylesheet
- `footer.html`: Footer block
- `cover.jpg`: Optional EPUB cover
- `cover.tex`: Optional LaTeX title page for PDF

> The navigation header is generated automatically. Do **not** edit `header.html` manually—it's built during the workflow run using your Markdown titles.

---

## 🔧 Enabling GitHub Pages

1. Go to **Settings → Pages** in your repo
2. Set source to the `gh-pages` branch and root (`/`) folder
3. Visit your site at `https://<your-username>.github.io/<your-repo>/`

---

##   📄 Accessing PDF and EPUB Deliverables

The PDF and EPUB outputs are not deployed directly to GitHub Pages.  
Instead, each workflow run on the **Actions** page provides the PDF and EPUB as a downloadable **artifacts**:

1. Go to the **Actions** tab in your repository.  
2. Select the latest successful workflow run.  
3. Scroll down to the **Artifacts** section.  
4. Click the PDF or EPUB artifact link to download your deliverable.  

---

## 🔐 GitHub Actions Permissions

1. Go to **Settings → Actions → General**
2. Under **Workflow permissions**, check:
   > ✅ "Read and write permissions"
3. Click **Save**

This is required for GitHub Actions to deploy your site.

---

## 📁 Folder Overview

```
.github/workflows/      # GitHub Actions workflow
assets/                 # CSS, footer, LaTeX, optional cover image
src/                    # Markdown files (index.md, 01-intro.md, etc.)
output/                 # Generated site and files
metadata.yaml           # Global metadata (for EPUB, PDF)
README.md               # This file
```

---

## 🙋 Need Help?

This template was created by Carlos Evia with help from your uncle ChatGPT.  
Feel free to fork and adapt it to your own documentation workflows.
