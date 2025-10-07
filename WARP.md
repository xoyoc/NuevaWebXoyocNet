# WARP.md

This file provides guidance to WARP (warp.dev) when working with code in this repository.

## Project Overview

This is a static website project for Xoyoc.Net, a professional web development portfolio and business site. The site showcases web development services, projects, and contact information for Antonio Xoyoc, a web developer specializing in React and Python development based in Lázaro Cárdenas, Michoacán, Mexico.

## Architecture

**Single Page Application Structure:**
- `index.html` - Complete single-page website with embedded CSS and JavaScript
- `CNAME` - GitHub Pages domain configuration for xoyoc.net
- Static hosting via GitHub Pages

**Technology Stack:**
- Vanilla HTML5, CSS3, and JavaScript
- Font Awesome icons for visual elements
- Responsive design with CSS Grid and Flexbox
- CSS Custom Properties (CSS Variables) for theming
- Intersection Observer API for scroll animations

**Design System:**
- Color scheme defined in CSS custom properties (`:root`)
- Primary colors: `--primary: #6366f1`, `--secondary: #8b5cf6`, `--accent: #ec4899`
- Dark theme with `--dark: #0f172a` background
- Responsive breakpoint at 768px for mobile devices

## Common Commands

### Development
```bash
# Serve locally for development (requires Python)
python3 -m http.server 8000

# Alternative with Node.js (if installed)
npx serve .

# Open in browser
open http://localhost:8000
```

### Version Control
```bash
# Check current status
git status

# Stage and commit changes
git add .
git commit -m "Update: description of changes"

# Push to GitHub Pages
git push origin main

# View recent commits
git log --oneline -10
```

### Deployment
The site is automatically deployed to GitHub Pages when changes are pushed to the main branch. The live site is available at https://xoyoc.net

### Validation & Testing
```bash
# Validate HTML (if html5validator is installed)
html5validator index.html

# Check for broken links (if linkchecker is installed)  
linkchecker http://localhost:8000

# Lighthouse audit (requires Chrome/Chromium)
lighthouse http://localhost:8000 --output html --output-path lighthouse-report.html
```

## Code Organization

**HTML Structure:**
- Navigation with smooth scroll links
- Hero section with tech stack badges and GitHub stats
- Services grid (6 service cards)
- Projects showcase (4 featured projects)
- Contact section with social links
- Footer

**CSS Architecture:**
- Mobile-first responsive design
- CSS Grid for layout systems (services-grid, projects-grid)
- CSS custom properties for consistent theming
- Keyframe animations for entrance effects
- Hover effects with transforms and box shadows

**JavaScript Features:**
- Navbar scroll effects with class toggling
- Mobile menu toggle functionality
- Smooth scrolling for anchor links
- Intersection Observer for scroll-triggered animations

## Key Features

**Responsive Design:**
- Mobile menu with slide-out navigation
- Flexible grid layouts that stack on mobile
- Scalable typography using `clamp()`
- Touch-friendly button and link sizing

**Performance Optimizations:**
- Single file architecture reduces HTTP requests
- Efficient CSS with minimal specificity conflicts
- Intersection Observer for performance-conscious animations
- External Font Awesome loaded from CDN

**Professional Portfolio Elements:**
- GitHub integration with repository links
- Project showcase with live site links
- Contact information and social media links
- Professional service descriptions

## External Dependencies

- **Font Awesome 6.4.0** - Icons and visual elements
- **GitHub Pages** - Static site hosting
- **Custom Domain** - xoyoc.net configured via CNAME

## Project Context

This site represents Antonio Xoyoc's professional web development business, featuring:
- 20+ completed projects
- 30+ years of experience  
- Specialization in React and Python
- Enterprise platform development (AAALAC, SIGA Loginco)
- Full-stack development capabilities

The site serves as both a portfolio and business landing page for client acquisition in the Lázaro Cárdenas, Michoacán region and beyond.