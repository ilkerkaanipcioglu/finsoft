# Design System Document: Corporate High-End Editorial

## 1. Overview & Creative North Star: "The Financial Architect"

This design system is built to transform complex SAP Finance expertise into a premium, editorial-grade digital experience. We move away from the "standard corporate template" by embracing a philosophy we call **The Financial Architect**. 

The aesthetic is grounded in the precision of high finance and the forward-leaning nature of enterprise technology. We achieve this through:
*   **Intentional Asymmetry:** Breaking the 12-column grid with hero elements that bleed off-canvas or sit in unexpected gutters.
*   **Sophisticated Breathing Room:** Using large scale-20 and scale-24 spacing tokens to isolate key value propositions, ensuring the "SAP Financial Expert" messaging has the gravity it deserves.
*   **High-Contrast Tech Details:** Pairing the deep `on-background` (#131B2E) with vibrant `primary-container` (#10B981) accents to evoke a sense of a high-tech dashboard.

## 2. Colors: Tonal Depth & The "No-Line" Rule

The palette is designed to convey stability and growth. We use color not just for decoration, but as a structural tool.

### The "No-Line" Rule
Traditional 1px borders are strictly prohibited for sectioning. To separate content, designers must use background shifts. For example, a section using `surface-container-low` should sit directly against a `surface` background. This creates a seamless, modern flow that feels engineered rather than "boxed in."

### Surface Hierarchy & Nesting
Treat the UI as a physical stack of premium materials:
*   **Base Layer:** `surface` (#FAF8FF) - Used for the main page canvas.
*   **Floating Layers:** `surface-container-lowest` (#FFFFFF) - Reserved for high-priority cards or navigation bars.
*   **Recessed Layers:** `surface-container` (#EAEDFF) - Used for background sections that contain multiple secondary elements.

### The "Glass & Gradient" Rule
For hero sections and key CTAs, use a subtle linear gradient transitioning from `primary` (#006C49) to `primary-container` (#10B981). For floating navigation or language selectors, utilize **Glassmorphism**: apply `surface-container-lowest` at 70% opacity with a `20px` backdrop-blur to create a "frosted glass" effect that feels deeply integrated into the environment.

## 3. Typography: Editorial Authority

We utilize two distinct typefaces to balance human-centric service with technical precision.

*   **Headlines (IBM Plex Sans):** This is our "Technical Backbone." The geometric nature of IBM Plex Sans reflects SAP’s data-driven world. Use `display-lg` for hero statements with tight letter-spacing (-0.02em) to command attention.
*   **Body (Inter):** Our "Communication Engine." Inter provides maximum readability for complex financial explanations.
*   **Hierarchy Strategy:** We use a high-contrast scale. A `display-lg` headline should often be followed by a `body-lg` intro text to create a clear "Editorial Hook" that guides the user’s eye immediately to the most important information.

## 4. Elevation & Depth: Tonal Layering

We eschew traditional drop shadows in favor of **Tonal Layering**.

*   **Layering Principle:** Instead of a shadow, place a `surface-container-highest` element inside a `surface` area. The 1-2% shift in color provides all the "lift" necessary for a high-end look.
*   **Ambient Shadows:** If a card must "float" (e.g., a hovered state), use a shadow tinted with the `on-surface` color: `rgba(19, 27, 46, 0.06)` with a 40px blur and 12px Y-offset. It should feel like a soft glow of light, not a dark stain.
*   **The "Ghost Border" Fallback:** For input fields or interactive elements where a boundary is critical, use the `outline-variant` token at **15% opacity**. This provides a "Ghost Border"—visible only when needed, maintaining the minimalist aesthetic.

## 5. Components: Precision Built

### Buttons
*   **Primary:** Solid `primary` background with `on-primary` text. Use `rounded-md` (0.375rem) for a professional, slightly sharp edge. No shadows; use a subtle `primary-container` glow on hover.
*   **Secondary:** `surface-container-lowest` with a 15% `outline-variant` Ghost Border.
*   **Tertiary:** Pure text with a 2px `primary` underline that expands on hover.

### Cards & Lists
*   **Prohibition:** Never use divider lines. 
*   **Layout:** Separate list items using `spacing-4` (1.4rem) of vertical white space. Use a `surface-container-low` background on the entire list container to group items together.

### Language Selector (TR/EN)
A minimalist, high-end component. Use `label-md` for the text. The active language should be indicated by a small `primary` dot (2px) underneath, rather than a bold font or a box. Place this in the top-right `surface-container-lowest` floating navigation bar.

### SAP Specialist "Tech Badge"
A custom component for highlighting SAP modules. Use `secondary-container` backgrounds with `on-secondary-container` text, applying `rounded-full` for a pill shape. These should be small (`label-sm`) and used sparingly to denote expertise.

## 6. Do's and Don'ts

### Do:
*   **Do** use asymmetrical layouts where text is left-aligned in a container that sits 20% off-center to the right.
*   **Do** leverage the `surface-bright` token for backgrounds behind high-resolution "tech-abstract" imagery.
*   **Do** ensure all financial data points use the `IBM Plex Sans` font for a calculator-precise feel.

### Don't:
*   **Don't** use high-contrast black (#000000). Always use `on-background` (#131B2E) for text to maintain a premium, deep-navy depth.
*   **Don't** use rounded-xl or rounded-full for main containers; keep the "Architectural" feel with `rounded-md` or `none`.
*   **Don't** clutter the screen. If a section feels busy, double the spacing token (e.g., move from `spacing-8` to `spacing-16`).