# 01 Questions Round 1 - Profile Page

Please answer each question below (select one or more options, or add your own notes). Feel free to add additional context under any question.

## 1. Tech Stack

What technology approach do you want for the new profile page?

- [ ] (A) Plain HTML/CSS/JS — no build step, simplest to maintain, served directly by GitHub Pages
- [X] (B) A lightweight static site generator (e.g., Hugo, Eleventy, Jekyll) — more structure, GitHub Pages compatible
- [ ] (C) A modern JS framework (e.g., React, Vue, Svelte) with a static build step
- [ ] (D) Other (describe)

## 2. Content Sections

Which sections from the old site should carry over? (Select all that apply)

- [ ] (A) Hero/landing with name and greeting
- [X] (B) About/bio with profile image and title
- [ ] (C) Projects showcase with skills and tools
- [ ] (D) Contact info (email, links)
- [ ] (E) Links to GitHub, LinkedIn, or other social profiles
- [X] (F) Other (describe) just a single paragraph summary of professional career and accomplishments

## 3. Design Style

What visual style are you going for with "very succinct"?

- [ ] (A) Minimal single-column — text-focused, almost like a styled resume/CV
- [ ] (B) Card-based — compact cards for each section
- [ ] (C) Terminal/developer aesthetic — monospace, dark theme, command-line feel
- [X] (D) Modern clean — whitespace-heavy, sans-serif, subtle animations
- [ ] (E) Other (describe)

## 4. Content Source

Where will the profile content (name, bio, projects, skills) come from?

- [X] (A) Hardcoded directly in the HTML — simplest, edit the file to update
- [ ] (B) Loaded from a JSON/YAML data file — separates content from presentation
- [ ] (C) Pulled from the PostgreSQL schema (pg-rld) at build time — reuses existing data model
- [ ] (D) Other (describe)

## 5. Responsiveness & Dark Mode

What display requirements matter to you?

- [ ] (A) Must be responsive (looks good on mobile and desktop)
- [ ] (B) Dark mode support (either always dark, or toggle, or respects system preference)
- [X] (C) Both responsive and dark mode
- [ ] (D) Desktop-only is fine, no dark mode needed

## 6. Projects Detail

How should projects be presented on this succinct page?

- [ ] (A) Just project names as a simple list
- [ ] (B) Project names with a one-line description
- [ ] (C) Project cards with description, skills/tools used, and links
- [X] (D) No projects section — keep it strictly to bio and contact
- [ ] (E) Other (describe)

## 7. Proof of Success

How will you verify the page is working correctly?

- [ ] (A) Visually inspect at `https://daileyo.github.io` after deploying to GitHub Pages
- [ ] (B) Local preview is sufficient (open index.html in browser)
- [X] (C) Both local preview and live deployment verification
- [ ] (D) Other (describe)
