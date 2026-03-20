# Design System Document: High-End Editorial Strategy

## 1. Overview & Creative North Star: "The Global Architect"
This design system moves beyond the "SaaS template" aesthetic to establish a visual language rooted in precision, legacy, and modern authority. Our Creative North Star is **"The Global Architect"**—a style that treats digital interfaces like a high-end architectural blueprint or a premium financial journal.

The system breaks away from generic layouts through **intentional asymmetry** and **tonal depth**. We favor generous whitespace (using the higher end of our spacing scale) and "breathing" layouts where content is organized not by lines, but by logic and light. Every element should feel curated, not just placed.

---

## 2. Colors & Surface Philosophy
The palette is anchored by a commanding corporate red (`primary: #98001b`), balanced by a sophisticated spectrum of stone, charcoal, and off-white.

### The "No-Line" Rule
To maintain a premium editorial feel, **1px solid borders are strictly prohibited** for sectioning. Boundaries must be defined through:
1.  **Tonal Shifts:** A `surface-container-low` (#f4f4f3) section sitting on a `surface` (#f9f9f8) background.
2.  **Negative Space:** Using `spacing-16` (5.5rem) or `spacing-20` (7rem) to create clear mental models of content separation.

### Surface Hierarchy & Nesting
Treat the UI as a series of stacked, high-grade paper layers. Use the surface tiers to create "nested" depth:
*   **Base:** `surface` (#f9f9f8) for the main canvas.
*   **Secondary Content:** `surface-container-low` (#f4f4f3) for subtle background shifts.
*   **Interactive/Elevated Elements:** `surface-container-lowest` (#ffffff) for cards or search bars to create a crisp, "popping" effect against the off-white base.

### The "Glass & Soul" Rule
Flat colors can feel static. To inject "soul":
*   **Signature Gradients:** Use a subtle linear gradient from `primary` (#98001b) to `primary_container` (#be1e2d) for hero CTAs to give them a three-dimensional, metallic weight.
*   **Glassmorphism:** For navigation bars or floating overlays, use `surface` at 80% opacity with a `20px` backdrop-blur. This ensures the sophisticated background colors bleed through, softening the interface.

---

## 3. Typography
Our typography is the voice of authority. It pairs the structural rigidity of **Inter** with the approachable clarity of **Public Sans**.

*   **Display & Headlines (Inter):** High-contrast sizing. Use `display-lg` (3.5rem) for hero statements to command attention. Letter spacing should be tightened slightly (-0.02em) for headlines to increase the "authoritative" feel.
*   **Titles & Body (Public Sans):** Designed for deep readability. Use `title-lg` for sector headings and `body-lg` (1rem) for insights. 
*   **Visual Rhythm:** Always maintain a 4:1 ratio between headline and body copy size in editorial sections to ensure a clear hierarchy that feels "designed" rather than "filled."

---

## 4. Elevation & Depth
In this system, depth is a whisper, not a shout. We reject heavy dropshadows in favor of **Tonal Layering**.

*   **The Layering Principle:** Place a `surface-container-lowest` card on top of a `surface-container-low` section. This creates a natural "lift" based on color value alone.
*   **Ambient Shadows:** When a floating state is required (e.g., a hovered service card), use a shadow with a 40px blur, 0% spread, and an opacity of 4% using the `on_surface` color. It should feel like a soft shadow on a gallery wall.
*   **The "Ghost Border" Fallback:** If accessibility requires a container boundary, use the `outline_variant` (#e3bebb) at **15% opacity**. This provides a hint of structure without cluttering the editorial flow.

---

## 5. Components

### Buttons: The Executive Action
*   **Primary:** A solid `primary` (#98001b) base with `on_primary` (#ffffff) text. Use `rounded-md` (0.375rem) for a sharp, professional look. 
*   **Hover State:** Transition to `primary_container` (#be1e2d) with a subtle `2px` upward shift to simulate physical tactility.
*   **Tertiary (Text-only):** `label-md` in `primary` with a custom `2px` underline that expands on hover.

### Service Cards: The Editorial Grid
*   **Style:** No borders. Background: `surface-container-lowest`. 
*   **Interaction:** On hover, the background shifts to `surface-bright`, and the `primary` red is introduced via a small, fluid organic line (inspired by the logo) at the top-right corner.
*   **Spacing:** Use `spacing-8` (2.75rem) internal padding to ensure the content never feels cramped.

### Input Fields: Minimalist Rigor
*   **Style:** Only a bottom border using `outline` (#8f6f6e) at 30% opacity. 
*   **Focus State:** The bottom border transforms into a 2px `primary` line. Label moves from `body-md` to `label-sm` using a smooth quintic transition.

### Navigation: The Glass Bar
*   **Style:** Fixed at the top, `surface` color at 85% opacity with backdrop-blur.
*   **Dividers:** Never use vertical lines between nav items. Use horizontal `spacing-6` (2rem) to separate links.

---

## 6. Do’s and Don'ts

### Do
*   **Do** use asymmetrical margins. For example, a headline might be offset further to the left than the body text to create an editorial "pull."
*   **Do** use `primary` red sparingly. It is a precision tool for focus, not a background color for large sections.
*   **Do** prioritize "Overlapping Elements." Let a high-quality corporate image slightly overlap a `surface-container` block to create 3D depth.

### Don’t
*   **Don’t** use pure black (#000000). Always use `on_surface` (#1a1c1c) for text to maintain a sophisticated, "ink-on-paper" feel.
*   **Don’t** use standard "cards-in-a-row" layouts for everything. Vary the grid—one large card followed by two smaller stacked ones.
*   **Don’t** use "neon" or high-vibrancy gradients. Stick to the tonal variations within the defined red and charcoal scales.
*   **Don't** use 1px dividers to separate list items. Use `spacing-4` (1.4rem) of vertical whitespace or a 1% shift in background grey.