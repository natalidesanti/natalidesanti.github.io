# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this is

Natalí de Santi's personal academic website (`natalidesanti.github.io`), built on the **academicpages** template (a fork of the Minimal Mistakes Jekyll theme). It is a static Jekyll site deployed via GitHub Pages. There is no application backend, build pipeline, or test suite — content lives in Markdown/YAML/JSON and is rendered by Jekyll/Liquid at build time.

## Commands

Local development requires Ruby, Bundler, and Jekyll:

```bash
bundle install                 # install Ruby gems (delete Gemfile.lock first if this errors)
bundle exec jekyll serve       # serve at localhost:4000, rebuilds on file change
bundle exec jekyll liveserve   # live-reloading dev server (via the `hawkins` gem)
```

There is no JS build required for normal edits. The `npm` scripts in `package.json` only re-minify the bundled jQuery/plugins into `assets/js/main.min.js` and are rarely needed:

```bash
npm run build:js   # regenerate assets/js/main.min.js from assets/js/_main.js + plugins
npm run watch:js    # rebuild on change
```

There is no automated test suite or linter in this repo. Validate changes by running the dev server and visually checking the affected page(s).

Two Jekyll configs exist: `_config.yml` (production) and `_config.dev.yml` (local overrides — disables analytics, uses `localhost:4000`, expanded Sass output). When serving locally with both configs, pass them explicitly if you want dev overrides:

```bash
bundle exec jekyll serve --config _config.yml,_config.dev.yml
```

## Site architecture

Standard Jekyll collections-based structure. Each collection is a directory of Markdown files with YAML front matter, rendered through a shared layout:

- `_posts/` — blog posts (collection: `posts`, layout `single`)
- `_publications/` — papers, one file per publication, front matter includes `date`, `venue`, `paperurl`, `citation`, `excerpt` (collection: `publications`, layout `single`)
- `_talks/` — talks/presentations, front matter includes `type`, `venue`, `date`, `location` (collection: `talks`, layout `talk`)
- `_teaching/` — teaching entries (collection: `teaching`, layout `single`)
- `_portfolio/` — portfolio items (collection: `portfolio`, layout `single`)
- `_pages/` — standalone pages (About, CV, Publications index, Talks index, Teaching index, Portfolio index, Talk map, etc.), most using `layout: archive` to list a collection via Liquid loops (see `_pages/portfolio.html`, `_pages/talks.html`) or `layout: single` for free-form content (`_pages/about.md`, `_pages/cv.md`)
- `_data/` — site-wide structured data:
  - `navigation.yml` — top nav bar entries
  - `authors.yml` — author/sidebar profile info
  - `ui-text.yml` — localizable UI strings (English defaults under `en:`)
  - `cv.json` — JSON Resume–format CV data (currently template placeholder data, not wired into `_pages/cv.md`, which is hand-written Markdown instead)
  - `comments/` — stored static comments (staticman provider)
- `_includes/` — Liquid partials for layout pieces (head, footer, masthead, author-profile, comments, analytics, social-share, etc.), with provider-specific subfolders (`_includes/analytics-providers/`, `_includes/comments-providers/`) selected based on `_config.yml` settings
- `_layouts/` — top-level page templates (`default`, `single`, `archive`, `talk`, `splash`, `home`, `archive-taxonomy`, `compress`)
- `_sass/` — Sass partials; `_sass/theme/_default.scss` and `_sass/theme/_dark.scss` hold theme/color variants, `_sass/vendor/` bundles third-party Sass (breakpoint, font-awesome, magnific-popup, susy)
- `assets/` — compiled CSS output target, JS (vendor + `_main.js` + `main.min.js`), fonts
- `images/`, `files/` — static media and downloadable files (PDFs, etc.); anything in `files/` is served at `/files/...`

## Content authoring conventions

- New posts, publications, talks, teaching entries, and portfolio items are added by dropping a new Markdown file into the corresponding `_posts/`, `_publications/`, `_talks/`, `_teaching/`, `_portfolio/` directory with the same front-matter shape as existing files in that directory (see examples already in each folder for exact required fields per collection).
- Front matter `collection:` must match the collection name; `permalink:` is often left blank to use the collection's default `/:collection/:path/` pattern set in `_config.yml`.
- Filenames for posts/talks/publications are date-prefixed (`YYYY-MM-DD-slug.md`), which Jekyll uses for chronological sorting/permalinks.
- `markdown_generator/` contains standalone Jupyter notebooks + equivalent `.py` scripts (`pubsFromBib.py`, `talks.py`) that bulk-generate `_publications/` or `_talks/` Markdown files from a BibTeX file or TSV (`talks.tsv`/`publications.tsv`). These are optional bulk-import tools, not part of the site build.
- `talkmap.ipynb` / `talkmap.py` regenerate `talkmap/map.html`, a Leaflet map built from `location:` fields in `_talks/*.md`; the map is embedded via `_pages/talkmap.html`.
- Nav bar entries are edited in `_data/navigation.yml`, not hardcoded in layouts.
- Site metadata (title, description, author bio, social links, analytics provider) lives in `_config.yml` under `author:`, `social:`, `analytics:` — this is the single source of truth for sidebar/profile info actually used by the theme (`_data/cv.json` is unused template boilerplate; don't assume it drives the rendered CV page).
- Comments, if enabled, are configured under `comments:` in `_config.yml` (provider is currently unset/disabled); provider-specific templates are in `_includes/comments-providers/`.

## Notes for making changes

- This is a visual, content-driven site — after editing Sass, layouts, or includes, run the Jekyll dev server and check the rendered page rather than relying on inspection alone.
- Sass compiles in `compressed` style in production (`_config.yml`) and `expanded` in dev (`_config.dev.yml`); use the dev config locally to get readable CSS output for debugging.
- `_config.yml` is not auto-reloaded by `jekyll serve` — restart the server after editing it.
