# Culinary Geometry 🍽️
A high-performance, visually-driven culinary catalog built as a fusion of three premium design philosophies: Neo-Brutalist typography, Glassmorphic depth, and Cinematic Grid transitions during an AI prompt asking AI to select one choice but in my prompt, I also took pieces of each option using one word from each option to examine if AI would combine all three. Culinary Geometry presents 20 fine-dining recipes through immersive 180° card flips, a full-panel recipe modal, and a cinematic scroll-reveal entrance — all delivered in pure Vanilla HTML, CSS, and JavaScript with zero dependencies.

## 👤 Author
**Jacqueline**
[Check out my GitHub Profile](https://github.com/jdbostonbu-ops)
🚀 **[Launch — Culinary Geometry](https://jdbostonbu-ops.github.io/Claude-fused-culinary-recipe-page/)**

<div align="center">
  <img src="src/Screen Recording 2026-05-03 at 2.58.41 PM.gif" width="100%" alt="Culinary Geometry Demo">
</div>

---

# 🌟 Key Features

- **180° Card Flip Reveal:** Each recipe card rotates on hover using CSS `transform: rotateY(180deg)` with `transform-style: preserve-3d` and `backface-visibility: hidden` — the front shows the full-bleed image and recipe title overlaid on a gradient, the back reveals key ingredients, cook time, difficulty level, and a "View Recipe" button.
- **Cinematic Geometry Mask Entrance:** Cards enter the viewport via a `clip-path` animation — each card starts collapsed at `polygon(0 50%, 100% 50%, 100% 50%, 0 50%)` and opens to full height on scroll using an `IntersectionObserver` with a staggered `100ms` delay per card.
- **Grayscale-to-Color Image Transition:** Card images load at `grayscale(80%) contrast(120%)` and transition to full color on hover with a simultaneous `scale(1.05)` zoom.
- **Full-Panel Recipe Modal:** Clicking "View Recipe" opens a two-column modal — on desktop the image occupies 45% of the panel width at full height with `object-fit: cover`, and the recipe content occupies the remaining 55% with a scrollable body. On mobile it stacks vertically with the image at `35vh`. The modal entrance uses `translateY(40px) scale(0.98)` animating to `translateY(0) scale(1)` via `cubic-bezier(0.175, 0.885, 0.32, 1.275)`.
- **Glassmorphic Modal Overlay:** The modal backdrop uses `backdrop-filter: blur(12px)` with `-webkit-backdrop-filter` fallback for Safari — a frosted dark glass layer over the recipe grid.
- **Hero Text Reveal Animation:** The hero title uses a `clip-path` keyframe animation that sweeps the text up from hidden to fully visible over `1.2s` using `cubic-bezier(0.85, 0, 0.15, 1)`. The subtitle fades up with a `0.6s` delay via a separate `fadeUp` keyframe.
- **Contact Section with Smooth Scroll:** A "Contact Us" nav link in the hero header smooth-scrolls via `scrollIntoView({ behavior: 'smooth' })` to a full contact section at the bottom of the page.
- **Fully Accessible:** ARIA roles (`role="dialog"`, `aria-modal`, `aria-labelledby`), focus management on modal open (`closeBtn.focus()`), `Escape` key to close modal, and `aria-label` on all interactive elements.
- **Zero Dependencies:** Pure Vanilla HTML5, CSS3, and JavaScript ES6+ — no frameworks, no build tools, no npm.

---

# 🎨 Design Philosophy — Three Styles, One Vision

This project fuses all three design concepts into a single unified aesthetic:

### 1. Neo-Brutalist (Style #1)
- Deep matte black background `#070707` with fiery orange accent `#FF4D00` — maximum contrast
- All-caps typography with tight `letter-spacing: -0.05em` on the hero title — bold editorial authority
- Hard `border-radius: 0.25rem` on cards — minimal rounding, sharp and industrial
- `btn-view` uses a transparent background with an orange `1px` border that fills solid on hover — classic brutalist button treatment
- Modal section headers use `letter-spacing: 0.15em` uppercase with an orange bottom border separator

### 2. Glassmorphic (Style #2)
- Modal overlay: `backdrop-filter: blur(12px)` with `-webkit-backdrop-filter` fallback for Safari compatibility
- Modal content panel: `background: #121212` with `border: 1px solid rgba(255,255,255,0.1)` — subtle glass border
- Card backs: `background: linear-gradient(135deg, #121212 0%, #000 100%)` with matching glass border
- Custom scrollbar on modal body styled with orange thumb (`scrollbar-color: var(--accent) var(--surface)`) and `scrollbar-width: thin`

### 3. Cinematic Grid (Style #3)
- `clip-path` polygon geometry mask reveal on scroll — the signature cinematic card entrance
- Full-bleed `object-fit: cover` images with grayscale-to-color transition on hover
- 180° CSS card flip as the primary content reveal interaction with `perspective: 1200px` for realistic depth
- Hero title `clip-path` sweep animation — text emerges from the bottom like a film title card
- Two custom easing curves: `--ease-cinematic: cubic-bezier(0.85, 0, 0.15, 1)` and `--ease-bounce: cubic-bezier(0.175, 0.885, 0.32, 1.275)`
- Event delegation on the grid container for dynamically generated cards — all 20 cards injected via JavaScript at runtime

---

# 📋 The 20 Recipes

| # | Recipe | Difficulty | Time |
| :--- | :--- | :--- | :--- |
| 1 | Smoked Wagyu Tartare | Expert | 25 Min |
| 2 | Pan-Seared Scallops | Medium | 15 Min |
| 3 | Miso Glazed Black Cod | Hard | 40 Min |
| 4 | Deconstructed Tiramisu | Medium | 45 Min |
| 5 | Venison Loin | Expert | 35 Min |
| 6 | Saffron Risotto | Medium | 30 Min |
| 7 | Charred Octopus | Hard | 60 Min |
| 8 | Duck Confit | Hard | 120 Min |
| 9 | Oyster Emulsion | Expert | 20 Min |
| 10 | Truffle Tagliatelle | Medium | 25 Min |
| 11 | Beetroot Salad | Medium | 50 Min |
| 12 | Pork Belly Bao | Hard | 90 Min |
| 13 | Matcha Mille-Feuille | Expert | 180 Min |
| 14 | Lobster Thermidor | Hard | 45 Min |
| 15 | King Crab Legs | Medium | 30 Min |
| 16 | Foie Gras Torchon | Expert | 24 Hrs |
| 17 | Hamachi Crudo | Medium | 15 Min |
| 18 | Pigeon Pithivier | Expert | 120 Min |
| 19 | Squid Ink Chitarra | Hard | 35 Min |
| 20 | Yuzu Soufflé | Expert | 40 Min |

---

# 🌐 Browser & Device Compatibility

| Browser / Device | Status | Performance Notes |
| :--- | :--- | :--- |
| **Google Chrome** | ✅ Optimized | Full support — card flip, clip-path reveal, modal blur, and all animations. |
| **Microsoft Edge** | ✅ Optimized | Matches Chrome's rendering engine exactly. |
| **Firefox** | ✅ Supported | Full feature support. Minor `backdrop-filter` rendering difference. |
| **Apple Safari (macOS)** | ✅ Supported | Full support including `-webkit-backdrop-filter` fallback. |
| **Safari (iPhone 17 OS)** | ✅ Supported | Touch interactions and modal fully functional. Card flip triggers on tap via `:focus-within`. |
| **iPad / iPadOS** | ✅ Supported | Responsive grid adapts to tablet viewport using CSS Grid `auto-fill` and `minmax`. |
| **Android Chrome** | ✅ Supported | Full mobile compatibility. |

> **Technical Note:** The card flip hover state is preserved for keyboard and touch navigation via `:focus-within` on the `.card` wrapper. The modal traps focus on open and restores it via `closeBtn.focus()`. The `Escape` key is handled via a global `keydown` event listener.

---

# 🛠️ Tech Stack

- **Frontend:** Vanilla JavaScript (ES6+) — `DOMContentLoaded`, `IntersectionObserver`, event delegation, `classList`, `setAttribute`, `scrollIntoView`, focus management
- **Styling:** CSS3 — Custom Properties (CSS variables), CSS Grid (`auto-fill`, `minmax`), Flexbox, `transform-style: preserve-3d`, `clip-path`, `backdrop-filter`, `@keyframes`, `cubic-bezier` easing, custom scrollbars, `clamp()` for fluid typography
- **Typography:** `"Helvetica Neue"`, Inter, system-ui — system font stack, no external font dependency
- **Images:** Mixed local assets (`src/` folder) and Unsplash CDN — all with `loading="lazy"` for performance
- **Easing:** Two custom curves — `cubic-bezier(0.85, 0, 0.15, 1)` (cinematic) and `cubic-bezier(0.175, 0.885, 0.32, 1.275)` (bounce)
- **Storage:** No backend, no cookies, no localStorage — stateless on every load
- **Deployment:** GitHub Pages — zero-config static hosting

---

# 🚀 The User Flow

- **Land:** 40vh hero with `clip-path` text sweep animation and subtitle `fadeUp` — title reveals like a film title card
- **Scroll:** Recipe cards enter through a cinematic geometry mask (`clip-path` polygon) with staggered `100ms` delays per card via `IntersectionObserver`
- **Flip:** Hover any recipe card — 180° rotation over `0.9s` with bounce easing reveals ingredients, time, difficulty, and the "View Recipe" button
- **Explore:** Click "View Recipe" — full-panel modal opens with recipe image (45%) left and step-by-step preparation (55%) right on desktop
- **Dismiss:** Click the ✕ button, click the backdrop overlay, or press `Escape` to close the modal
- **Contact:** Click "Contact Us" in the hero nav — smooth scrolls to the contact section below all 20 recipe cards

---

# 🎓 Future Vision

- **Filter & Search:** Add category filter pills and a debounced keyword search across recipe titles and ingredients
- **Recipe Expansion:** Connect to Spoonacular or Edamam API to extend beyond the 20 static fine-dining concepts
- **Saved Recipes:** Add `localStorage` persistence to bookmark favourites with a heart toggle per card
- **Print Stylesheets:** A `@media print` stylesheet outputting a clean single-column recipe card for kitchen use
- **WebGL Hero:** Replace the CSS `clip-path` hero with a live GLSL shader for mouse-reactive depth

⭐ Love this project? Give it a star and explore the other projects in this portfolio.
