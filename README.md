# Stuart Street Apps — Website

Marketing website for Stuart Street Apps. Currently features our first iOS app, *Learn About Your United States*, with a scalable structure for adding future apps.

## Structure

This is a two-page static site:

- **Home** — Hero, features, screenshots, about strip, and an "Our Apps" grid
- **Support** — Per-app support FAQs, contact, and privacy policy

Page navigation is handled with a small inline JavaScript switcher (no framework required).

## Setup

No build process required.

### Local Development

1. Clone the repository
2. Open `index.html` in your browser, or use a local server:

```bash
# Python 3
python -m http.server 8000

# Node.js
npx serve
```

## Adding a New App

When you launch a new app, update three places in `index.html`:

### 1. Our Apps grid (Home page)
Duplicate the `<!-- App card -->` block and update the icon, name, description, platform badge, and App Store link. Remove the `app-card-placeholder` block when you have two or more real apps.

### 2. Support tabs (Support page)
Add a new `<button class="app-tab">` to `.app-selector` with `onclick="showAppSupport('app2', this)"`.
Add a matching `<div id="support-app2" class="support-content">` block with that app's FAQs.

### 3. Privacy policy (Support page)
Add a new `.privacy-block` inside `.privacy-section` with the app label and policy text.

## Required Assets

The site expects the following in the `images/` directory:

| File | Used for |
|---|---|
| `favicon.png` | Site favicon and app card icon |
| `apple-touch-icon.png` | iOS home screen icon |
| `iphone-home.png` | Hero + screenshots: app home screen |
| `iphone-map.png` | Hero + screenshots: interactive map |
| `iphone-capitalQuiz.png` | Hero: quiz screen |
| `iphone-quizLength.png` | Screenshots: quiz length selection |
| `iphone-medals.png` | Screenshots: medals screen |
| `social-preview.png` | Open Graph preview (1200×630px recommended) |

## App Store

[Download on the App Store](https://apps.apple.com/us/app/learn-about-your-united-states/id6752962821)

## Technologies

- Semantic HTML5
- Modern CSS with custom properties
- Google Fonts (Lora, Nunito, DM Sans)
- Minimal vanilla JavaScript (page switcher only)
- No build tools, no dependencies

## Features

- Two-page layout with JS-driven navigation (no page reloads)
- Fully responsive — mobile nav hides text links, stacks grids
- Smooth animations with `prefers-reduced-motion` support
- Accessible keyboard navigation and focus states
- SEO and Open Graph meta tags
- Performance optimised (lazy loading, font preconnect)

## License

© 2025 Stuart Street Apps. All rights reserved.
