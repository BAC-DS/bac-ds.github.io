# BAC To The Data — bac-ds.github.io

Personal data science blog and portfolio for Dr. Ben Coombs. Built with Jekyll, hosted on GitHub Pages.

## Local Development

```bash
bundle install                # first time only
bundle exec jekyll serve      # → http://localhost:4000 (live reload)
bundle exec jekyll build      # production build → _site/
```

If port 4000 is busy: `lsof -ti :4000 | xargs kill -9`

## Site Structure

| Page | URL | Source |
|------|-----|--------|
| Landing | `/` | `index.markdown` + `_layouts/home.html` |
| Blog | `/blog/` | `blog.md` |
| Portfolio | `/portfolio/` | `portfolio.md` + `_projects/*.md` |
| CV | `/cv/` | `cv.md` + `assets/timeline.json` |
| About | `/about/` | `about.markdown` |

**Adding a blog post:** create `_posts/YYYY-MM-DD-slug.markdown` — layout is applied automatically.

**Adding a portfolio project:** create `_projects/my-project.md` with front matter fields `title`, `description`, `type` (`notebook`/`marimo`/`dashboard`/`repo`), `github`, `notebook`, `demo`. Appears in the grid and homepage teaser automatically.

**Updating the CV timeline:** edit `assets/timeline.json` — one JSON object per career event.

**Changing colours/fonts:** edit CSS tokens at the top of `assets/css/main.css`.

**Swapping the hero banner:** update the image URL in the `.hero` rule in `main.css`. New banners go in `assets/images/banners/` (target ~1400px wide × 500px tall, JPG preferred).

## Branch Strategy

- `dev` — active development
- `main` — production; GitHub Pages auto-builds on push

---

## TODO

### In Progress / Near Term
- [ ] Update `_projects/example-project.md` description to match the real Lego analysis write-up
- [ ] Replace placeholder images in `assets/timeline.json` with real ones (career timeline on CV page)
- [ ] Update skills section in `cv.md` to reflect current stack accurately
- [ ] Update `about.markdown` content for the new site design

### Content
- [ ] Write up remaining Data Governance drafts (Pt 3 & 4 are in `_drafts/`)
- [ ] Add real portfolio projects as `.md` files in `_projects/`
- [ ] Flesh out portfolio project pages with write-up content (not just front matter)

### Design & Features
- [ ] Source/commission additional hero banner images for variety (`assets/images/banners/`)
- [ ] Add hero banner auto-rotation (vanilla JS cycling through banner images on an interval)
- [ ] Add Google Analytics back in — snippet goes in `_layouts/base.html` before `</body>`
- [ ] Consider adding post reading-time estimate to `_layouts/post.html`
- [ ] Consider a simple tag/category filter on the Blog page
- [ ] Consider pagination on the Blog page once post count grows (Jekyll `jekyll-paginate` plugin)

### CV
- [ ] Replace `placehold.co` media images in `timeline.json` with real images or company logos
- [ ] Explore embedding a Tableau or Plotly chart on the CV page as a skills showcase

### Infrastructure
- [ ] Set up a proper GitHub Actions workflow for deploying `dev` previews
- [ ] Add a `_redirects` or `404.html` strategy for old Minima-era URLs if needed
- [ ] Review and update `Gemfile` — remove unused `jekyll-theme-yat` gem
