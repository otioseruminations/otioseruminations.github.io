# Otiose Ruminations

Source repository for **Otiose Ruminations**, a personal essay site hosted at:

https://otioseruminations.github.io

The site is built with **Quarto** and deployed through **GitHub Pages** using **GitHub Actions**.

## Purpose

Otiose Ruminations is a home for slow, serious essays.
The main recurring interests are likely to be mathematics and history, but the site is deliberately not restricted to a fixed list of topics.

Subjects may change over time.

## Site structure

```text
.
├── _quarto.yml                  # Main Quarto website configuration
├── index.qmd                    # Home page
├── essays.qmd                   # Essay listing page
├── about.qmd                    # About page
├── styles.css                   # Custom styling
├── posts/                       # Individual essays
│   └── first-essay/
│       └── index.qmd
└── .github/
    └── workflows/
        └── publish.yml          # GitHub Actions deployment workflow
```

## Adding a new essay

Create a new folder inside `posts/`.

Example:

```text
posts/euler-and-logarithmic-integrals/index.qmd
```

Use this template:

```markdown
---
title: "Essay Title"
date: 2026-06-03
description: "Short description of the essay."
categories: [mathematics, history]
---

Write the essay here.

Display mathematics works like this:

$$
\int_0^1 \log^2(1-x)\log^2(1+x)\,dx
$$
```

After committing the new essay to the `main` branch, GitHub Actions automatically rebuilds and redeploys the site.

## Deployment

The site is deployed using the workflow:

```text
.github/workflows/publish.yml
```

The workflow renders the Quarto project and publishes the generated site to GitHub Pages.

The public site is available at:

https://otioseruminations.github.io

## Notes

This is a public website. Do not commit private drafts, proprietary material, API keys, credentials, unpublished data, or sensitive personal information.

## License

Unless otherwise stated, the writing on this site is © 2026 Otiose Ruminations. All rights reserved.
