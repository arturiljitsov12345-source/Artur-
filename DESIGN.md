# Design System Strategy: The Digital Archivist

## 1. Overview & Creative North Star
The Creative North Star for this design system is **"The Digital Archivist."** 

We are not building a standard social portal; we are designing a living heritage. The goal is to evoke the tactile prestige of a leather-bound yearbook translated into a fluid, modern digital experience. We move beyond the "template" look by rejecting rigid, boxy grids in favor of **Intentional Editorial Asymmetry**. 

By layering rich `primary` (Dark Blue) depths against `surface` (Soft Beige) breaths of air, we create a sense of "The Golden Hour"—that nostalgic, emotional glow of looking back while moving forward. We use high-contrast typography scales and overlapping elements to ensure the UI feels curated, professional, and deeply personal.

---

## 2. Colors: Tonal Depth & The "No-Line" Rule
This palette is rooted in tradition but executed with modern restraint.

*   **Primary (`#002045`):** The "Scholar’s Ink." Use this for high-authority moments, deep headers, and grounding elements.
*   **Secondary (`#775a19`):** The "Heritage Gold." Use sparingly for highlights, active states, and prestige markers.
*   **Surface & Background (`#fcf9f4`):** The "Vellum." A soft, warm beige that prevents the digital fatigue of pure white.

### The "No-Line" Rule
**Explicit Instruction:** Designers are prohibited from using 1px solid borders to define sections. Layout boundaries must be achieved through:
1.  **Background Shifts:** Transitioning from `surface` to `surface-container-low` to define a new content block.
2.  **Tonal Transitions:** Using the `surface-variant` for subtle structural changes.

### Surface Hierarchy & Nesting
Treat the UI as physical layers of fine paper. 
*   **Level 0:** `surface` (The base page).
*   **Level 1:** `surface-container-low` (Secondary content regions).
*   **Level 2:** `surface-container-highest` (Interactive cards or floating modules).
Nesting a `surface-container-lowest` card inside a `surface-container-low` section creates a natural "lift" that feels organic rather than engineered.

### Glass & Gradient Signature
To move beyond a "flat" appearance:
*   **Glassmorphism:** For floating navigation or over-image modals, use `surface` at 80% opacity with a `backdrop-blur` of 20px. 
*   **Signature Gradients:** For primary CTAs, use a subtle linear gradient from `primary` (`#002045`) to `primary_container` (`#1a365d`) at a 135-degree angle. This adds a "silk" sheen that flat hex codes cannot replicate.

---

## 3. Typography: The Editorial Voice
We pair the intellectual rigor of a serif with the modern clarity of a geometric sans-serif.

*   **Display & Headlines (`newsreader`):** Our "Legacy" typeface. Large-scale serifs communicate authority and nostalgia. Use `display-lg` (3.5rem) for hero statements and `headline-md` (1.75rem) for storytelling chapters.
*   **Body & Titles (`manrope`):** Our "Utility" typeface. A modern sans-serif that ensures readability across generations. Use `body-lg` (1rem) for long-form alumni stories to maintain an approachable, professional tone.

**Hierarchy Note:** Always lead with the serif to establish the "Editorial" feel, then support with the sans-serif for functional data.

---

## 4. Elevation & Depth: Tonal Layering
Traditional drop shadows are too "software-like." We use **Ambient Shadows** and **Tonal Layering** to define space.

*   **Layering Principle:** Instead of a shadow, place a `surface-container-lowest` card on a `surface-container-low` background. The slight delta in beige tones creates a sophisticated, soft-edge separation.
*   **Ambient Shadows:** If a card must float (e.g., a featured donation prompt), use a shadow with a 40px blur and only 4% opacity. The shadow color should be a tint of `on-surface` (`#1c1c19`), never pure black.
*   **The "Ghost Border" Fallback:** If accessibility requires a stroke, use `outline-variant` at 15% opacity. High-contrast, 100% opaque borders are strictly forbidden.

---

## 5. Components

### Buttons
*   **Primary:** `primary` background with `on-primary` text. Use `full` (pill) roundedness for a "Smooth" feel. Include a 2px horizontal "Heritage Gold" (`secondary`) underline on hover for a signature touch.
*   **Secondary:** `surface-container-highest` background with `primary` text. No border.

### Cards & Lists
*   **The "No-Divider" Rule:** Never use horizontal lines to separate list items. Use the **Spacing Scale** (specifically `spacing-6` or `spacing-8`) to create "breathing room" or use alternating `surface-container-low` and `surface-container-lowest` backgrounds.
*   **Cards:** Use `lg` (1rem) or `xl` (1.5rem) corner radii. Cards should feel like rounded stationary, not sharp digital tiles.

### Input Fields
*   **Styling:** Use `surface-container-low` as the fill. On focus, transition the background to `surface-container-lowest` and add a "Ghost Border" of `primary` at 20% opacity.

### Navigation (The "Floating Header")
*   Utilize a `surface` background with a 90% opacity and a heavy `backdrop-blur`. The header should feel like it is floating over the content, subtly picking up the colors of the imagery beneath it.

---

## 6. Do’s and Don’ts

### Do:
*   **Embrace Asymmetry:** Offset images and text blocks. Let a photo of the campus spill over the edge of a container to create a "scrapbook" feel.
*   **Use White Space as a Luxury:** High-end design is defined by what you leave out. Use `spacing-20` (7rem) between major sections.
*   **Tint Your Greys:** Every "neutral" color should lean toward the warm beige (`surface`) or deep navy (`primary`) to ensure the palette feels emotional and cohesive.

### Don't:
*   **Don't use 100% Black:** It is too harsh for a nostalgic brand. Use `on-surface` (`#1c1c19`) for text.
*   **Don't use Sharp Corners:** Except for the very edge of the screen, everything should have a minimum of `sm` (0.25rem) roundedness to maintain the "smooth" requirement.
*   **Don't Over-Animate:** Transitions should be "Slow and Heavy" (e.g., 400ms Ease-Out) to mimic the feeling of turning a thick page of a book.