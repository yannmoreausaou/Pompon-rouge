# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Shopify theme project called "Pompon-rouge" (Shopify theme creation).

## Common Commands

### Development
```bash
shopify theme dev        # Start local development server
shopify theme push        # Push theme to Shopify store
shopify theme pull        # Pull theme from Shopify store
shopify theme check       # Run Shopify theme linter
```

### Testing
```bash
shopify theme check       # Validate theme code
```

## Architecture

Shopify themes follow a specific directory structure:

- `layout/` — Theme layouts (base.liquid, etc.)
- `templates/` — Page templates (product, collection, page, etc.)
- `sections/` — Reusable section blocks
- `snippets/` — Reusable Liquid snippet files
- `assets/` — CSS, JavaScript, images
- `locales/` — Translation files (en.default.json, fr.json, etc.)
- `config/` — Theme settings schema

### Key Files
- `config/settings_data.json` — Theme settings/configuration
- `layout/theme.liquid` — Main theme layout
- `templates/product.liquid` — Product page template
- `templates/collection.liquid` — Collection page template
