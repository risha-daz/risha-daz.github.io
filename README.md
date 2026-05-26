# Personal Site

Built with [Quarto](https://quarto.org). Deployed to GitHub Pages via GitHub Actions.

## Local development

```bash
# Install Quarto: https://quarto.org/docs/get-started/
quarto preview   # live-reloading dev server at localhost:4444
```

## Deploy

Push to `main` — the GitHub Actions workflow renders the site and deploys it automatically.

## Adding a blog post

Create a new `.md` file in `blog/`:

```
blog/my-new-post.md
```

Include this frontmatter at the top:

```yaml
---
title: "Post Title"
date: "YYYY-MM-DD"
description: "One sentence shown in the blog listing."
categories: [tag1, tag2]
---
```

Then write in plain Markdown. The blog listing page updates automatically on next render.

## Structure

```
├── _quarto.yml          # site config and nav
├── index.qmd            # homepage
├── experience.qmd       # resume
├── projects.qmd         # project showcase
├── blog/
│   ├── index.qmd        # auto-generated listing
│   └── *.md             # posts in plain markdown
├── assets/              # images, resume PDF, favicon
├── styles.css           # custom CSS overrides
└── .github/workflows/
    └── deploy.yml       # CI/CD → GitHub Pages
```

## GitHub Pages setup (one-time)

1. Go to repo **Settings → Pages**
2. Set **Source** to **GitHub Actions**
3. Push to `main` — the workflow handles the rest
