# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a static website for "The Easy Company" built with vanilla HTML, CSS, and hosted on GitHub Pages (domain: easycompany.vn). The site showcases company apps, primarily PackEasy - a packing assistant application.

## Repository Structure

```
/
├── index.html              # Company homepage
├── style.css              # Global styles for homepage
├── CNAME                  # Custom domain configuration
└── apps/
    ├── index.html         # Apps listing page
    ├── style.css          # Apps page styles
    └── packeasy/
        ├── index.html     # PackEasy app landing page
        ├── style.css      # PackEasy-specific styles
        ├── logo.png       # App logo
        ├── favicon.png    # App favicon
        ├── policy/        # Privacy policy page
        ├── support/       # Support page
        └── terms/         # Terms of use page
```

## Development Commands

This is a static HTML/CSS site with no build process or package managers. Development is done by:

1. **Local Development**: Open HTML files directly in browser or use a simple HTTP server
2. **Testing**: Manual testing in browser - no automated test suite
3. **Deployment**: Push to main branch, GitHub Pages automatically serves the site

## Architecture and Design Patterns

### CSS Architecture
- **Global Reset**: All pages start with margin/padding reset and box-sizing: border-box
- **Consistent Typography**: Uses system font stack (-apple-system, BlinkMacSystemFont, etc.)
- **Dark Theme**: Consistent dark color scheme (#0d1117 background, white text)
- **Component-Based Styling**: Reusable classes like .nav-btn, .btn-primary, .btn-outline
- **Responsive Design**: Uses clamp() for fluid typography and flexbox for layouts

### Page Structure Pattern
All pages follow consistent structure:
- Header with logo and navigation
- Main content area with flex: 1 for full height
- Footer with copyright information

### Navigation System
- Bidirectional navigation between home → apps → individual app pages
- SVG icons for visual consistency
- Primary/secondary button styling for hierarchy

### Color Scheme
- Background: #0d1117 (dark)
- Text: white primary, #a1a1aa secondary
- Borders: #1a1a1a, #2a2a2a
- Primary actions: #2563eb (blue)
- Secondary backgrounds: #1f2937, #111

### File Organization
- Each app has its own subdirectory with dedicated styles
- Policy pages are nested within app directories
- Images and favicons stored alongside their respective pages

## Content Management

The site is content-focused with no CMS. Updates require direct HTML editing:
- Company information in root index.html
- App descriptions in apps/index.html  
- Individual app pages in respective subdirectories
- Legal pages (policy, terms, support) as separate HTML files

## Domain and Hosting

- Custom domain: easycompany.vn (configured via CNAME file)
- Hosted on GitHub Pages
- SSL automatically provided by GitHub Pages