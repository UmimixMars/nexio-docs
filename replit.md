# Nexio Discord Bot Website

## Overview

Nexio is a static multi-page website for a Discord bot, designed for deployment on GitHub Pages. The site provides comprehensive documentation for bot features, commands, premium tiers, and support resources. Built with pure HTML, Tailwind CSS (via CDN), and vanilla JavaScript, it requires no server-side processing and is optimized for static hosting environments.

The website serves as the primary online presence for Nexio, a Discord bot built in Python that offers moderation, leveling, fun commands, and utility features. The site facilitates user onboarding, command discovery, premium subscriptions, and support access.

## Recent Changes

**November 13, 2025** - Complete website implementation
- Created all 6 HTML pages (index.html, commands.html, premium.html, support.html, legal.html, 404.html)
- Implemented downtown purple theme with Tailwind CSS via CDN
- Added responsive mobile navigation with hamburger menu
- Implemented collapsible accordion sections for commands and FAQ
- Created 4-tier premium comparison table with all 17 features
- Set up Jekyll configuration for GitHub Pages (_config.yml)
- Added comprehensive deployment instructions in README.md
- Configured .gitignore for repository
- Verified all pages render correctly with proper JavaScript functionality
- Site is deployment-ready for GitHub Pages

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture

**Static Site Generation**
- Pure HTML/CSS/JavaScript implementation with no build process
- No frontend framework or library dependencies
- All pages are standalone HTML files that can be served directly
- Tailwind CSS loaded via CDN (https://cdn.tailwindcss.com) for zero-configuration styling
- Custom Tailwind configuration embedded in each page via inline script tags

**Design System**
- Consistent "Downtown Purple" theme across all pages
- Custom color palette defined in Tailwind config:
  - `midnight` (#0F0A1A) - primary background
  - `card` (#1A1429) - card backgrounds
  - `accent` (#C77DFF) - primary accent color
  - `accent-hover` (#9D4EDD) - hover states
- Inter font family loaded from Google Fonts for modern typography
- Mobile-first responsive design with breakpoint-based layouts

**Component Architecture**
- Shared navigation component duplicated across all pages (sticky header with mobile menu)
- Reusable card-based layout pattern for content sections
- Accordion components for collapsible command sections
- Mobile hamburger menu with JavaScript toggle functionality

**Page Structure**
- 6 total pages: index.html, commands.html, premium.html, support.html, legal.html, 404.html
- Each page is self-contained with embedded styles and scripts
- Consistent header/footer navigation across all pages
- Custom 404.html for GitHub Pages error handling

### Routing and Navigation

**Client-Side Routing**
- Standard HTML anchor-based navigation between pages
- No client-side router or SPA framework
- GitHub Pages serves static files directly with Apache/nginx-style routing
- Custom 404.html catches invalid routes and provides navigation back to site

**Mobile Menu Implementation**
- JavaScript event listeners toggle mobile menu visibility
- Click-outside detection to close menu when user clicks elsewhere
- Responsive breakpoint at `md` (768px) switches between desktop nav and mobile menu

### Deployment Architecture

**GitHub Pages Hosting**
- Designed for deployment from `gh-pages` branch
- All files under 100MB individual limit, total repo under 1GB limit
- HTTPS enabled by default with custom domain support
- No server-side processing or dynamic content generation
- Public repository required for free GitHub Pages hosting

**Static Asset Delivery**
- All CSS/JS loaded from CDNs (Tailwind, Google Fonts)
- No local asset bundling or optimization pipeline
- Images and icons use inline SVG for zero additional HTTP requests
- No image optimization or lazy loading implemented

### Styling Approach

**Utility-First CSS**
- Tailwind CSS utility classes for all styling
- No custom CSS files or preprocessors
- Theme configuration injected via `tailwind.config` script block
- Consistent spacing, typography, and color usage via utility classes

**Responsive Design**
- Mobile-first breakpoints (sm, md, lg, xl)
- Hidden/visible classes toggle mobile vs desktop navigation
- Flexbox and grid utilities for responsive layouts
- No media query CSS files - all responsive behavior via Tailwind utilities

### Interactive Features

**JavaScript Functionality**
- Vanilla JavaScript only (no jQuery or libraries)
- Mobile menu toggle with DOM manipulation
- Accordion expand/collapse for command sections
- Click-outside detection for menu closing
- All scripts embedded inline in HTML files

**Progressive Enhancement**
- Core content accessible without JavaScript
- Interactive features enhance but don't block base functionality
- Links work with JavaScript disabled (standard anchor navigation)

## External Dependencies

### Third-Party Services

**Discord Integration**
- Discord OAuth2 bot invite URL for adding bot to servers
- Discord server invite link for community support
- No direct API integration - website is informational only

**Ko-fi Payment Platform**
- Three premium tier subscription links hosted on Ko-fi
- Monthly recurring subscriptions handled entirely through Ko-fi
- No payment processing or webhook integration in website
- Users redirected to Ko-fi for checkout flow

**Support Server**
- Discord server link (https://discord.gg/vMWuDvk4dZ) for:
  - Lifetime premium key purchases
  - Direct support and troubleshooting
  - Community engagement
- No embedded Discord widget or API integration

### CDN Dependencies

**Tailwind CSS**
- Loaded from official Tailwind CDN (cdn.tailwindcss.com)
- JIT (Just-In-Time) compilation in browser
- No build step or PostCSS processing
- Custom theme config via inline script

**Google Fonts**
- Inter font family loaded from Google Fonts CDN
- Preconnect links for performance optimization
- Font weights: 400, 600, 700, 800

### Hosting Platform

**GitHub Pages**
- Static file hosting from `gh-pages` branch
- Automatic HTTPS with `github.io` subdomain
- Custom domain support via CNAME configuration
- No database, server-side processing, or API endpoints
- File serving only - no compute layer

### Content Management

**No CMS or Database**
- All content hardcoded in HTML files
- Updates require direct HTML file editing
- No dynamic content or data fetching
- Command lists, pricing, and documentation maintained manually in source files

### Analytics and Monitoring

**No Analytics Implemented**
- No Google Analytics, Plausible, or similar tracking
- No error monitoring or logging services
- No user behavior tracking or metrics collection
- Could be added via script tags if needed in future