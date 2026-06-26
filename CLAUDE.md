# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

**Pompon-rouge** is a Shopify theme for a luxury toiletries brand. The theme features a maritime/sailor aesthetic with a red pompom design element.

## Brand Guidelines

### Colors
- **Navy** `#0F2D3D` — titles, menu, footer, secondary buttons
- **Red** `#C62828` — primary buttons, accents, important links
- **Off-white** `#F8F6F2` — main background
- **Sand** `#E8DDC8` — section backgrounds, cards
- **Slate gray** `#5B6770` — body text, descriptions

### Typography
- **Headings** — Cinzel
- **Body** — Montserrat (regular 400, semibold 600)
- **Buttons** — Montserrat Semibold, uppercase, letter-spacing 0.1em

### Buttons
- **Primary**: Red background (#C62828), white text
- **Secondary**: Transparent background, navy border (#0F2D3D)

## Common Commands

```bash
shopify theme dev        # Start local development server
shopify theme push       # Push theme to Shopify store
shopify theme pull       # Pull theme from Shopify store
shopify theme check      # Validate theme code
```

## Architecture

```
├── assets/              # CSS (critical.css)
├── blocks/              # Theme blocks (group.liquid, text.liquid)
├── config/              # settings_data.json, settings_schema.json
├── layout/              # theme.liquid, password.liquid
├── locales/             # Translation files (en.default.json, fr.json)
├── sections/            # Theme sections
│   ├── header.liquid    # Sticky navy header with block system
│   ├── footer.liquid    # Navy footer with newsletter
│   ├── hero.liquid      # Homepage hero section
│   ├── featured-product.liquid
│   ├── about-section.liquid
│   └── features-section.liquid
├── snippets/            # Liquid snippets (css-variables, image, meta-tags)
└── templates/          # Page templates
```

### Key Files
- [config/settings_schema.json](config/settings_schema.json) — Theme settings (colors, fonts)
- [snippets/css-variables.liquid](snippets/css-variables.liquid) — CSS custom properties
- [assets/critical.css](assets/critical.css) — Global styles, buttons, typography
- [sections/header.liquid](sections/header.liquid) — Header with blocks: logo, menu, icons
- [sections/footer.liquid](sections/footer.liquid) — Footer with blocks: brand, links, newsletter, payment

## Block System

All sections use Shopify's block system for user customization:
- Each section has defined block types in its schema
- Users can add/remove/reorder blocks via Shopify theme editor
- Blocks are defined with `{%- when 'block_type' -%}` and rendered with `{{ block.shopify_attributes }}`

## Workflow

1. Develop locally: `shopify theme dev`
2. Validate: `shopify theme check`
3. Push to Shopify: `shopify theme push`
4. **After every modification, commit and push to GitHub:**
   ```bash
   git add -A && git commit -m "Description of changes" && GIT_SSH_COMMAND="ssh -i ~/.ssh/pompon_rouge_key" git push origin main
   ```
