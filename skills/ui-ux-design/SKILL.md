---
name: ui-ux-design
description: Create a project-specific frontend UI and UX design guide in root THEME.md through repository inspection and a user interview. Use at the start of a project when the user wants to define or revise its visual direction before implementation.
---

# UI and UX Design Guide

Produce the current project's root `THEME.md` and link it from the project's root `AGENTS.md`.
This skill writes design instructions only: do not add UI code, new features, or functionality.

## Learn the project

Read the root `AGENTS.md` if present, along with the README, product or design docs, existing `THEME.md`, relevant UI code or mockups, dependencies, and other files that explain the product.
Identify the app type, target users, use cases, existing brand, technical stack, installed UI libraries, and any visual decisions already made.
Preserve established choices unless the user asks to change them.
Do not assume a theme from the framework or from generic design trends.

## Interview

Ask only about important choices the repository cannot answer, in small groups, and wait for replies.
Learn the intended mood, brand personality, accessibility needs, light or dark mode expectations, preferred or forbidden colors, typography preferences, and any reference products or visuals.
Offer these visual directions as choices, briefly explaining each in plain language: skeuomorphism, neomorphism, glassmorphism, claymorphism, minimalism, maximalism, brutalism, and liquid glass.
Help the user choose **one primary direction** for the entire product.
Ask how much motion feels appropriate and which screens or interactions matter most.
If the user has no preference, propose a direction grounded in the product and ask them to confirm it.

## Write `THEME.md`

Turn the decisions into specific, usable instructions, not a list of adjectives.
Include:

- Product context, target users, chosen visual direction, and intended mood.
- One coherent theme with concrete design principles and rules for layout, hierarchy, spacing, surfaces, corners, depth, and imagery or icons where relevant.
- A named color palette with exact values and roles for background, surfaces, text, accents, states, and interactive elements, including contrast guidance.
- Specific font families and fallbacks for headings and body text, plus type hierarchy and weight guidance.
- Motion guidance for transitions, feedback, and reduced-motion preferences.
- A single, concrete UI library appropriate for the project's stack, or an explicit decision to use no library, with a short reason.
- Design rules for existing product elements only; do not invent features or screens.

Keep these avoidances explicit and adapt them to the selected direction:

- Do not turn every item into a generic card grid.
- Do not leave meaningful interactions without feedback or motion; respect reduced-motion settings.
- Do not default to a plain purple-tinted background.
- Avoid em dashes in interface copy.
- Avoid colored card outlines and uniform single-color borders on cards; use spacing, surface contrast, or depth where separation is needed.
- Do not mix unrelated visual styles across the product.

If `THEME.md` already exists, update it carefully rather than discarding useful project decisions.
Show the proposed direction to the user before writing when its core choices remain uncertain.

## Link from local instructions

Create or update only the **current project root** `AGENTS.md` with these instructions, preserving its existing content:

```md
- For frontend UI and UX work, read and follow the project-root `THEME.md`.
- Notify the user before modifying this `AGENTS.md` file.
```

Do not edit global or home-directory agent instructions.
Use `THEME.md` consistently as the filename and reference.
