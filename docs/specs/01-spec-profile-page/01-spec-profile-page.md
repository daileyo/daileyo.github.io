# 01-spec-profile-page

## Introduction/Overview

The current `daileyo.github.io` repository is an empty GitHub Pages site with no content. The goal is to create a succinct, modern profile page that serves as a personal landing page for R.L. Dailey. The page will feature a brief bio, profile image, professional title, and a paragraph summarizing career accomplishments — nothing more. It replaces the outdated Angular 8 portfolio app (a-rld) with something deliberately minimal and easy to maintain.

## Goals

- Create a clean, single-page profile site hosted on GitHub Pages
- Use a lightweight static site generator for structure and maintainability
- Present a professional bio, title, and profile image in a modern, whitespace-heavy design
- Support responsive layout (mobile and desktop) and dark mode (system preference)
- Keep content hardcoded for simplicity — no external data sources or build-time integrations

## User Stories

- **As a visitor**, I want to quickly learn who R.L. Dailey is and what they do so that I can understand their professional background at a glance.
- **As the site owner**, I want a minimal, easy-to-maintain profile page so that I can keep it up to date without dealing with complex build pipelines or frameworks.
- **As a mobile user**, I want the page to look good on my phone so that I can view it anywhere.
- **As a user who prefers dark mode**, I want the page to respect my system preference so that it's comfortable to read.

## Demoable Units of Work

### Unit 1: Static Site Generator Setup and Base Layout

**Purpose:** Establish the project scaffolding with a static site generator (e.g., Jekyll, Hugo, or Eleventy) so that GitHub Pages can serve the site, and provide a base HTML layout with responsive meta tags.

**Functional Requirements:**
- The project shall use Jekyll as the static site generator (native GitHub Pages support)
- The project shall include a base layout template with proper HTML5 structure, viewport meta tag, and charset declaration
- The site shall build successfully and produce a valid `index.html`
- The project shall include a local development server for previewing changes

**Proof Artifacts:**
- CLI: Build command completes without errors demonstrates project scaffolding works
- Browser: Local dev server shows a blank or placeholder page at `localhost` demonstrates local preview is functional

### Unit 2: Profile Content and Styling

**Purpose:** Add the actual profile content (name, title, profile image, career summary paragraph) and implement the modern clean visual design with responsive layout and dark mode support.

**Functional Requirements:**
- The page shall display a profile image (`profile-right.png` from a-rld), full name, and professional title
- The page shall use `header-bg.png` from a-rld as a banner or background element
- The page shall display a single paragraph summarizing professional career and accomplishments
- The page shall use a modern clean design: sans-serif typography, generous whitespace, subtle animations (e.g., fade-in on load)
- The page shall be responsive, rendering well on screens from 320px to 1920px+ wide
- The page shall support dark mode via CSS `prefers-color-scheme` media query, automatically matching the user's system preference
- All content shall be hardcoded directly in the HTML/template — no external data files

**Proof Artifacts:**
- Screenshot: Desktop view of profile page demonstrates layout and content rendering
- Screenshot: Mobile view (narrow viewport) demonstrates responsive design
- Screenshot: Dark mode view demonstrates dark mode support
- URL: `https://daileyo.github.io` loads the profile page demonstrates live deployment works

## Non-Goals (Out of Scope)

1. **Projects section**: No project showcase or portfolio listings on this page
2. **Contact form or email links**: No contact section or interactive elements
3. **PostgreSQL integration**: The pg-rld schema will not be used as a data source
4. **Multi-page site**: This is a single page only — no navigation, no sub-pages
5. **JavaScript interactivity**: No client-side JS beyond what the static site generator requires (if any); subtle CSS animations only

## Design Considerations

- **Typography**: Sans-serif font (system font stack or a clean web font like Inter)
- **Layout**: Single centered column, generous vertical spacing between elements
- **Color**: Light background with dark text by default; inverted for dark mode with comfortable contrast ratios (WCAG AA minimum)
- **Animations**: Subtle fade-in on page load for content elements (CSS only)
- **Profile image**: Circular crop, appropriately sized, with subtle shadow or border
- **Overall feel**: Professional, minimal, "less is more" — the page should feel intentionally sparse

## Repository Standards

No existing patterns or conventions exist in this repository (it's a clean slate). The following standards should be established:

- Use the static site generator's default file organization conventions
- Keep the project structure minimal — avoid unnecessary configuration or tooling
- Use semantic HTML5 elements
- Follow the MIT License already present in the repository

## Technical Considerations

- **Static site generator**: Jekyll (native GitHub Pages support, no GitHub Actions needed)
- **No JavaScript dependencies**: Avoid npm/node dependencies if possible; CSS-only animations preferred
- **Profile image**: Copy `profile-right.png` from `a-rld/src/assets/images/` into this repo's assets
- **Banner/background image**: Copy `header-bg.png` from `a-rld/src/assets/images/` into this repo's assets for use as a page banner or background element
- **Build simplicity**: The build process should be as simple as possible — ideally zero-config or near-zero-config with Jekyll's defaults

## Security Considerations

- Do not include personal contact information (phone number, personal email) in the public repository
- No API keys, tokens, or credentials are involved in this project
- Profile image should not contain sensitive EXIF metadata

## Success Metrics

1. **Page loads successfully** at `https://daileyo.github.io` with all content visible
2. **Responsive**: Page renders correctly at mobile (320px), tablet (768px), and desktop (1200px+) widths
3. **Dark mode**: Page automatically switches to dark theme when system preference is set to dark
4. **Performance**: Page loads in under 2 seconds on a standard connection (minimal assets, no JS bundles)
5. **Maintainability**: Content can be updated by editing a single file

## Open Questions

No open questions at this time. All decisions have been resolved:
- Static site generator: Jekyll
- Profile image: `profile-right.png` from a-rld
- Banner/background: `header-bg.png` from a-rld
- Social links: None for now
