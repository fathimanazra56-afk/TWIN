# Design System: High-End Editorial Luxe

## 1. Overview & Creative North Star: "The Digital Atelier"
This design system is not a template; it is a curated editorial experience. Our Creative North Star is **The Digital Atelier**. Much like a high-end boutique in Paris or Milan, the interface must feel spacious, tactile, and intentionally composed. 

We break the "standard e-commerce grid" by embracing **Intentional Asymmetry**. Product imagery should breathe, often overlapping container boundaries or sitting off-center to create a sense of movement. We shun the "boxed-in" look of traditional web design in favor of layered, organic compositions that guide the eye through tonal depth rather than rigid lines.

---

## 2. Colors & Tonal Depth
The palette is a sophisticated blend of earthen neutrals and metallic warmth, designed to evoke the feeling of fine linen and gold hardware.

### The "No-Line" Rule
**Prohibit 1px solid borders for sectioning.** To define boundaries, use background color shifts. A product gallery sitting on `surface` (`#fbf9f5`) might transition into a "Featured Collection" section using `surface-container-low` (`#f5f3ef`). This creates a seamless, high-end flow.

### Surface Hierarchy & Nesting
Treat the UI as physical layers of premium paper.
*   **Base:** `surface` (#fbf9f5) for the widest layout areas.
*   **Nesting:** Place a `surface-container-lowest` (#ffffff) card atop a `surface-container` (#efeeea) background to create a "lift" that feels natural and light.
*   **The Glass & Gradient Rule:** For navigation bars or floating "Quick Buy" menus, use **Glassmorphism**. Apply `surface` at 80% opacity with a `24px` backdrop-blur. 
*   **Signature Textures:** For primary Action Buttons or Hero accents, use a subtle linear gradient from `primary` (#725b28) to `primary-container` (#bea268) at a 135-degree angle. This mimics the shimmer of brushed gold.

---

## 3. Typography: The Editorial Contrast
We pair a high-contrast serif with a functional sans-serif to mirror the aesthetic of a luxury fashion magazine.

*   **Display & Headlines (Noto Serif):** Used for brand moments and collection titles. The high-contrast strokes convey authority and elegance. 
    *   *Usage:* `display-lg` for Hero headers; `headline-md` for category titles.
*   **Body & Labels (Manrope):** A modern sans-serif that ensures legibility in product descriptions and navigation.
    *   *Usage:* `body-lg` for product descriptions; `label-md` for uppercase "Add to Cart" text to maintain a clean, architectural look.
*   **Hierarchy Note:** Always over-size your headlines. A `display-lg` title should feel significantly more "important" than the `body-lg` text beneath it, creating a clear editorial focal point.

---

## 4. Elevation & Depth
In this system, we do not use "shadows" in the traditional sense; we use **Ambient Glows**.

*   **The Layering Principle:** Achieve depth by stacking `surface-container` tiers. A `surface-container-highest` (#e4e2de) element acts as a "heavy" base, while `surface-container-lowest` (#ffffff) feels like a light, floating sheet.
*   **Ambient Shadows:** For floating elements (Modals, Hovered Cards), use: `0px 20px 40px rgba(114, 91, 40, 0.06)`. This uses a tiny fraction of the `primary` gold color to create a warm, natural lift rather than a cold grey shadow.
*   **The Ghost Border Fallback:** If a divider is mandatory for accessibility, use `outline-variant` (#d1c5b4) at **15% opacity**. It should be felt, not seen.
*   **Soft Rounding:** Use the `md` (0.375rem) or `lg` (0.5rem) tokens for components. This provides a "tailored" feel—neither sharp and aggressive nor overly "bubbly" and tech-focused.

---

## 5. Components

### Buttons: The "Jewelry" of the UI
*   **Primary:** Gradient from `primary` to `primary-container`. Typography: `label-md` in `on-primary` (#ffffff), uppercase with 0.05em letter spacing.
*   **Secondary:** Ghost style. No background. `outline` (#7f7667) border at 20% opacity. On hover, transition to `surface-container-low`.
*   **Tertiary:** Text only, underlined with a 1px offset using the `surface-tint` (#725b28).

### Input Fields: Clean Minimalism
*   **Style:** No background (transparent). A single `outline-variant` (#d1c5b4) bottom border. 
*   **States:** On focus, the bottom border transitions to `primary` (#725b28) and the label floats upward using `label-sm`.

### Cards & Product Grids
*   **Rule:** Forbid divider lines. 
*   **Structure:** Use `spacing-6` (2rem) of vertical whitespace to separate the image from the product title. Use `surface-container-lowest` for the card background to make product photography "pop" against the `surface` background.

### Editorial Specialty Components
*   **Lookbook Carousel:** An asymmetric slider where images vary in aspect ratio (e.g., 4:5 paired with 1:1), using `spacing-10` to create a "gallery wall" effect.
*   **Floating Navigation:** A centered, glassmorphic pill using `rounded-full` that appears on scroll-up, containing only essential icons and a "Bag" count.

---

## 6. Do's and Don'ts

### Do:
*   **Embrace Negative Space:** If a section feels crowded, double the spacing token (e.g., move from `spacing-8` to `spacing-16`).
*   **Use Tonal Transitions:** Separate the Footer from the Main content using a shift from `surface` to `surface-dim`.
*   **Editorial Imagery:** Use photography with soft, warm lighting that complements the beige and gold palette.

### Don't:
*   **No Pure Black:** Never use `#000000`. Use `on-surface` (#1b1c1a) for all high-contrast text to keep the "premium" softness.
*   **No Heavy Borders:** Never use 100% opaque borders to define a container. It breaks the "Atelier" flow.
*   **No Standard Grids:** Avoid the "4-column-row" look where possible. Try a "2-large, 3-small" masonry layout for product discovery.

---

*Director's Final Note: Remember, the goal of this system is to make the user feel like they are flipping through a luxury magazine, not scrolling through a database. Every pixel should feel intentional, quiet, and expensive.*