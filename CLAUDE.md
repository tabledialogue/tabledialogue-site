# CLAUDE.md

Guidance for Claude Code when working in this repository.

## Project

Marketing/content site for **Table** — a monthly in-person gathering in NYC for founders, operators, advisors, and investors.

Live URL: https://tabledialogue.github.io/tabledialogue-site

## Stack

- **Jekyll** static site (Ruby)
- **Theme:** [`mmistakes/minimal-mistakes`](https://github.com/mmistakes/minimal-mistakes) v4.24.0 via `jekyll-remote-theme`
- **Hosting:** GitHub Pages (built from `main` by GitHub's `github-pages` gem)
- **Plugins:** `jekyll-feed`, `jekyll-sitemap`, `jekyll-seo-tag`, `jekyll-include-cache`, `jekyll-remote-theme`

Because the site builds on GitHub Pages, only the plugins/versions whitelisted by the `github-pages` gem are available. Don't add Jekyll plugins that GitHub Pages doesn't support.

## Repository layout

```
_config.yml          # Jekyll site config (title, theme, plugins, defaults)
_data/navigation.yml # Top nav links
_includes/head/      # Theme overrides injected into <head>
_layouts/home.html   # Custom homepage layout (hero, gallery, values, quotes, CTA)
assets/css/main.scss # Site styles (compiled by Jekyll-Sass)
assets/images/       # Logo, favicons, hero/gallery photos
index.md             # Homepage content + front-matter (uses layout: home)
about.md             # /about/ page (origin story, team, values)
docs/                # Source material (PDFs, etc.) — excluded from build
```

The custom `home` layout reads structured front-matter from `index.md` (`hero_*`, `photos`, `values`, `testimonials`, `closing_cta`). Edit page content in front-matter for structured sections; use the Markdown body for "The idea" prose.

## Local development

```bash
bundle install                    # first time, installs gems into vendor/bundle if configured
bundle exec jekyll serve          # http://127.0.0.1:4000/tabledialogue-site/
bundle exec jekyll serve --livereload
bundle exec jekyll build          # one-shot build into _site/
```

`Gemfile.lock` is gitignored (GitHub Pages controls versions).

## Conventions

- **Don't change `baseurl`** in `_config.yml` (`/tabledialogue-site`) — it matches the GitHub Pages project path. Use `{{ '/path' | relative_url }}` in templates and `[text](/path)` in Markdown won't auto-prefix; prefer `relative_url` filters in Liquid.
- **Page titles** in front-matter should not repeat the site name — `jekyll-seo-tag` appends it automatically.
- **Images** go in `assets/images/`; reference with leading slash and `relative_url` in Liquid.
- **Theme overrides** belong in `_includes/`, `_layouts/`, or `assets/css/main.scss` — don't vendor the whole theme.
- **Markdown content** should be plain prose; structured/visual sections (hero, gallery, quote band) are driven by front-matter consumed by `_layouts/home.html`.

## Branching

- Default branch: `main` (deploys to GitHub Pages).
- Feature work happens on `claude/*` branches; open a PR into `main`.
- Don't push directly to `main` — always go through a PR.

## Things to watch for

- After editing `_config.yml`, restart `jekyll serve` (it isn't watched).
- Custom layout/CSS class names use a `td-` prefix (Table Dialogue) — keep that prefix when extending styles.
- The homepage IntersectionObserver script in `_layouts/home.html` adds `is-in` to `[data-reveal]` elements; respect `prefers-reduced-motion`.
- `docs/` contains source PDFs and is excluded from the build via `_config.yml`. Don't link to files in `docs/` from rendered pages.
