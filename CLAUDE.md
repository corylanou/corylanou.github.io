# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with
code in this repository.

## Repository Overview

This is a GitHub Pages Jekyll-based personal portfolio website for Cory LaNou,
an expert Go developer and trainer. The site uses the Cayman theme and consists
primarily of a single-page portfolio showcasing professional experience,
publications, and community contributions.

## Development Commands

### Local Development

```bash
# Install dependencies (first time setup)
bundle install --path vendor/bundle

# Serve the site locally with auto-reload
bundle exec jekyll serve

# Build the site without serving
bundle exec jekyll build

# View the site in browser
open http://127.0.0.1:4000

# Find Jekyll process
ps aux | grep jekyll

# Kill the Jekyll server
kill $(pgrep -f "jekyll serve")
```

### Linting

```bash
# Run markdownlint on markdown files
markdownlint index.md
```

## Project Structure

- `index.md` - Main content file containing portfolio information
- `_config.yml` - Jekyll configuration (uses Cayman remote theme)
- `images/` - Static image assets
- `stylesheets/` - CSS files for styling
- `_site/` - Generated site output (not tracked in git)

## Key Configuration

The site uses the Cayman theme via Jekyll remote themes plugin. The
configuration is minimal and straightforward in `_config.yml`.

## Deployment

This site is automatically deployed via GitHub Pages when changes are pushed to
the master branch. No manual deployment steps are required.

## Important Notes

- This is a static Jekyll site - changes to content should primarily be made
  in `index.md`
- The site uses GitHub Pages' Jekyll environment, so only GitHub
  Pages-compatible plugins can be used
- Always run markdownlint before committing markdown changes (per global
  CLAUDE.md instructions)
