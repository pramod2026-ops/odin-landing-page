# Odin Landing Page

This project is a landing page created as part of The Odin Project foundations course.

## About The Project

The website is built using only HTML and CSS.
It includes:
- Navigation bar
- Hero section
- Information cards
- Testimonial section
- Call-to-action section
- Footer

The goal of this project was to practice:
- CSS Flexbox
- Page layout structure
- Spacing and alignment

## Technologies Used

- HTML5
- CSS3
- Google Fonts (Roboto)

## What I Learned

While building this project, I practiced:
- Creating layouts using Flexbox
- Structuring webpages with HTML
- Styling buttons, sections, and navigation bars
- Working with images

## Reflection

After finishing the first version, I reviewed the code and found several things
to improve:

**HTML**
- The hero section was nested inside `<header>` by mistake. I moved it out so
  `<header>` only contains the navbar, and `<section class="hero-section">`
  sits as its own sibling element.
- The four info cards each had a unique class (`first-info`, `second-info`,
  etc.) even though they were styled identically. I merged them into a single
  `.info-card` class to keep the CSS DRY.
- Image `alt` text said `"coming soon.."` on every info image, which isn't a
  real description. I replaced each one with text describing what the image
  actually shows.
- The testimonial had no attribution. I added a name/title using
  `<figcaption>` inside a `<figure>` so the quote reads as a real testimonial.
- Fixed a broken link (`href="signup"`) that would have 404'd.

**CSS**
- Fixed `align-content: center` on `.info`, which does nothing without
  `flex-wrap` — it should have been `align-items: center`.
- Removed a duplicate semicolon and an ineffective `justify-content` rule
  that had no visible effect.
- Pulled repeated colors into CSS variables (`:root`) instead of repeating
  hex codes throughout the file.
- Added `:hover` and `:focus-visible` states to links/buttons, since the
  original had no interactive feedback.
- **Added responsive design**, which the project was originally missing
  entirely despite being one of the stated goals. Added media queries so the
  hero section stacks vertically, padding shrinks, and text scales down on
  smaller screens.

## Author

Pramod Ghimire