# tabledialogue-site

Source for **[Table](https://tabledialogue.github.io/tabledialogue-site)** — candid conversations for founders, operators, and investors. Monthly, in NYC.

Built with [Jekyll](https://jekyllrb.com/) and the [Minimal Mistakes](https://github.com/mmistakes/minimal-mistakes) theme. Hosted on GitHub Pages.

## Local development

Requires Ruby (3.x recommended) and Bundler.

```bash
bundle install
bundle exec jekyll serve --livereload
```

Then open http://localhost:4000/tabledialogue-site/.

To build without serving:

```bash
bundle exec jekyll build
```

The output goes to `_site/` (gitignored).

## Editing content

- **Homepage:** `index.md` — most of the visible content lives in front-matter (`hero_*`, `photos`, `values`, `testimonials`, `closing_cta`). The custom layout that renders it is `_layouts/home.html`.
- **About page:** `about.md`.
- **Navigation:** `_data/navigation.yml`.
- **Site metadata / theme settings:** `_config.yml`.
- **Styles:** `assets/css/main.scss`.
- **Images:** `assets/images/`.

## Deployment

Pushing to `main` triggers a GitHub Pages build automatically. There is no separate CI/CD step.

## Working with Claude Code

This repo includes a [`CLAUDE.md`](./CLAUDE.md) with project conventions, layout, and gotchas for [Claude Code](https://claude.com/claude-code) sessions. If you change the stack or conventions, update it.
