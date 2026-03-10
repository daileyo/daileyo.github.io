# Task 2.0 Proof Artifacts — Profile Content and Image Assets

## Image Assets

```
assets/images/profile-right.png  - 10,490 bytes (profile photo placeholder)
assets/images/header-bg.png      - 31,681 bytes (banner/background placeholder)
```

Both copied from `/home/daileyo/gws/a-rld/src/assets/images/`.

Note: Both images are geometric placeholders from the old a-rld app. The user should replace these with actual profile/banner images.

## Content Structure (index.html)

```html
<header class="hero" role="banner">        <!-- Banner section using header-bg.png via CSS -->
  <div class="hero-overlay"></div>
</header>

<main class="profile">
  <section class="profile-card">
    <figure class="profile-image">
      <img src="profile-right.png" alt="R.L. Dailey" width="160" height="160">
    </figure>
    <h1>R.L. Dailey</h1>
    <p class="profile-title">Software Engineer</p>
    <p class="profile-bio">Career summary paragraph...</p>
  </section>
</main>

<footer class="site-footer">              <!-- In default.html layout -->
  <p>&copy; 2026 R.L. Dailey</p>
</footer>
```

## Semantic HTML5 Elements Used

- `<header>` — Hero/banner section
- `<main>` — Primary content area
- `<section>` — Profile card grouping
- `<figure>` / `<img>` — Profile image
- `<footer>` — Copyright footer

## Verification

- Profile content includes: name, title, bio paragraph, profile image
- Banner image referenced via hero section (CSS background applied in Task 3.0)
- All content hardcoded directly in templates — no data files
- Placeholder bio text included; user should update with real career summary
