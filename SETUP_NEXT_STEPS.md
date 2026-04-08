# Your al-folio site — next steps

The al-folio theme has been cloned into this folder and lightly personalized.
Here's what's done and what you need to do to get it live.

## What I've customized

- `_config.yml` — name, description, footer, favicon, keywords
- `_pages/about.md` — homepage bio rewritten for a dual PhD/industry pitch
- `_news/announcement_{1,2,3}.md` — starter news items dated 2026
- Upstream git history detached (this is now a clean tree you'll init yourself)

## What you need to do

### 1. Fill in your info
Replace placeholders (anything in `[brackets]` or `YOUR-USERNAME`) in:
- `_config.yml` — especially `url:` (your GitHub username), `first_name`, `last_name`, socials section (further down the file)
- `_pages/about.md` — bio, university, interests
- `_news/announcement_*.md` — your actual news
- `assets/img/prof_pic.jpg` — replace with your photo (same filename)
- `assets/pdf/cv.pdf` — drop your CV here
- `_bibliography/papers.bib` — replace Einstein examples with your papers (keep the format)

### 2. Run it locally (Docker, easiest)
```bash
cd PersonalWebsite-alfolio
docker compose pull && docker compose up
# Visit http://localhost:8080
```

Or with Ruby directly:
```bash
bundle install
bundle exec jekyll serve
# Visit http://localhost:4000
```

### 3. Put it on GitHub
```bash
git init
git add .
git commit -m "Initial site from al-folio"
# Create a repo named YOUR-USERNAME.github.io on GitHub, then:
git remote add origin https://github.com/YOUR-USERNAME/YOUR-USERNAME.github.io.git
git branch -M main
git push -u origin main
```

### 4. Enable GitHub Pages
In the repo: **Settings → Pages → Source: GitHub Actions**. al-folio ships with a
workflow in `.github/workflows/` that builds and deploys automatically on push.
Your site will be live at `https://YOUR-USERNAME.github.io` within a few minutes.

### 5. Custom domain (optional)
If you own e.g. `yourname.com`, add a `CNAME` file with your domain and configure
DNS per GitHub's docs. Then update `url:` in `_config.yml`.

## Pages to customize next

Look in `_pages/` — there's a file per top-nav page:
- `publications.md` — auto-generated from `_bibliography/papers.bib`
- `projects.md` — showcases items from `_projects/`
- `cv.md` — either link your PDF or use the YAML-driven CV in `_data/cv.yml`
- `blog.md` — auto-generated from `_posts/`
- `teaching.md`, `repositories.md`, etc. — delete or disable pages you don't need

To hide a page from the nav, add `nav: false` in its front matter.

## Docs that ship with al-folio
- `QUICKSTART.md` — 5-minute overview
- `INSTALL.md` — full install/deploy
- `CUSTOMIZE.md` — theming, colors, fonts
- `FAQ.md`, `TROUBLESHOOTING.md` — common issues
