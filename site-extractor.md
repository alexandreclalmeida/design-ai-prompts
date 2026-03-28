# Design System Extractor from HTML Websites

## Overview

You are a **Design System Showcase Builder**.

You are given a reference website HTML:
[INDEX PAGE]

Your task is to create **one new intermediate HTML file** that acts as a **living design system + pattern library** for this exact design.

## Goal

Generate one single file called `design-system.html` and place it in the same folder of the HTML file.

This file must preserve the **exact look & behavior** of the reference design by reusing:

- HTML structure
- CSS classes
- Animations
- Keyframes
- Transitions
- Effects
- Layout patterns

**No approximations allowed.**

## Hard Rules (Non-Negotiable)

1. Do not redesign or invent new styles
2. Reuse exact class names, animations, timing, easing, hover/focus states
3. Reference the same CSS/JS assets used by the original
4. If a style/component is not used in the reference HTML, do not add it
5. The file must be self-explanatory by structure (sections = documentation)
6. Include a top horizontal nav with anchor links to each section

## Objective

Build a single page composed of canonical examples of the design system, organized in sections.

## 0. Hero (Exact Clone, Text Adapted)

The first section **MUST** be a direct clone of the original Hero.

### Requirements

- Same HTML structure
- Same class names
- Same layout
- Same images and components
- Same animations and interactions
- Same buttons and background
- Same UI components (if any)

### Allowed Change (only this)

- Replace the hero text content to present the Design System
- Keep similar text length and hierarchy

### Forbidden

- Do not change layout, spacing, alignment, or animations
- Do not add or remove elements

## 1. Typography

Create a Typography section rendered as a **spec table / vertical list**.

### Each row must contain:

- Style name (e.g. “Heading 1”, “Bold M”)
- Live text preview using the exact original HTML element and CSS classes
- Font size / line-height label aligned right
  - Format: `40px / 48px`

### Include ONLY styles that exist in the reference HTML, in this order:

- Heading 1
- Heading 2
- Heading 3
- Heading 4
- Bold L / Bold M / Bold S
- Paragraph (larger body, if exists)
- Regular L / Regular M / Regular S

### Rules

- No inline styles
- No normalization
- Typography, colors, spacing, and gradients MUST come from original CSS
- If a style uses gradient text, show it exactly the same
- If a style does not exist, do NOT include it

**Goal:** Communicate hierarchy, scale, and rhythm at a glance.

## 2. Colors & Surfaces

Include:

- Backgrounds (page, section, card, glass/blur if exists)
- Borders, dividers, overlays
- Gradients (as swatches + usage context)

## 3. UI Components

Include only components that exist in the reference:

- Buttons
- Inputs
- Cards
- Others (if present)

### Requirements

- Show states side-by-side:
  - Default
  - Hover
  - Active
  - Focus
  - Disabled

- Inputs only if present:
  - Default
  - Focus
  - Error (if applicable)

## 4. Layout & Spacing

Show:

- Containers
- Grids
- Columns
- Section paddings

### Include 2–3 real layout patterns:

- Hero layout
- Grid layout
- Split layout

## 5. Motion & Interaction

Show all motion behaviors present:

- Entrance animations (if any)
- Hover lifts / glows
- Button hover transitions
- Scroll / reveal behavior (only if present)

### Requirement

Include a **Motion Gallery** demonstrating each animation class.

## 6. Icons

If the reference uses icons:

- Display the same icon style/system
- Show size variants
- Show color inheritance
- Use the same markup and classes

If icons are not present:

- Omit this section entirely
