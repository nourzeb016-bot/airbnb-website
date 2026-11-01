# The Cliffs — Luxury Coastal Stay

A single-page, Airbnb-inspired marketing website for **The Cliffs**, a luxury cliff-top holiday home on the Great Ocean Road, Victoria, Australia. The site showcases the property with cinematic, immersive visuals and guides visitors toward booking their stay through Airbnb.

Built entirely with **HTML, CSS, and vanilla JavaScript** — no frameworks and no build step.

---

## Overview

The Cliffs is a calm, premium landing page whose single goal is to inspire visitors to book. Every section is designed to build an emotional connection with the property and funnel the visitor toward a clear call to action.

Key ideas behind the design:

- A warm, coastal palette (soft beige, deep teal-ocean, sunset gold) defined as CSS custom properties.
- An editorial type pairing — a display serif with a clean sans — for a refined feel.
- A cinematic **scroll-reveal hero** where the property photo expands to fill the screen as you scroll.
- Consistent "Book on Airbnb" calls to action throughout the page.

---

## Main Features

- **Scroll-reveal hero** — a sticky, native-scroll animation: the cliff photo sits behind the headline while the property photo expands from a small panel to a full-screen image as you scroll, and the "THE CLIFFS" wordmark animates apart.
- **Live rooms gallery** — a "Rooms" section with three auto-scrolling columns of room photography; hover to pause a column and reveal a room's name, and click any photo to open it in a lightbox.
- **Lightbox viewer** — click a room image to pop it out full-size, with keyboard (`Esc`) and click-to-close support.
- **Light & dark theme** — a theme toggle that remembers the visitor's choice using `localStorage` (the site defaults to the dark coastal theme).
- **Scroll-triggered animations** — sections fade and rise into view using the `IntersectionObserver` API, with a word-by-word reveal on key headings.
- **Booking widget** — check-in / check-out / guests controls that compute the number of nights and link out to Airbnb, plus a sticky top dock with a "Book on Airbnb" button that appears once you scroll past the hero.
- **Live touches** — an animated stat count-up, a live local-time clock for Victoria, a whale-season badge, rotating ambience captions, and subtle scroll parallax on feature imagery.
- **Fully responsive** — adapts cleanly from large desktop screens down to mobile.
- **Accessibility-aware** — focus styles, keyboard support, and `prefers-reduced-motion` handling so animations respect user settings.
- **Zero dependencies** — no npm packages and no bundler; the only external resource is Google Fonts.

---

## Technologies Used

| Technology | Purpose |
|------------|---------|
| **HTML5** | Semantic page structure and content |
| **CSS3** | Styling, layout, and animation — custom properties (design tokens), Flexbox & Grid, fluid `clamp()` typography, media queries, and light/dark theming |
| **JavaScript (ES6, vanilla)** | Interactivity — `IntersectionObserver`, `requestAnimationFrame`, `localStorage`, `Intl.DateTimeFormat`, the scroll-reveal hero, and the booking controls |
| **Google Fonts** | Typography — *Cormorant Garamond* (display serif) and *Jost* (sans-serif) |
| **Git** | Version control |

> No front-end frameworks, CSS frameworks, or build tools are used. The project is intentionally lightweight, and all styles and scripts live inside `index.html`.

---

## Project Structure

```text
airbnb-website/
├── index.html                      # The entire website (markup, styles, and scripts)
├── README.md
├── .gitignore
│
├── images/
│   ├── hero.jpg
│   ├── hero-crop.jpg
│   └── rooms/
│       ├── oceanfront.jpg
│       ├── private-pool-villa.jpg
│       ├── ocean-view-suite.jpg
│       ├── penthouse-suite.jpg
│       ├── minimalist-suite.jpg
│       ├── cliffside-glass-villa.jpg
│       ├── honeymoon-suite.jpg
│       ├── cta-bg.jpg              # Final call-to-action background
│       ├── experiences-bg.jpg      # "Signature Experiences" background
│       ├── guest-bg.jpg            # Guest-note background
│       ├── footer-bg.jpg           # Footer background
│       └── gallery/                # Live rooms gallery (g1 / g2 / g3 of each room)
│           ├── g1-minimalist.jpg   g2-minimalist.jpg   g3-minimalist.jpg
│           ├── g1-oceanview.jpg    g2-oceanview.jpg    g3-oceanview.jpg
│           ├── g1-poolvilla.jpg    g2-poolvilla.jpg    g3-poolvilla.jpg
│           ├── g1-penthouse.jpg    g2-penthouse.jpg    g3-penthouse.jpg
│           ├── g1-cliffside.jpg    g2-cliffside.jpg    g3-cliffside.jpg
│           └── g1-honeymoon.jpg    g2-honeymoon.jpg    g3-honeymoon.jpg
│
├── images-by-admin/
│   └── hero.png                    # Hero background (coastal cliffs)
│
└── hero-image-showcase/
    └── property.png                # Property photo revealed in the hero
```

---

## Installation and Setup

No installation or dependencies are required — you only need the project files and a modern web browser.

1. **Clone the repository**

   ```bash
   git clone https://github.com/nourzeb016-bot/airbnb-website.git
   ```

2. **Move into the project folder**

   ```bash
   cd airbnb-website
   ```

That's it — there are no packages to install.

---

## Running the Website Locally

You can open the site directly, but running it through a local server is recommended so all images and fonts load reliably.

**Option 1 — Open directly**

Double-click `index.html`, or open it in your browser.

**Option 2 — VS Code Live Server (recommended)**

1. Install the *Live Server* extension in VS Code.
2. Right-click `index.html` and choose **"Open with Live Server"**.

**Option 3 — Python's built-in server**

```bash
# Python 3
python -m http.server 8000
```

Then visit `http://localhost:8000` in your browser.

**Option 4 — Node (serve)**

```bash
npx serve
```

---

## Author

**nourzeb016-bot**
Frontend Developer

- GitHub: [https://github.com/nourzeb016-bot](https://github.com/nourzeb016-bot)

---

## Notes

- This is a front-end project. The booking actions link out to Airbnb; there is no back-end or payment processing in this repository.
- Imagery is used to present the property.
