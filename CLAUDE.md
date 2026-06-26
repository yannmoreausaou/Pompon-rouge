# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Shopify theme project called "Pompon-rouge". Based on Shopify skeleton-theme, it includes all standard theme files ready to be customized and imported into a Shopify store.

## Common Commands

```bash
shopify theme dev        # Start local development server
shopify theme push       # Push theme to Shopify store
shopify theme pull       # Pull theme from Shopify store
shopify theme check      # Validate theme code
```

## Architecture

```
├── assets/              # CSS (critical.css), SVG icons
├── blocks/              # Theme blocks (group.liquid, text.liquid)
├── config/              # settings_data.json, settings_schema.json
├── layout/              # theme.liquid, password.liquid
├── locales/             # Translation files (en.default.json)
├── sections/            # Theme sections (header, footer, product, collection, etc.)
├── snippets/             # Liquid snippets (css-variables, image, meta-tags)
├── templates/            # Page templates (product, collection, cart, blog, etc.)
└── blocks/              # Block definitions for the theme editor
```

### Key Files
- [config/settings_data.json](config/settings_data.json) — Theme settings/configuration
- [layout/theme.liquid](layout/theme.liquid) — Main theme layout
- [sections/header.liquid](sections/header.liquid) — Header section
- [sections/footer.liquid](sections/footer.liquid) — Footer section
- [sections/product.liquid](sections/product.liquid) — Product page section

## Workflow

1. Develop locally: `shopify theme dev`
2. Validate: `shopify theme check`
3. Push to Shopify: `shopify theme push`
4. Commit and push to GitHub for backup/tracking
