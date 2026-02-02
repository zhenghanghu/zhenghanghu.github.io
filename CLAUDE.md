# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a personal website built with Jekyll using the TeXt theme. It's deployed to GitHub Pages at zhenghanghu.github.io.

## Common Commands

```bash
# Local development (serves at http://localhost:4000)
npm run serve
# Or without npm:
bundle exec jekyll serve -H 0.0.0.0

# Production build (outputs to _site/)
npm run build
# Or without npm:
JEKYLL_ENV=production bundle exec jekyll build

# Lint JavaScript
npm run eslint-fix

# Lint SCSS
npm run stylelint-fix
```

**Prerequisites:** Ruby 3.0+, Bundler (`gem install bundler`), then `bundle install`.

## Architecture

### Content
- `_posts/` - Blog posts (Markdown with YAML front matter)
- `about.md` - About page
- `_config.yml` - Site configuration (title, author, plugins, comments via Valine)

### Theme Structure
- `_layouts/` - Page templates (base, home, article, archive)
- `_includes/` - Reusable components and JavaScript modules
- `_sass/` - SCSS stylesheets
- `_data/` - YAML data files (navigation, authors, locale strings)
- `assets/` - Static files (CSS, images, PDFs)

### Documentation
- `docs/` - Theme documentation (not deployed with the main site)

## Commit Message Format

Commits must follow Conventional Commits format (enforced by Husky + Commitlint):
- `feat:` new feature
- `fix:` bug fix
- `docs:` documentation
- `style:` formatting
- `refactor:` code restructuring
- `test:` tests
- `chore:` maintenance

## Writing Posts

Posts go in `_posts/` with filename format `YYYY-MM-DD-title.md`. Required front matter:

```yaml
---
title: Post Title
tags: [tag1, tag2]
---
```

Optional front matter: `key`, `excerpt_separator`, `mathjax`, `mermaid`, `chart`, `sharing`, `license`, `aside.toc`.
