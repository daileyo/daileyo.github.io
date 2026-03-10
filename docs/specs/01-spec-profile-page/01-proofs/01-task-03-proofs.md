# Task 3.0 Proof Artifacts — Styling, Responsive Layout, and Dark Mode

## Stylesheet Summary

Full stylesheet at `assets/css/style.scss` (SCSS processed by Jekyll).

### Typography
- Font stack: `-apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif`
- Base font size: 16px
- Name heading: 2rem (700 weight, -0.02em letter-spacing)
- Title: 1.125rem (400 weight, muted color)
- Bio: 1.0625rem (1.75 line-height)
- Antialiased rendering on macOS/iOS

### Layout
- Single centered column, `max-width: 640px`
- Hero banner: full-width, `background-size: cover` with `header-bg.png`
- Semi-transparent overlay on hero (light: white 55%, dark: black 55%)
- Profile card overlaps hero by 80px (negative margin)
- Bio text max-width: 520px for comfortable reading

### Profile Image
- 160px circular crop (`border-radius: 50%`, `object-fit: cover`)
- 4px solid border matching background color
- Box shadow: `0 4px 20px rgba(0,0,0,0.08)`

### Animations
- `fadeInUp` keyframes: opacity 0→1, translateY 16px→0
- Staggered delays: card (0s), image (0.1s), name (0.2s), title (0.3s), bio (0.4s)
- Duration: 0.6s ease-out

### Responsive Breakpoints

| Breakpoint | Hero Height | Image Size | Name Size | Notes |
|-----------|-------------|------------|-----------|-------|
| ≤480px    | 160px       | 120px      | 1.5rem    | Reduced padding/spacing |
| 481–767px | 220px       | 160px      | 2rem      | Default styles |
| 768–1199px| 260px       | 160px      | 2rem      | Taller hero |
| ≥1200px   | 300px       | 160px      | 2rem      | Tallest hero |

### Dark Mode (`prefers-color-scheme: dark`)

| Element | Light | Dark |
|---------|-------|------|
| Background | `#ffffff` | `#111118` |
| Text | `#1a1a2e` | `#e8e8ed` |
| Muted text | `#555770` | `#9a9ab0` |
| Image border | `#ffffff` | `#111118` |
| Footer border | `#e0e0e6` | `#2a2a3a` |
| Hero overlay | `rgba(255,255,255,0.55)` | `rgba(0,0,0,0.55)` |

All color pairs meet WCAG AA contrast requirements.

## Verification

- [ ] Desktop (1200px+): Centered layout, generous whitespace, full hero banner
- [ ] Mobile (375px): Reflowed content, smaller hero/image, readable text
- [ ] Dark mode: Inverted colors, comfortable contrast, adjusted shadows
- [ ] Animations: Staggered fade-in on page load
- [ ] Live URL: `https://daileyo.github.io` after push

**Note:** Local Jekyll not available. Testing deferred to post-push verification at `https://daileyo.github.io`.
