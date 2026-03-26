# Design System Strategy: Technical Precision & Primal Flow

## 1. Overview & Creative North Star
The Creative North Star for this design system is **"The Digital Apex Predator."** 

This system lives at the collision point between the cold, calculated geometry of techwear and the visceral, fluid power of a martial artist. In combat sports, technical mastery (Geometry) provides the structure, while instinctive movement (Organic) provides the soul. 

We break the "standard template" look by utilizing high-contrast corner treatments—where rigid, 45-degree angled containers house hyper-fluid "ink-bleed" imagery. The layout uses intentional asymmetry; content shouldn't just sit on a grid, it should feel trapped within a technical framework, ready to burst out. We favor extreme typography scales and overlapping elements to create a sense of aggressive depth.

## 2. Colors & Surface Philosophy
The palette is built on a foundation of obsidian and metallic silver, punctuated by "bioluminescent" accents that signify high-energy interaction points.

### The Palette
*   **Background:** `#0e0e0e` (Deep Obsidian)
*   **Primary (Bioluminescent):** `#81ecff` (Electric Blue)
*   **Secondary (Metallic):** `#e3e2e2` (Silver/Charcoal)
*   **Tertiary (Primal):** `#c47fff` (Purple Accent)

### The "No-Line" Rule
Standard 1px borders are strictly prohibited for defining sections. We define boundaries through **Tonal Shifting**. A section transition must occur by moving from `surface` to `surface-container-low` or `surface-container-high`. This creates a sophisticated, architectural feel rather than a "boxed-in" web look.

### Surface Hierarchy & Glassmorphism
*   **Layering:** Treat the UI as a series of stacked technical plates. Use `surface-container-lowest` for background utility areas and `surface-container-highest` for prominent interactive cards.
*   **The Signature Glow:** Main CTAs should not be flat. Use a subtle linear gradient transitioning from `primary` (#81ecff) to `primary-container` (#00e3fd) to mimic the glow of a technical interface.
*   **Technical Glass:** For floating overlays, use a background blur (minimum 20px) with `surface-variant` at 60% opacity. This allows the organic "tentacle" textures of the background to bleed through the geometric UI.

## 3. Typography
The typography is an exercise in tension: the mechanical rigidity of **Space Grotesk** against the functional clarity of **Inter**.

*   **Display & Headlines (Space Grotesk):** Used for "The Primal." These should be bold, condensed, and aggressive. Use `display-lg` (3.5rem) for hero statements to dominate the screen.
*   **Technical Metadata (Mono/Space Grotesk Label):** Use `label-md` for data like weight classes, session times, or "System Status." This reinforces the techwear aesthetic.
*   **Body & Title (Inter):** Used for "The Technical." Inter provides the necessary legibility for complex training descriptions and instructional content.

## 4. Elevation & Depth
We eschew traditional drop shadows for **Tonal Layering** and **Luminous Depth**.

*   **The Layering Principle:** Instead of a shadow, place a `surface-container-high` card against a `surface-dim` background. The slight shift in grey values creates a modern, premium lift.
*   **Ambient Shadows:** If a floating element (like a modal) requires a shadow, use a large blur (40px+) with an extremely low opacity (6%) using the `primary` color as the shadow tint. This creates a "glow" rather than a shadow.
*   **The "Ghost Border" Fallback:** If a technical line is required, use the `outline-variant` token at 15% opacity. This mimics laser-etched glass rather than a digital stroke.
*   **45-Degree Clipping:** Every major container must feature a 45-degree "clipped corner" (Geometry) while the image inside utilizes a curved, wavy mask (Organic).

## 5. Components

### Buttons (The Pill vs. The Plate)
*   **Primary:** High-contrast `primary` (#81ecff) background. Shape must be `rounded-full` (Pill shape) to contrast against the sharp-angled sections they inhabit.
*   **Secondary/Outlined:** Use the "Ghost Border" (15% opacity `outline-variant`) with `secondary` text. 

### Input Fields & Controls
*   **Inputs:** Sharp corners (`rounded-none`). The focus state should not be a border change, but a 1px `primary` underline and a subtle `surface-container-highest` background shift.
*   **Checkboxes/Radios:** Use `primary` for the "on" state. These are the only elements allowed to be perfectly circular to mimic technical "status lights."

### Cards & Lists
*   **Card Structure:** No dividers. Use `spacing-8` (1.75rem) as a vertical gap to separate list items. 
*   **Masking:** Cards should use a subtle technical texture (scanlines) at 3% opacity to feel like a high-end interface.

### Signature Component: The "Anatomy" Overlay
A custom component where a technical line (using the `primary` blue) connects a mono-font label (`label-sm`) to a specific point on a fluid, organic muscle/ink-bleed graphic. This perfectly marries the system's "Technical" and "Primal" pillars.

## 6. Do's and Don'ts

### Do
*   **Do** overlap typography. Let a large `display-lg` headline sit 20% over a background image.
*   **Do** use 45-degree diagonal lines as decorative "break-outs" in your grid.
*   **Do** use extreme contrast—white text on obsidian backgrounds.

### Don't
*   **Don't** use standard 1px borders to separate content sections.
*   **Don't** use standard "drop shadows" (black, high opacity). 
*   **Don't** use rounded corners on large containers; keep them sharp (`rounded-none`) to maintain the technical edge.
*   **Don't** use vibrant colors for body text. Keep all long-form text in `on-surface` (pure white) or `on-surface-variant` (soft grey) for elite-level readability.