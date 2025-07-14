# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is YinYang, a minimalist Hugo theme for blogs. It's a static site generator theme focused on simplicity and readability with black-white design aesthetics.

## Development Commands

Since this is a Hugo theme, development typically involves:

- Test the theme: `hugo server` (from a Hugo site using this theme)
- Build a site: `hugo` (from a Hugo site using this theme)
- View example site: `cd exampleSite && hugo server`

The theme doesn't have its own build system - it's consumed by Hugo sites that use it.

## Architecture

### Layout Structure
- `layouts/index.html` - Homepage template with post listings grouped by year
- `layouts/_default/single.html` - Individual post template
- `layouts/_default/list.html` - Category/tag listing template  
- `layouts/partials/` - Reusable components:
  - `head.html` - HTML head with meta tags, CSS, and SEO
  - `header.html` - Site header with title and navigation
  - `footer.html` - Site footer
  - `seo.html` - JSON-LD structured data for SEO
  - `disqus.html` - Disqus comments integration
  - `related.html` - Related posts section
  - `scripts.html` - JavaScript includes

### Styling
- `assets/css/index.css` - Main theme styles
- `assets/css/flexboxgrid-6.3.1.min.css` - CSS grid system
- Inline CSS processing through Hugo's resource pipeline
- Uses "Bree Serif" font from Google Fonts
- Responsive design with flexbox grid

### Key Features
- Multi-language support (English/Chinese by default)
- SEO optimization with OpenGraph and JSON-LD
- Disqus comments integration
- Twitter Cards support
- Responsive design
- Clean, minimalist black-white aesthetic
- Post categorization and tagging
- Related posts functionality

### Configuration
Theme configuration is handled through Hugo's `config.toml`:
- `params.headTitle` - Custom header title
- `params.mainSections` - Content sections to display
- `params.disqus` - Disqus shortname
- `params.socials` - Social media links
- `params.extraHead` - Additional head content
- `params.extraCSSFiles` - Extra CSS files
- `params.postHeaderContent/postFooterContent` - Post wrapper content

### Content Organization
- Posts should be in directories matching `params.mainSections`
- Multi-language content goes in `content/en/` and `content/cn/`
- Front matter supports: title, date, categories, tags, images (for Twitter Cards)

## Common Tasks

When modifying this theme:
1. Test changes using the `exampleSite/` directory
2. Ensure responsive design works across screen sizes
3. Verify multi-language functionality if applicable
4. Test SEO meta tags and structured data
5. Check that partials are properly included and functional