# Design System Strategy: The Precision Press

## 1. Overview & Creative North Star
**Creative North Star: "The Architectural Ledger"**
This design system moves away from the generic "neighborhood print shop" aesthetic and towards a high-end, editorial experience that mirrors the precision of modern printing technology. We treat digital space like a premium canvas. By utilizing **intentional asymmetry**, **exaggerated white space**, and **tonal layering**, we create an environment of absolute reliability. The goal is to make the user feel as though their documents are being handled by a luxury architectural firm, not just a retail shop.

We break the "template" look by using a rigorous "no-line" philosophy and a typography scale that favors dramatic contrast between massive display headers and hyper-legible utility text.

---

## 2. Colors: Tonal Depth & Soul
We move beyond flat hex codes to a system of "Atmospheric Blue" and "Active Red."

### The Palette
*   **Primary Core:** `primary` (#00236f) and `primary_container` (#1e3a8a). Used for authoritative moments.
*   **Secondary Energy:** `secondary` (#bb0112) for precision alerts and high-importance CTAs.
*   **The Neutrals:** A sophisticated range of `surface` tokens from `surface_container_lowest` (#ffffff) to `surface_dim` (#d9dadc).

### The "No-Line" Rule
**Explicit Instruction:** Prohibit the use of 1px solid borders for sectioning content. Boundaries must be defined solely through background color shifts. To separate a pricing table from a hero section, transition from `surface` to `surface_container_low`. The eye should perceive change through "weight" and "fill," never through a drawn line.

### Surface Hierarchy & Nesting
Treat the UI as physical layers of stacked paper.
*   **Base:** `surface` (#f8f9fb).
*   **Sectioning:** `surface_container_low` (#f3f4f6) for secondary information.
*   **Prominence:** Place a `surface_container_lowest` (#ffffff) card on top of a `surface_container_low` background to create a "lifted" feel without a shadow.

### The "Glass & Gradient" Rule
To avoid a "flat" corporate feel, use **Glassmorphism** for floating navigation bars or selection overlays. Utilize `surface_container_lowest` at 80% opacity with a `24px` backdrop blur. For primary CTAs, apply a subtle linear gradient from `primary` to `primary_container` at a 135-degree angle to provide a metallic, "ink-like" sheen.

---

## 3. Typography: The Editorial Edge
We use **Plus Jakarta Sans** (Display/Headings) for a modern, geometric authority and **Inter** (Body/Labels) for neutral, high-speed legibility.

*   **Display (Large/Medium):** Use for hero value propositions. The tight tracking and `plusJakartaSans` weight communicate "Industrial Strength."
*   **Headline (Small/Medium):** Used for service categories (e.g., "Large Format Printing").
*   **Title & Body:** `Inter` provides the "functional" contrast. While the headlines are bold and loud, the body text is spaced generously to ensure no "ink-bleed" visual fatigue.
*   **Hierarchy Note:** Always maintain a minimum 2:1 scale ratio between your `headline-lg` and `body-md` to ensure a premium, spacious feel.

---

## 4. Elevation & Depth: Tonal Layering
We reject the 2010-era "drop shadow." Depth is achieved through light and atmospheric density.

*   **The Layering Principle:** Stack `surface-container` tiers. An "Order Summary" panel should be `surface-container-highest` nesting inside a `surface-container-low` page.
*   **Ambient Shadows:** For floating elements (Modals/Dropdowns), use a multi-layered shadow:
    *   *Shadow:* `0px 12px 32px rgba(0, 35, 111, 0.06)` (A tinted shadow using the `on-surface` color). This mimics natural light passing through blue-tinted glass.
*   **The "Ghost Border" Fallback:** If a border is required for accessibility (e.g., Input Fields), use `outline_variant` at **20% opacity**. It should be a suggestion of a container, not a cage.

---

## 5. Components: Precision Primitives

### Buttons: The "Action Block"
*   **Primary:** Massive, `9999px` (full) rounded edges or `0.75rem` (xl) for a more architectural look. Background: `primary` gradient. Text: `on_primary` (Bold).
*   **Secondary:** `surface_container_lowest` with a "Ghost Border."
*   **States:** On hover, the primary button should shift to `primary_container` with a subtle `4px` vertical lift.

### Input Fields: The "Typewriter"
*   **Style:** No background fill. Only a bottom-weighted `outline_variant` (20% opacity) or a subtle `surface_container_low` background.
*   **Focus:** Transition the bottom border to `primary` (2px thickness).

### Cards & Lists: The "No-Divider" Protocol
*   **Rule:** Forbid 1px dividers between list items. Use `16px` of vertical white space or alternate row colors using `surface` and `surface_container_low`. 
*   **Service Cards:** Use `xl` (0.75rem) corner radius. Elements inside the card should overlap the edge slightly (intentional asymmetry) to break the "boxed-in" feel.

### Specialized Component: The "Print Status" Chip
*   **Design:** Use `tertiary_container` for "In Progress" (Warm Orange/Brown) and `secondary_container` for "Urgent." These should be pill-shaped and use `label-sm` typography.

---

## 6. Do's and Don'ts

### Do
*   **Do** use extreme white space. If you think there is enough padding, add 8px more.
*   **Do** use asymmetrical layouts (e.g., a large headline on the left with body text offset to the right).
*   **Do** use `primary_fixed_dim` for subtle background accents to keep the "Blue" brand identity present without being overwhelming.

### Don't
*   **Don't** use black (#000000). Use `on_surface` (#191c1e) for all "black" text to maintain a high-end softened contrast.
*   **Don't** use standard "Drop Shadows." If it looks like a default Photoshop shadow, delete it.
*   **Don't** use 1px borders to separate content. Let the background colors do the work.
*   **Don't** crowd the "Call to Action." A print shop is about "output"—give the buttons room to breathe.