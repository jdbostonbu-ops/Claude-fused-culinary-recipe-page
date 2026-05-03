# Culinary Archive 🍽️
A high-performance, visually-driven culinary catalog built as a fusion of three premium design philosophies: Neo-Brutalist typography, Glassmorphic depth, and Cinematic Grid transitions.  Culinary Geometry presents 20 essential recipes through immersive 180° card flips, a full-panel recipe modal, and a live filter and search system — all delivered in pure Vanilla HTML, CSS, and JavaScript.

## 👤 Author
**Jacqueline**
[Check out my GitHub Profile](https://github.com/jdbostonbu-ops)
🚀 **[Launch — Culinary Archive](https://jdbostonbu-ops.github.io/Claude-fused-culinary-recipe-page/)**

<div align="center">
  <img src="src/Screen Recording 2026-05-03 at 2.58.41 PM.gif" width="100%" alt="Culinary Archive Demo">
</div>

---

# 🌟 Key Features

- **180° Card Flip Reveal:** Each recipe card rotates on hover using CSS `transform: rotateY(180deg)` with `transform-style: preserve-3d` and `backface-visibility: hidden` — the front shows the full-bleed image and title, the back reveals key ingredients, time, serves, difficulty level, and a "View Full Recipe" button.
- **Full-Panel Recipe Modal:** Clicking "View Full Recipe" opens a two-column cinematic modal — left side is a full-bleed image panel, right side delivers the complete ingredient list and numbered method steps with animated entrance using `cubic-bezier(0.16,1,0.3,1)`.
- **Live Filter & Search System:** Five category filter pills (All, Savory, Sweet, Seafood, Vegetarian) combined with a debounced keyword search — results re-render with a staggered card entrance animation on every filter change.
- **Custom Magnetic Cursor:** A dual-layer cursor system — a solid dot that moves at native speed and a trailing ring that follows with `0.12` lerp dampening, blending to `mix-blend-mode: difference` for a high-end editorial feel.
- **Cinematic Hero Section:** Full-viewport hero with animated scroll-reveal staggered text (`[data-reveal]` / `IntersectionObserver`), a gold ticker-tape headline bar, and a sweeping animated scroll cue line.
- **Staggered Card Entrance:** Every grid render applies per-card animation delays (`i * 0.06s`) for a cascading reveal on load and filter change.
- **Zero Dependencies:** Pure Vanilla HTML5, CSS3, and JavaScript ES6+ — no frameworks, no build tools, no npm.

---

# 🎨 Design Philosophy — Three Styles, One Vision

This project fuses all three design concepts into a single unified aesthetic:

### 1. Neo-Brutalist (Style #1)
- **Bebas Neue** display font — heavy, high-contrast typographic authority
- Gold `#e8c84a` on near-black `#0a0a08` — maximum contrast ratio
- `box-shadow: 6px 6px 0px rgba(0,0,0,0.8)` offset on all interactive buttons — the signature brutalist shadow
- Hard `border-radius: 4px` — minimal rounding, production call sheet influence
- Solid gold ticker tape headline bar running at full viewport width

### 2. Glassmorphic (Style #2)
- Sticky filter bar: `backdrop-filter: blur(20px)` over scrolling content
- Recipe modal overlay: `backdrop-filter: blur(24px)` with `rgba(5,5,4,0.92)` — full frosted-glass backdrop
- Card backs: inner glow via `box-shadow: inset 0 0 40px rgba(232,200,74,0.04)`
- Consistent glass border system throughout: `border: 1px solid rgba(255,255,255,0.10–0.25)`

### 3. Cinematic Grid (Style #3)
- Full-bleed `object-fit: cover` images with grayscale-to-full-color transition on hover
- 180° CSS card flip as the experimental reveal transition (`transform-style: preserve-3d`)
- Staggered `IntersectionObserver` scroll-reveal on hero text lines
- Cinematic two-panel modal with image filling the entire left column
- Film-grain noise texture overlay on the hero section via SVG `feTurbulence` filter

---

# 🌐 Browser & Device Compatibility

| Browser / Device | Status | Performance Notes |
| :--- | :--- | :--- |
| **Google Chrome** | ✅ Optimized | Full support — card flip, modal, cursor, blur, and all animations. |
| **Microsoft Edge** | ✅ Optimized | Matches Chrome's rendering engine exactly. |
| **Firefox** | ✅ Supported | Full feature support. Minor `backdrop-filter` rendering difference. |
| **Apple Safari (macOS)** | ✅ Supported | All features functional including card flip and glassmorphic blur. |
| **Safari (iPhone 17 OS)** | ✅ Supported | Touch interactions, filter pills, modal, and search fully functional. |
| **iPad / iPadOS** | ✅ Supported | Responsive grid adapts to tablet viewport. All interactions usable. |
| **Android Chrome** | ✅ Supported | Full mobile compatibility. |

> **Technical Note:** The custom cursor is hidden on touch devices via CSS `cursor: none` — touch-based interactions use native tap events with no functionality loss. The card flip hover state is preserved via `:focus-within` for keyboard and touch navigation.

---

# 🛠️ Tech Stack

- **Frontend:** Vanilla JavaScript (ES6+) — `IntersectionObserver`, `requestAnimationFrame`, `debounce`, `escHtml` sanitization, keyboard navigation
- **Styling:** CSS3 — Custom Properties (CSS variables), CSS Grid, Flexbox, `transform-style: preserve-3d`, `backdrop-filter`, `@keyframes`, `cubic-bezier` transitions
- **Typography:** Bebas Neue (display) + DM Serif Display (italic accent) + DM Mono (body/UI) via Google Fonts
- **Images:** Unsplash CDN — `loading="lazy"` with explicit `width` and `height` for layout stability
- **Storage:** No backend, no cookies, no localStorage — stateless on every load
- **Deployment:** GitHub Pages — zero-config static hosting

---

# 🚀 The User Flow

- **Land:** Full-viewport cinematic hero with staggered text reveal and scrolling gold ticker
- **Filter:** Select a category pill (Savory, Sweet, Seafood, Vegetarian) — grid re-renders with staggered animation
- **Search:** Type in the search field — debounced live search across title, tag, and ingredient list
- **Flip:** Hover any recipe card — 180° rotation reveals ingredients preview and difficulty on the back
- **Explore:** Click "View Full Recipe →" — full-panel cinematic modal opens with complete ingredients and numbered method steps
- **Dismiss:** Click the ✕ button, click the backdrop, or press `Escape` to close modal

---

# 🎓 Future Vision

- **WebGL Background:** Replace the CSS noise texture with a live GLSL shader for reactive, mouse-driven depth in the hero
- **Recipe Search API:** Connect to Spoonacular or Edamam API to expand beyond 20 static recipes to a dynamic live catalog
- **Saved Recipes:** Add localStorage persistence to bookmark favorites with a heart toggle per card
- **Print Stylesheets:** A `@media print` stylesheet that outputs a clean, single-column recipe card optimized for kitchen use
- **Expanded Categories:** Cocktails, Ferments, Pastry — expanding the catalog toward a definitive culinary reference

⭐ Love this project? Give it a star and explore the other projects in this portfolio.
