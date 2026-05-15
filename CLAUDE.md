# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Jekyll static site hosted on GitHub Pages at `bac-ds.github.io`. Personal data science blog and portfolio for Dr. Ben Coombs. **No theme gem** — fully custom layouts and CSS (no Sass, no build step).

## Commands

```bash
bundle install                # first-time setup
bundle exec jekyll serve      # local dev → http://localhost:4000 (live reload)
bundle exec jekyll build      # production build → _site/
```

If port 4000 is busy: `lsof -ti :4000 | xargs kill -9`

## Architecture

### Layout Chain

All layouts extend `base.html` (HTML shell: head, sticky nav, footer). The chain is:

| Layout | Used by |
|--------|---------|
| `home.html` | `index.markdown` — hero, about strip, post/project teasers |
| `page.html` | `blog.md`, `portfolio.md`, `cv.md`, `about.markdown` — dot-grid header + content |
| `post.html` | `_posts/` — blog post with date, categories, back-link |
| `project.html` | `_projects/` — portfolio card with type badge, links, back-link |

`_config.yml` applies `layout: post` and `layout: project` automatically via defaults — source files don't need to declare it.

### CSS (`assets/css/main.css`)

All styling lives in one file. Design tokens at the top control everything:

```css
:root {
  --c-accent: #2563EB;   /* primary blue */
  --c-teal:   #0D9488;   /* secondary teal (notebook/marimo badges) */
  --font-sans: 'Inter', ...;
  --font-mono: 'JetBrains Mono', ...;
}
```

### Navigation

`_data/navigation.yml` — add or reorder nav links here. Active link is highlighted automatically via `page.url`.

### Blog Posts (`_posts/`)

Filename: `YYYY-MM-DD-slug.markdown`. Minimum front matter:

```yaml
---
title: "Post Title"
date: YYYY-MM-DD HH:MM:SS +0000
categories: blog general
---
```

Images go in `assets/images/posts/` and are referenced as `/assets/images/posts/filename.png`.

### Portfolio Projects (`_projects/`)

One `.md` file per project. Only `title` is required; other front matter fields are optional:

```yaml
---
title: "Project Name"
description: "One-liner for the card."
type: notebook          # notebook | marimo | dashboard | repo  (controls badge colour)
tech: [Python, Plotly]  # list → shown as tags on project page
status: in-progress
github: https://github.com/...
notebook: https://...
demo: https://...
---
```

Projects appear in the portfolio grid and as teasers on the landing page (3 most recent).

### CV Page

Timeline is powered by **TimelineJS3** (KnightLab, CDN). Career data lives in `assets/timeline.json` — follow the [TimelineJS JSON spec](https://timeline.knightlab.com/docs/json-format.html): each event needs `start_date.year`, `text.headline`, `text.text`.

Skills are hardcoded as `<span class="tag ...">` elements in `cv.md`. Downloadable PDF is at `assets/CV_DrBenCoombs.pdf`.

### Hero Banner

Background image referenced in the `.hero` rule in `main.css`. Banners live in `assets/images/banners/` (target ~1400×500px, JPG preferred).

## Deployment & Branch Strategy

- `dev` — active development
- `main` — GitHub Pages auto-builds on push; no CI config needed

`_site/` is git-ignored. The `rafts/` directory is an archived snapshot — do not modify it.

## Gemfile Note

`gem "minima"` and `gem "jekyll-theme-yat"` are listed in the Gemfile but unused — the site uses fully custom layouts. These can be removed when convenient.
