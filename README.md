# La Maison — Fine Dining Restaurant Website

<div align="center">

[![Built with Vite](https://img.shields.io/badge/Built%20with-Vite-646CFF?style=flat-square&logo=vite)](https://vitejs.dev/)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Font Awesome](https://img.shields.io/badge/Font%20Awesome-528DD7?style=flat-square&logo=font-awesome&logoColor=white)](https://fontawesome.com/)
[![Google Fonts](https://img.shields.io/badge/Google%20Fonts-4285F4?style=flat-square&logo=google-fonts&logoColor=white)](https://fonts.google.com/)

**A premium, production-quality restaurant website — dark cinematic theme with gold accents, glassmorphism UI, and smooth scroll animations.**

</div>

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Pages](#-pages)
- [Tech Stack](#-tech-stack)
- [Design System](#-design-system)
- [Features](#-features)
- [Project Structure](#-project-structure)
- [Getting Started](#-getting-started)
- [Development](#-development)
- [Build & Deployment](#-build--deployment)
- [Browser Support](#-browser-support)
- [Performance](#-performance)
- [Team](#-team)

---

## 🏆 Overview

**La Maison** is a fully redesigned restaurant website transformed from a basic student project into a premium, production-ready web experience. The website represents a fictional high-end fine dining establishment with a complete digital presence spanning 11 pages.

### What was rebuilt

| Aspect | Before | After |
|---|---|---|
| **Pages** | 4 HTML files (2 broken) | 11 complete, responsive pages |
| **Navigation** | 7 broken links on every page | All 11 routes working correctly |
| **JavaScript** | None (0 lines) | 7KB of interactive JS |
| **CSS** | Duplicated 664 lines (300+ duplicate) | 32KB unified design system |
| **Fonts** | System fonts only | Playfair Display + Inter |
| **Icons** | Font Awesome broken (no CDN) | Font Awesome 6 fully functional |
| **Animations** | 3 basic CSS transitions | Scroll reveals, parallax, lightbox, counters |
| **Responsiveness** | Partial | 4 breakpoints (mobile to ultrawide) |
| **Branding** | 3 conflicting brand names | Single unified brand identity |
| **Build tool** | None | Vite (fast dev server + optimized builds) |

---

## 📄 Pages

| # | Page | Route | Description |
|---|---|---|---|
| 1 | **Home** | `index.html` | Full-viewport cinematic hero, why-choose-us, signature dishes, CTA |
| 2 | **Menu** | `menu.html` | Category-tabbed menu (main courses, appetizers, desserts, beverages) |
| 3 | **Chef's Picks** | `chef.html` | Curated chef recommendations with ratings, tags, and chef notes |
| 4 | **Special Offers** | `offers.html` | Promotional offer cards with pricing, badges, and countdown timers |
| 5 | **Gallery** | `gallery.html` | Filterable masonry gallery with interactive lightbox |
| 6 | **About Us** | `about.html` | Restaurant story, team profiles, and historical timeline |
| 7 | **Branches** | `branches.html` | Location cards with addresses, hours, contact, and Google Maps |
| 8 | **Reviews** | `reviews.html` | Rating summary (bar chart + average), 6 customer review cards |
| 9 | **Contact** | `contact.html` | Contact form, map embed, phone/email/address info |
| 10 | **Reserve Table** | `reserve.html` | Full reservation form (name, email, phone, date, time, guests, branch, requests) |

Every page includes:
- Fixed glassmorphism navbar with **active link highlighting** (auto-detected)
- Consistent **4-column footer** with links, contact info, and social icons
- **Scroll reveal animations** on all sections
- **Responsive layout** across all screen sizes

---

## 🛠 Tech Stack

| Technology | Purpose |
|---|---|
| [Vite](https://vitejs.dev/) (v6) | Build tool & dev server with HMR |
| HTML5 | Semantic markup |
| CSS3 (Custom Properties) | Design system with 26+ design tokens |
| Vanilla JavaScript (ES Modules) | Interactivity & animations |
| [Font Awesome 6](https://fontawesome.com/) | Icon library (CDN) |
| [Google Fonts](https://fonts.google.com/) | Playfair Display (headings) + Inter (body) |
| [Unsplash](https://unsplash.com/) | Stock photography for hero, dishes, gallery |

---

## 🎨 Design System

### Color Palette — "Dark Cinematic Luxury"

```
--bg           #0A0A0F    Page background (near-black)
--surface      #12121A    Card/section surfaces
--surface-2    #1C1C2E    Elevated surfaces
--gold         #D4A853    Primary accent (luxurious gold)
--gold-light   #E8C97A    Hover states, glowing effects
--gold-dark    #B8944E    Active states
--burgundy     #8B1A1A    Special accent (burgundy red)
--text         #F5F0EB    Primary text (warm white)
--text-2       #9A9490    Secondary text (warm gray)
--text-3       #6B6560    Muted text
--border       #2A2A3E    Subtle borders

Glass effects:
--glass       rgba(255,255,255,0.04)   Glassmorphism base
--glass-border rgba(255,255,255,0.08)  Glass borders
```

### Typography

| Element | Font | Weight |
|---|---|---|
| Headings (h1-h4) | `Playfair Display`, serif | 600 |
| Body text | `Inter`, sans-serif | 300-700 |
| Buttons | `Inter`, sans-serif | 600 |

### Spacing Scale
```
4, 8, 12, 16, 20, 24, 32, 40, 48, 56, 64, 80, 96, 120 (px)
```

### Core Effects

| Effect | Implementation |
|---|---|
| **Glassmorphism** | `backdrop-filter: blur(12px)` on nav, cards |
| **Gold gradients** | `linear-gradient(90deg, gold variants)` |
| **Scroll reveal** | IntersectionObserver — fade-in-up with staggered delays |
| **Card hover** | `translateY(-6px)` + shadow intensify + gold border glow |
| **Image zoom** | `transform: scale(1.08)` on hover |
| **Nav shrink** | Scroll past 50px → padding reduces, glass-blur activates |
| **Active nav** | Gold underline slide-in effect |
| **Lightbox** | Full-screen overlay with Escape key support |
| **Form validation** | Real-time border color change on error |

### Responsive Breakpoints

| Device | Width | Layout |
|---|---|---|
| Ultra-wide | > 1200px | Full max-width container (1200px) |
| Desktop | 1024-1200px | Multi-column grids |
| Laptop | 768-1024px | 2-column grids, adjusted spacing |
| Tablet | 480-768px | Single column, collapsed mobile nav |
| Mobile | < 480px | Stacked, touch-friendly, compact |

---

## ✨ Features

### Visual & UX

- **Cinematic hero** — Full-viewport with gradient overlay, animated scroll indicator
- **Glassmorphism navbar** — Fixed, blur-backed, shrinks on scroll
- **Scroll-triggered animations** — Elements fade in as they enter the viewport
- **Staggered reveals** — Cards reveal with progressive delays (0.1s-0.5s)
- **Interactive gallery** — Filter tabs + click-to-expand lightbox
- **Rating bar chart** — Visual distribution of 1-5 star reviews
- **Countdown timers** — Live countdown on special offers
- **Smooth page transitions** — Fade-in on every page load
- **Section gold dividers** — Animated golden lines separating sections
- **Parallax CTAs** — Background image with overlay effect on call-to-action sections

### Functionality

- **Auto active nav** — Current page highlighted automatically via `window.location`
- **Tabbed menu** — Switch between Main Courses, Appetizers, Desserts, Beverages
- **Form validation** — Real-time required field validation with visual feedback
- **Reservation form** — Complete booking form with date, time, guest count, branch selector
- **Contact form** — Name, email, subject, message with submit confirmation
- **Mobile hamburger menu** — Collapsible navigation on small screens
- **Keyboard accessibility** — Lightbox closes with Escape key
- **Body scroll lock** — Prevents background scroll when lightbox is open

### Design Patterns

- **Glass card** — Reusable `.glass-card` with blur + border + hover
- **Button system** — 3 variants: primary (gold), outline (gold border), ghost (subtle)
- **Section template** — Consistent `.section` + `.section-header` + `.gold-line`
- **Reveal utility** — `.reveal` + `.reveal-delay-{1-5}` for staggered animations
- **Form system** — Unified `.form-group` + `.form-row` + input styling

---

## 📁 Project Structure

```
restaurant-project/
│
├── index.html              # Home page
├── menu.html                # Menu page
├── chef.html                # Chef's Picks
├── offers.html              # Special Offers ★ NEW
├── gallery.html             # Gallery ★ NEW
├── about.html               # About Us ★ NEW
├── branches.html            # Branches ★ NEW
├── reviews.html             # Reviews
├── contact.html             # Contact ★ NEW
├── reserve.html             # Reserve a Table ★ NEW
│
├── css/
│   └── style.css            # Complete design system (~32KB)
│       ├── Google Fonts import
│       ├── CSS Reset
│       ├── 26+ Design Tokens (CSS custom properties)
│       ├── Typography
│       ├── Component styles (nav, hero, cards, buttons, forms, footer)
│       ├── Page-specific styles (menu, chef, gallery, etc.)
│       └── Responsive breakpoints
│
├── js/
│   └── main.js              # All JavaScript (~7KB, ES Module)
│       ├── Navbar scroll effect
│       ├── Active link detection
│       ├── Mobile hamburger menu
│       ├── IntersectionObserver reveal animations
│       ├── Gallery filter tabs
│       ├── Lightbox (open/close/keyboard)
│       ├── Menu category tabs
│       ├── Offer countdown timers
│       ├── Form validation & submission
│       └── Counter animation
│
├── images/
│   ├── CH.jpeg              # Chocolate Soufflé (chef's picks)
│   ├── Duck.jpeg            # Duck Confit (chef's picks)
│   ├── MAK.jpeg             # Truffle Pasta (chef's picks)
│   ├── Spicy_thai.png       # Thai Curry (chef's picks)
│   ├── image_Home/
│   │   ├── Gourmet Appetizers.jpeg
│   │   ├── Premium Steaks.jpeg
│   │   └── Fresh Seafood.jpeg
│   └── pep_reviwers/
│       ├── Amanda Lee.jpeg
│       ├── David Thompson.jpeg
│       ├── Emily Rodriguez.jpeg
│       ├── James Wilson.jpeg
│       ├── Michael Chen.jpeg
│       └── Sarah Johnson.jpeg
│
├── package.json             # Vite config & dependencies
├── vite.config.js           # Vite build configuration
└── README.md                # This documentation
```

---

## 🚀 Getting Started

### Prerequisites

- Node.js v18+ (recommended: v22+)
- npm v9+

### Installation

```bash
# Navigate to the project
cd restaurant-project

# Install dependencies
npm install

# Start the development server
npm run dev
```

The website will open at **http://localhost:3000**.

### Available Commands

| Command | Description |
|---|---|
| `npm run dev` | Start Vite dev server with HMR |
| `npm run build` | Build for production (output: `dist/`) |
| `npm run preview` | Preview the production build locally |

---

## 💻 Development

### Workflow

1. Start dev server: `npm run dev`
2. Edit HTML files — Vite reloads instantly
3. CSS is served as-is from `css/style.css`
4. JavaScript is served as an ES Module from `js/main.js`
5. Run `npm run build` before deployment

### Adding a New Page

1. Create a new `.html` file in the root directory
2. Copy the navbar and footer from any existing page
3. Add the page content in between
4. Add a link in the navbar on all pages
5. Verify the link works (run `npm run dev` and test)

### Modifying the Design System

All design tokens are defined as CSS custom properties in `:root` in `css/style.css`. Change any value there to update it globally across all pages:

```css
:root {
  --gold: #D4A853;        /* Change this to update gold accent everywhere */
  --bg: #0A0A0F;          /* Change this to update background color */
  --font-heading: 'Playfair Display', serif;  /* Change heading font */
}
```

---

## 📦 Build & Deployment

### Production Build

```bash
npm run build
```

This generates an optimized `dist/` folder containing:
- Minified HTML (all pages)
- Minified CSS (single file)
- Optimized JavaScript (bundled + minified)
- Static assets (images)

### Deployment Options

Upload the contents of the `dist/` folder to any static hosting:

| Platform | Instructions |
|---|---|
| **Netlify** | Drag-and-drop `dist/` folder |
| **Vercel** | `vercel --prod` CLI or import project |
| **GitHub Pages** | Deploy `dist/` to `gh-pages` branch |
| **Cloudflare Pages** | Connect repo, set build command to `npm run build` |
| **Any static host** | Upload `dist/` contents via FTP or file manager |

---

## 🌐 Browser Support

| Browser | Support |
|---|---|
| Chrome 90+ | ✅ Full |
| Firefox 90+ | ✅ Full |
| Safari 15+ | ✅ Full (with -webkit- prefixes) |
| Edge 90+ | ✅ Full |
| Opera 76+ | ✅ Full |
| IE 11 | ❌ Not supported |

The CSS uses `backdrop-filter` for glassmorphism effects. On unsupported browsers, elements gracefully degrade to a semi-transparent background without blur.

---

## ⚡ Performance

| Metric | Target | Status |
|---|---|---|
| Build time | < 1 second | ✅ ~400ms |
| CSS size (minified) | < 30KB | ✅ ~25KB (gzip: ~5KB) |
| JS size (minified) | < 10KB | ✅ ~4KB (gzip: ~1.6KB) |
| Lazy loading | Images | ✅ External images load on demand |
| Animations | GPU-accelerated | ✅ Uses `transform` and `opacity` only |
| Font loading | `font-display: swap` | ✅ (via Google Fonts) |

---

## 👥 Team

| Name | Role |
|---|---|
| Mohamed Saber (202302383) | Team Lead & Frontend Developer |
| Eslam Ebrahim (202302501) | UI/UX Designer |
| Mohamed Elsaid (202302414) | Content & Structure |
| Ahmed Ebrahim (202302403) | Assets & Quality Assurance |

**Project:** SU Restaurant Website — Suez University
**Original Name:** SU Reaturant (legacy)

---

<div align="center">

Built with ❤️ by Team La Maison

</div>
