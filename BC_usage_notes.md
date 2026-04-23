# Usage notes

## Project Overview

Jekyll static site hosted on GitHub Pages at `bac-ds.github.io`. Personal data science blog and portfolio for Dr. Ben Coombs. **No theme gem** — fully custom layouts and CSS.

## Common Commands

```bash
bundle install                # install Ruby dependencies
bundle exec jekyll serve      # local dev server with live reload → http://localhost:4000
bundle exec jekyll build      # production build → _site/
```

If port 4000 is already in use: `lsof -ti :4000 | xargs kill -9`

## Architecture

### Layouts (in `_layouts/`)

| Layout | Used by | Purpose |
|--------|---------|---------|
| `base.html` | all others (via `layout:` front matter) | HTML shell: head, sticky nav, footer |
| `home.html` | `index.markdown` | Landing page: hero, about strip, post/project teasers |
| `page.html` | `blog.md`, `portfolio.md`, `cv.md`, `about.markdown` | Dot-grid header + content wrapper |
| `post.html` | `_posts/` | Blog post with date, categories, back-link |
| `project.html` | `_projects/` | Portfolio project with type badge, links, back-link |

The layout chain is: `home/page/post/project` → `base` → rendered HTML. Layout defaults are set in `_config.yml` so post and project files don't need to declare `layout:` manually.

### CSS (`assets/css/main.css`)

All styling lives here. Design tokens are CSS custom properties at the top of the file — change colours, spacing, and fonts by editing these variables:

```css
:root {
  --c-accent:  #2563EB;   /* primary blue */
  --c-teal:    #0D9488;   /* secondary teal (notebook/marimo badges) */
  --font-sans: 'Inter', ...;
  --font-mono: 'JetBrains Mono', ...;
}
```

No Sass, no build step — edit and reload.

### Navigation (`_data/navigation.yml`)

Add or reorder nav links here. Active link is highlighted automatically based on `page.url`.

### Blog Posts (`_posts/`)

Filename format: `YYYY-MM-DD-slug.markdown`. Front matter:

```yaml
---
title: "Post Title"
date: YYYY-MM-DD HH:MM:SS +0000
categories: blog general
---
```

`layout: post` is applied automatically via `_config.yml` defaults. Images go in `assets/images/posts/` and are referenced as `/assets/images/posts/filename.png`.

### Portfolio Projects (`_projects/`)

Add a `.md` file per project. All front matter fields are optional except `title`:

```yaml
---
title: "Project Name"
description: "One-liner for the card."
type: notebook          # notebook | marimo | dashboard | repo  (controls badge colour)
tech: [Python, Plotly]  # list → shown as tags on the project page
status: in-progress     # shown as a badge
github: https://github.com/...
notebook: https://...   # Jupyter / Marimo link
demo: https://...       # Plotly / Tableau / Quarto live link
---

Write-up content in Markdown here.
```

`layout: project` is applied automatically. The project appears in the portfolio grid and as a card teaser on the landing page (limited to 3 most recent).

### CV Page (`cv.md`)

The interactive timeline is powered by **TimelineJS3** (KnightLab, loaded via CDN). Career data lives in `assets/timeline.json` — edit that file to update the timeline. Format is the [TimelineJS JSON spec](https://timeline.knightlab.com/docs/json-format.html): each event needs `start_date.year`, `text.headline`, and `text.text`.

Skills are hardcoded in `cv.md` under the `<div class="skills-grid">` block — edit the `<span class="tag ...">` elements directly.

The downloadable PDF is at `assets/CV_DrBenCoombs.pdf`.

### Hero Banner

The landing page hero uses `assets/images/banners/Blog_Banner.png` as a background image, with a dark gradient overlay for text contrast. To swap the banner, update the `background-image` URL in the `.hero` rule in `main.css`. `New_Banner.png` is also available in the same directory.

## Deployment

GitHub Pages auto-builds from the `main` branch on push — no CI config needed. `_site/` is git-ignored. The `rafts/` directory is an archived snapshot; do not modify it.

Active development happens on the `dev` branch; merge to `main` to publish.
