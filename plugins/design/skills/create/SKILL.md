---
name: create
description: UI design assistant for building interfaces from scratch. Applies foundational craft principles — typography, layout, color, style, imagery, elements, and tactics — to produce beautiful, functional designs. Triggered when the user wants to design, build, or scaffold a UI, screen, flow, component, or interface (e.g. "design a settings screen", "make a UI for X", "help me design Y"), or asks craft-level questions about typography, layout, color, spacing, hierarchy, or contrast in a forward-direction (no design exists yet).
---

# Create — UI Design Craft

A reference-driven assistant for designing UIs from scratch. Walks the user from brief to finished design using a structured set of craft principles.

This skill is reference-heavy. The principles live in `references/*.md` — load them on demand, not all at once. The body of this skill tells Claude when to load which reference.

If the user is asking for feedback on an *existing* design, use the sibling `critique` skill instead.

## Workflow

### 1. Understand the brief

Before any visual decision, get the brief straight. Use `AskUserQuestion` to batch:

- **What's being designed?** A screen, a flow, a component, a system, a page.
- **For whom?** The audience shapes density, formality, vocabulary, color palette.
- **What platform?** Mobile, desktop, responsive web, native app. Each has different conventions and constraints.
- **What's the goal?** What should the user think, feel, or do after seeing this?
- **What tasks must succeed?** Concrete user tasks the design has to enable — these are the bar usability is measured against. Load `references/usability.md` for the framing (learnability, efficiency, memorability, errors, satisfaction; utility vs. usability).
- **Constraints?** Existing design system, brand, technology, accessibility requirements.

Skip questions whose answer is already clear from context. But never skip "for whom" and "what tasks must succeed" — they anchor everything that follows.

### 2. Foundation pass

Design in this order. Each layer constrains the next.

1. **Typography** — load `references/typography.md`. Pick font sizes (aim for ≤4), weights, hierarchy. Most decisions here cascade through everything else.
2. **Layout** — load `references/layout.md`. Define grid, box model, negative space, alignment. Choose density (tight, medium, generous).
3. **Color** — load `references/color.md`. Pick base hue, derive structural vs. interactive colors, define a grey scale, set contrast ratios.
4. **Style** — load `references/style.md`. Decide on corner radius, borders/dividers, depth (shadow/lighting/blur), and overall design direction (e.g. minimal, expressive, dense, friendly).
5. **Imagery** — load `references/imagery.md`. Plan icons, photos, illustrations, and how dynamic content will fit.

Don't load every reference upfront. Load the ones the current task touches. Reading a 30 KB reference into context to design a single button is wasteful.

### 3. Elements pass

Load `references/elements.md` for specific component guidance: navigation, user input, forms, profile, settings, cards. Apply per element.

### 4. Tactics pass

For complex projects, load `references/tactics.md` — covers low-fidelity wireframing, iOS conventions, prototyping, and design system thinking.

### 5. Self-critique pass

Run through `references/ui-checklist.md` on the design you produced. Be honest — name the weak points. Loop back to fix.

### 6. Usability pass

Re-load `references/usability.md` and stress-test the design against the 5 quality components — learnability, efficiency, memorability, errors, satisfaction — plus utility. For each of the user tasks named in the brief: walk through it step by step. Where does the user have to think? Where could they slip? Where would a returning user lose the thread? Note specific friction points.

### 7. Accessibility pass

Run through `references/accessibility-checklist.md`. Color contrast, label clarity, keyboard navigation, screen-reader semantics, and media alt text are non-negotiable. Flag anything below WCAG 2.1 AA.

### 8. Hand-off

A finished design that doesn't reach the developer or stakeholder is a half-finished design. Ask where it's going (Figma, Notion, code, slide deck), and help with the last mile — formatting, exporting, or describing the design so it can be implemented.

## Reference index

| Reference | When to load |
|---|---|
| `references/typography.md` | Font sizing, weights, hierarchy, line height, case, type pairing, system vs. alternate fonts |
| `references/layout.md` | Grids, box model, negative space, alignment, density, layout anchors, optical vs. mathematical alignment |
| `references/color.md` | Color systems, structural vs. interactive color, primary/secondary/tertiary, gradients, grey scales, dark UI |
| `references/style.md` | Design direction, corner radius, borders & dividers, depth/lighting/shadow, opacity & blur |
| `references/imagery.md` | Icons, static and dynamic images, blend modes, illustrations, app icons |
| `references/elements.md` | Navigation, user input, forms, profile, settings, cards, lists |
| `references/tactics.md` | Design experiments, lo-fidelity wireframes, iOS conventions, prototyping, design systems, hand-off |
| `references/usability.md` | Usability framing for the brief + usability stress-test before sign-off (5 quality components, utility vs. usability, when/how to test with real users) |
| `references/ui-checklist.md` | Visual-craft self-critique before sign-off |
| `references/accessibility-checklist.md` | Accessibility review before sign-off |

## Core principles (always apply)

These are the load-bearing ideas across the references. Keep them in mind even when the matching reference isn't loaded.

1. **Constraint beats choice.** A small palette of font sizes, weights, and colors produces a cleaner interface than wide variety. Aim for ≤4 font sizes per screen, a defined color system, and a single design direction.
2. **Hierarchy follows attention.** The most important element should be the most visually weighted — through size, weight, color, position, or negative space. If everything is loud, nothing is loud.
3. **Negative space is a tool.** Empty space defines relationships and creates rhythm. Tight spacing means "these go together." Generous spacing means "these are separate."
4. **Alignment is non-negotiable.** Every element should align to something else — left edge, baseline, grid line, optical center. Drift breaks the illusion of intentionality.
5. **Color does work.** Each color in the palette should have a defined role (structural, interactive, semantic). Random color choices erode trust.
6. **Form serves function.** Beauty without usability is decoration. Usability without beauty is unfinished. The best interfaces do both.
7. **Usability is measurable.** Five components: learnability, efficiency, memorability, errors, satisfaction — plus utility (does it do what users need?). Design choices should make each one better, not worse.
8. **Design for the real user.** Empty states, error states, long content, missing content, slow connections, dark mode, small screens, screen readers. Edge cases are where the design either holds up or breaks.
9. **Trust what users do, not what they say.** Observation beats opinion. When in doubt, the answer is to put the design in front of 5 real users and watch.

## Anti-patterns

- Don't load every reference upfront — it bloats context and slows responses. Load on demand.
- Don't skip the brief. A design without an audience is a design problem in disguise.
- Don't apply principles mechanically. Rules are scaffolding — break them when there's a reason, but know why.
- Don't ship without the self-critique and accessibility passes.
- Don't forget hand-off. A finished design that doesn't reach the developer or stakeholder is a half-finished design.
