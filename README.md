# DARTH EDP Documentation

This repository contains the standalone **EDP documentation site**, built using **MkDocs** and deployed to **GitHub Pages**.

This site is completely independent from the main DARTH documentation.

**Live site:**  
https://unsw-ceem.github.io/EDP-docs/

---

# Editing & Deploying Using GitHub Codespaces

Everything can be done directly from GitHub. No local installation required.

---

## 1️⃣ Open the Repository in Codespaces

1. Go to the GitHub repository.
2. Click:

   Code → Codespaces → Create codespace on main

GitHub will:
- Launch a cloud development environment
- Clone the repository
- Open VS Code in your browser

---

## 2️⃣ Install MkDocs (First Time Only)

Open the terminal inside Codespaces and run:

```bash
pip install mkdocs mkdocs-material
```

If additional plugins are added in the future, install them here as well.

---

## 3️⃣ Edit Documentation Content

All documentation files live inside:

```
docs/
```

- `docs/index.md` → Home page  
- Additional `.md` files → Additional pages  

Edit any Markdown file and save.

---

## 4️⃣ Preview the Site (Inside Codespaces)

Run:

```bash
mkdocs serve
```

You will see:

```
Serving on http://127.0.0.1:8000/
```

Then:

1. Open the **Ports** tab in Codespaces.
2. Find port `8000`.
3. Click **Open in Browser**.

The preview auto-refreshes when you save files.

---

## 5️⃣ Commit Your Changes

Once satisfied with edits:

```bash
git add .
git commit -m "Update EDP documentation"
git push
```

This updates the source files on GitHub.

---

## 6️⃣ Deploy to GitHub Pages

To publish the updated site:

```bash
mkdocs gh-deploy
```

This:
- Builds the static site
- Pushes it to the `gh-pages` branch
- Updates the live website

---

# Important Rules

- Do not manually edit the `gh-pages` branch.
- Do not commit the generated `site/` folder.
- Always run `mkdocs gh-deploy` after content updates to publish changes.

---

# Project Structure

```
EDP-docs/
  docs/
    index.md
    ...
  mkdocs.yml
  README.md
```

---

# Summary Workflow

Edit → Preview → Commit → Deploy

```bash
mkdocs serve
git add .
git commit -m "message"
git push
mkdocs gh-deploy
```