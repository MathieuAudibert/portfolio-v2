# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is a personal portfolio website (v3) built with **Zensical**, a static site generator built on Python. The site showcases:
- School career & projects
- Work experience
- Personal projects
- Tools & skills
- Contact information

Live at: https://mathieuaudibert.vercel.app/

## Quick Commands

### Setup
```bash
# Install dependencies
uv install
```

### Development
```bash
# Build the site (generates HTML in ./site/)
uv run zensical build

# Serve locally with live reload
uv run zensical serve
# Then visit http://localhost:8000
```

### Content
```bash
# Edit markdown files in ./docs/ directory
# Navigation structure is defined in zensical.toml under [project] nav
```

## Architecture

### Tech Stack
- **Generator**: Zensical (Python-based static site generator)
- **Package Manager**: uv (Python project manager)
- **Hosting**: Vercel (deployed from this repo)
- **Content**: Markdown files with YAML frontmatter

### Project Structure
```
docs/                 # Content source (Markdown)
├── index.md         # Introduction/homepage
├── school.md        # School projects & studies
├── pro.md           # Professional work experience
├── outside.md       # Personal projects
├── tools.md         # Skills & tools cloud
├── contact.md       # Contact links
├── upcomming.md     # Future content (thesis)
└── images/          # Image assets for docs

site/                 # Generated static site (do not edit)
├── index.html
├── school/
├── pro/
├── outside/
├── tools/
├── contact/
└── assets/          # CSS, JS, images

zensical.toml         # Site configuration (theme, nav, metadata)
pyproject.toml        # Python project metadata
AGENTS.md             # (deprecated quickstart—superseded by this file)
```

### Content Workflow
1. Edit markdown files in `docs/`
2. Add/update navigation in `zensical.toml` under `[project] nav` (arrays of links)
3. Run `uv run zensical build` to regenerate the static site
4. The `site/` directory is generated and deployed to Vercel

### Theme & Customization
- **Logo**: `project.theme.logo` in zensical.toml points to `docs/images/logo-b.png`
- **Favicon**: `project.theme.favicon` points to `docs/images/logo-w.png`
- **Fonts**: Configured in `[project.theme.font]`
  - Text: Lora
  - Code: Jetbrains Mono
- **Color schemes**: Dark/light mode toggle configured in `[[project.theme.palette]]`
- **Icons**: Lucide + FontAwesome used throughout (configured in `[project.theme.icon]`)

### Markdown Features (Zensical)
- Code annotations (with `<!-- (1) -->` markers)
- Copy-to-clipboard for code blocks
- Footnote tooltips
- Content tabs with language switching
- Instant navigation (XHR-based page transitions)
- Breadcrumb navigation
- Search with highlighting

### Metadata & SEO
Configured in zensical.toml:
- `site_name`: "Mathieu A."
- `site_description`: "Mathieu AUDIBERT's portfolio"
- `site_author`: "@MathieuAudibert"
- Social links in `[[project.extra.social]]`

## Key Files to Know

| File | Purpose |
|------|---------|
| `zensical.toml` | Central config for theme, nav, metadata, features |
| `docs/*.md` | Content pages (edit these) |
| `docs/images/` | Images referenced in markdown |
| `site/` | Generated output (regenerated on build) |
| `.venv/` | Virtual environment (created by `uv install`) |

## Common Tasks

### Add a new page
1. Create a new `.md` file in `docs/`
2. Add it to the `nav` array in `zensical.toml`
3. Run `uv run zensical build`
4. Verify in `site/` or locally with `uv run zensical serve`

### Update content
1. Edit the relevant markdown file in `docs/`
2. Run `uv run zensical build` to regenerate
3. Check the output in `site/`

### Change theme/colors/fonts
Edit the `[project.theme]` section in `zensical.toml` (e.g., `font.text`, `font.code`, `palette`).

### Add an image
1. Place image in `docs/images/`
2. Reference in markdown as `![alt text](images/my-image.png)`

## Git & Deployment

- **Current branch**: release/v3 (checked on 2026-07-22)
- **Deployment**: Auto-deploys to Vercel on push to main
- **Status**: Site generated in `site/` directory; do not manually edit HTML there

## Notes

- The `site/` directory is **generated**—all edits should be to `docs/` and `zensical.toml`
- Zensical auto-handles all HTML generation, styling, and layout
- Python 3.14+ required (per pyproject.toml)
- uv is the package manager; use `uv run` to execute Python scripts
