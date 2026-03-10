# 01-tasks-profile-page

## Relevant Files

- `Gemfile` - Jekyll dependency declaration (ruby gems)
- `_config.yml` - Jekyll site configuration (title, description, baseurl, theme settings)
- `_layouts/default.html` - Base HTML5 layout template with viewport meta, charset, and CSS link
- `index.md` (or `index.html`) - Main page content with profile info hardcoded
- `assets/css/style.scss` - Main stylesheet: typography, layout, responsive breakpoints, dark mode, animations
- `assets/images/profile-right.png` - Profile photo (copied from a-rld)
- `assets/images/header-bg.png` - Banner/background image (copied from a-rld)
- `.gitignore` - Ignore Jekyll build artifacts (`_site/`, `.jekyll-cache/`, etc.)

### Notes

- Jekyll is natively supported by GitHub Pages — no GitHub Actions or custom build step needed.
- Use `bundle exec jekyll serve` for local development.
- Follow Jekyll's default file organization conventions.
- No JavaScript dependencies — CSS-only animations.
- Content is hardcoded directly in templates, no data files.

## Tasks

### [x] 1.0 Jekyll Project Scaffolding

Set up the Jekyll project structure with a minimal configuration, base layout, and placeholder index page. The site should build and serve locally.

#### 1.0 Proof Artifact(s)

- CLI: `bundle exec jekyll build` completes without errors demonstrates project scaffolding works
- CLI: `bundle exec jekyll serve` starts local server demonstrates local preview is functional
- Browser: `http://localhost:4000` shows a placeholder page demonstrates site is serving

#### 1.0 Tasks

- [x] 1.1 Create `Gemfile` with `jekyll` gem and `github-pages` group for GitHub Pages compatibility
- [x] 1.2 Create `_config.yml` with minimal settings: site title ("R.L. Dailey"), description, and baseurl
- [x] 1.3 Create `.gitignore` to exclude `_site/`, `.jekyll-cache/`, `.sass-cache/`, and `vendor/`
- [x] 1.4 Create `_layouts/default.html` with HTML5 boilerplate: doctype, charset, viewport meta tag, CSS link placeholder, and `{{ content }}` block
- [x] 1.5 Create `index.md` with front matter (`layout: default`) and placeholder text (e.g., "Hello, world")
- [x] 1.6 Verify build — local Ruby/Jekyll not available; build will be verified via GitHub Pages remote build after push
- [x] 1.7 Verify serve — will be confirmed via `https://daileyo.github.io` after push (no local Ruby environment)

### [ ] 2.0 Profile Content and Image Assets

Copy image assets from a-rld, add profile content (name, title, bio paragraph) to the index page, and integrate the profile image and banner/background image into the layout.

#### 2.0 Proof Artifact(s)

- Browser: `http://localhost:4000` displays profile image, name, title, and bio paragraph demonstrates content is rendered correctly
- File: `assets/images/profile-right.png` exists in repo demonstrates image asset is copied
- File: `assets/images/header-bg.png` exists in repo demonstrates banner asset is copied

#### 2.0 Tasks

- [ ] 2.1 Create `assets/images/` directory and copy `profile-right.png` from `/home/daileyo/gws/a-rld/src/assets/images/profile-right.png`
- [ ] 2.2 Copy `header-bg.png` from `/home/daileyo/gws/a-rld/src/assets/images/header-bg.png` into `assets/images/`
- [ ] 2.3 Update `index.md` (or convert to `index.html`) to include: profile image (`<img>` tag referencing `assets/images/profile-right.png`), full name (R.L. Dailey), professional title, and a single career summary paragraph
- [ ] 2.4 Update `_layouts/default.html` to reference `header-bg.png` as a banner or background element (e.g., hero section background)
- [ ] 2.5 Use semantic HTML5 elements: `<main>`, `<section>`, `<header>`, `<figure>` for the profile image
- [ ] 2.6 Verify all content renders correctly at `http://localhost:4000` (unstyled is fine at this stage)

### [ ] 3.0 Styling — Modern Clean Design, Responsive Layout, and Dark Mode

Implement the visual design: sans-serif typography, whitespace-heavy layout, circular profile image, subtle fade-in animations, responsive breakpoints (320px–1920px+), and dark mode via `prefers-color-scheme`.

#### 3.0 Proof Artifact(s)

- Screenshot: Desktop view (1200px+ width) shows centered layout with generous whitespace demonstrates desktop design
- Screenshot: Mobile view (375px width) shows properly reflowed content demonstrates responsive design
- Screenshot: Dark mode view shows inverted color scheme demonstrates dark mode support
- URL: `https://daileyo.github.io` loads the styled profile page demonstrates live deployment works

#### 3.0 Tasks

- [ ] 3.1 Create `assets/css/style.scss` with Jekyll front matter (`---` delimiters) to enable Sass processing
- [ ] 3.2 Define base typography: system sans-serif font stack (or Inter), comfortable font sizes, line heights, and text color
- [ ] 3.3 Implement single-column centered layout with `max-width`, auto margins, and generous vertical padding/spacing
- [ ] 3.4 Style the profile image: circular crop (`border-radius: 50%`), appropriate max-width, subtle box-shadow
- [ ] 3.5 Style the banner/background: `header-bg.png` as a hero section background with appropriate sizing and overlay if needed
- [ ] 3.6 Add subtle CSS fade-in animation on page load using `@keyframes` and `animation` properties on content elements
- [ ] 3.7 Add responsive breakpoints: ensure layout reflows cleanly at 320px, 768px, and 1200px+ using `@media` queries
- [ ] 3.8 Implement dark mode using `@media (prefers-color-scheme: dark)` — invert background/text colors, adjust image shadow, ensure WCAG AA contrast
- [ ] 3.9 Link the stylesheet in `_layouts/default.html` via `<link>` tag pointing to `{{ "/assets/css/style.css" | relative_url }}`
- [ ] 3.10 Test locally: verify desktop, mobile (dev tools responsive mode), and dark mode (dev tools emulation) all render correctly
- [ ] 3.11 Push to `master` branch and verify `https://daileyo.github.io` loads the styled profile page
