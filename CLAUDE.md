# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a personal blog and portfolio site built with [Hugo](https://gohugo.io/), a static site generator. The site is hosted on GitHub Pages and automatically deployed via GitHub Actions whenever changes are pushed to the `master` branch.

**Site URL**: https://jason.motylinski.com
**Theme**: Anatole (minimalist two-column theme)

## Common Commands

### Local Development
```bash
hugo server
```
Starts a local development server at `http://localhost:1313/`. Hugo automatically rebuilds and hot-reloads as you make changes.

### Build for Production
```bash
hugo --gc --minify
```
Generates optimized static files to the `public/` directory. The `--gc` flag cleans up unused resources, and `--minify` compresses output.

### Create New Post
Posts go in `content/posts/`. File naming convention: `YYYYMMDD-slug.md` (e.g., `20231212-hello.md`).

Posts use front matter with at least:
```yaml
---
title: 'Post Title'
date: 2023-12-12T20:17:06-05:00
draft: false
tags: ['tag1', 'tag2']
---
```

## Project Architecture

### Directory Structure

- **`content/`**: Site content
  - `posts/`: Blog posts, one file per post with `YYYYMMDD-slug.md` naming
  - `projects/`: Project pages and portfolio items
- **`themes/anatole/`**: The Anatole theme (git submodule). Generally avoid modifying this; use layouts overrides instead
- **`layouts/`**: Hugo template overrides for the site
  - `shortcodes/`: Custom Hugo shortcodes
    - `postlist.html`: Lists posts with a specific tag
    - `directorylist.html`: Creates a list of files in a directory
- **`static/`**: Static assets served as-is
  - `images/`: Site images including profile picture (`me-work.png`)
  - `projects/`: Project-related static files
  - `Jason Motylinski Resume.pdf`: Resume file linked from social icons
- **`assets/`**: Hugo asset files (for Sass, etc.)
- **`.github/workflows/hugo.yaml`**: GitHub Actions workflow for automated deployment
- **`hugo.toml`**: Main Hugo configuration file

### Key Configuration

**`hugo.toml`** contains:
- Base URL and site title
- Theme selection (set to 'anatole')
- Parameters for site customization (author, description, profile picture, social links)
- Google Analytics ID: `G-N18DLRD200`
- Mermaid diagram support enabled
- Goldmark markdown renderer with unsafe HTML allowed
- Related posts feature (3 related posts shown)
- Light mode disabled (light display only)

**Social Icons** (in hugo.toml): LinkedIn, GitHub, Email, and Resume PDF link

### Content Organization

Posts are automatically organized by:
- **Tags**: Posts can have multiple tags; tag pages are auto-generated
- **Publication date**: Posts are sorted by date
- **Archives page**: Auto-generated from publish dates

The theme supports:
- Full post content in listing pages (`fullPostContent = true`)
- Related posts feature showing 3 most relevant posts
- Content ratio of 0.8 for narrower column layout

## Deployment

GitHub Actions workflow (`.github/workflows/hugo.yaml`) handles deployment:
- Triggers on pushes to `master` branch or hourly via cron schedule (`0 * * * *`)
- Installs Hugo 0.121.0 and Dart Sass
- Optionally runs `npm install` if npm lockfiles exist
- Builds with Hugo and deploys to GitHub Pages

The workflow uses `HUGO_ENVIRONMENT: production` and `HUGO_ENV: production` for production builds.

## Theme Documentation

The Anatole theme has comprehensive documentation in its GitHub wiki:
https://github.com/lxndrblz/anatole/wiki

Theme supports optional features including:
- Dark mode (disabled in current config with `disableThemeSwitcher = true`)
- Comments (Disqus, Commento, Gitalk, Utterances, Giscus)
- Post series
- Post thumbnails
- Formspree contact forms
- KaTeX math support
- Mermaid diagrams (enabled in config)
