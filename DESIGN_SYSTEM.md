# Kevin Keithley — Design System

This document records the shared visual and editorial system for
`kevinkeithley.github.io` and the public résumé. It is the reference for future
site pages, résumé variants, project descriptions, and related professional
materials.

## Design direction

The system should feel:

- analytical without looking clinical;
- warm without becoming decorative;
- multidisciplinary without appearing unfocused;
- confident, direct, and grounded in real work;
- modern, readable, and intentionally restrained.

The core visual contrast is warm paper, near-black charcoal, and a muted orange
accent. Large, tightly set headings provide personality; generous whitespace and
plain typography keep the content credible.

## Color system

### Core tokens

| Token | Value | Primary use |
| --- | --- | --- |
| `paper` | `#FFFDF9` | Main cards, page surfaces, résumé background |
| `canvas` | `#F4F1EB` | Website page background |
| `charcoal` | `#292722` | Strong text, dark project cards, major rules |
| `ink` | `#252525` | Default body text |
| `orange` | `#C76A12` | Résumé headings and primary accent |
| `orange-border` | `#D88728` | Portrait border and card-top rules |
| `orange-link` | `#9A4F00` | Links on light surfaces |
| `orange-label` | `#A85800` | Eyebrows and small uppercase labels |
| `orange-on-dark` | `#F0AD61` | Links on charcoal surfaces |
| `muted` | `#5D574F` | Secondary text |
| `muted-copy` | `#58534B` | Homepage supporting copy |
| `line` | `#D7D0C4` | Borders and major dividers |
| `line-soft` | `#E2DDD4` | Secondary dividers |
| `sand` | `#EFE9DF` | Light feature and principle cards |

### Usage rules

- Orange is an accent, not a background theme. Use it for section labels,
  borders, and links rather than large blocks.
- Use `charcoal` rather than pure black to keep the system warm.
- Use `paper` rather than pure white for primary surfaces.
- On dark cards, body copy should use a warm light gray such as `#DED9D0`.
- Do not introduce additional bright brand colors without a specific semantic
  need.

## Typography

### Website

The website uses a system sans-serif stack for interface text and headings:

```css
font-family: Inter, ui-sans-serif, system-ui, -apple-system,
  BlinkMacSystemFont, "Segoe UI", sans-serif;
```

Long-form About copy uses a serif stack to distinguish reflective narrative
from interface and project content:

```css
font-family: Georgia, "Times New Roman", serif;
```

### Résumé

The résumé uses embedded DejaVu Sans and DejaVu Sans Bold. Embedding the fonts
produces consistent rendering while keeping text selectable and extractable by
applicant-tracking systems.

### Type roles

| Role | Treatment |
| --- | --- |
| Display name | Bold sans serif, very large, tight tracking (`-0.055em` to `-0.065em`) |
| Page title | Bold sans serif, fluid size, compact line height (`0.92`–`0.98`) |
| Eyebrow | Uppercase, bold, orange, `0.12em`–`0.14em` tracking |
| Section heading | Uppercase or compact bold sans serif, orange accent |
| Lead copy | Larger sans serif, muted charcoal, relaxed line height |
| Narrative copy | Serif, approximately `1.18rem`, `1.85` line height |
| Interface/link text | Sans serif, medium-to-bold weight |

Avoid excessive weight changes. Hierarchy should come primarily from size,
spacing, and color.

## Spacing and layout

The website uses responsive spacing through `clamp()` rather than a rigid pixel
scale. When new components need fixed spacing, prefer this approximate scale:

| Step | Value | Typical use |
| --- | --- | --- |
| `xs` | `0.5rem` | Label gaps, tight inline spacing |
| `sm` | `1rem` | Card gaps, compact padding |
| `md` | `1.4rem`–`1.5rem` | Standard card padding |
| `lg` | `2rem`–`2.25rem` | Section/card padding |
| `xl` | `3rem`–`3.5rem` | Section separation |
| `2xl` | `4rem`–`5.5rem` | Hero and wide-screen page padding |

### Widths

- Homepage card: maximum `900px`.
- About page: maximum `880px`.
- Lead paragraph: maximum `730px`.
- Homepage body copy: maximum `34rem`.
- Résumé: US Letter, portrait, two pages for the master version.

### Grid behavior

- Homepage desktop: portrait/sidebar plus main content.
- Project section desktop: featured project at `1.35fr`, secondary project at
  `1fr`.
- Principles desktop: three equal columns.
- At `700px` and below, all major grids collapse to a single column.

## Components

### Homepage identity card

- Warm paper surface on the canvas background.
- `20px` outer radius and a soft, large shadow.
- Charcoal portrait panel with a `4px` orange portrait border.
- Large name, one short positioning statement, and three labeled professional
  links.

### Project card

- Charcoal surface with warm-white title text.
- Muted light body copy.
- Small orange uppercase project-type label.
- Featured cards receive a `4px` orange top border.
- Links use the lighter `orange-on-dark` token.

### Principle card

- Sand surface with a `3px` orange top border.
- Compact title and short explanation.
- Avoid icons unless they add information.

### Navigation and footer

- Text links rather than button-like chrome.
- Links are normally unadorned and receive an underline on hover.
- Dividers use the `line` token.

### Résumé

- Single-column document structure for reliable text extraction.
- Orange section labels, charcoal headings, and no sidebars or skill meters.
- Work history occupies page one; projects, education, and skills occupy page
  two in the master version.
- Targeted versions may be reduced to one page by selecting relevant material,
  not by shrinking type below comfortable reading size.
- Internal labels such as “general résumé” never appear in an employer-facing
  file.

## Interaction and responsive rules

- Preserve visible keyboard focus; never remove outlines without a clear
  replacement.
- Hover behavior should be subtle: underline links or slightly raise a card.
- Do not make essential information available only on hover.
- Keep touch targets comfortably sized and avoid icon-only links without an
  accessible label.
- Navigation and footers may wrap or stack on narrow screens.

## Accessibility

- Use semantic landmarks: `main`, `nav`, `section`, `article`, `header`, and
  `footer`.
- Maintain one `h1` per page and a logical heading hierarchy.
- Decorative images use empty alt text; meaningful images receive concise alt
  text.
- Link purpose must be understandable without relying on an icon.
- Preserve strong contrast between text and its background.
- The résumé must remain selectable, searchable, and readable when converted to
  plain text.

## Editorial voice

The writing system is as important as the visual system.

### Use

- concrete descriptions of work performed;
- specific systems, tools, constraints, and outcomes;
- plain language that connects analysis to practice;
- first person on the website and concise action language on the résumé;
- measured confidence supported by evidence.

### Avoid

- generic corporate filler such as “results-driven,” “customer-centric,” or
  “strategic priorities” without supporting detail;
- treating Kevin’s careers as unrelated identities;
- inflating informal job titles;
- claiming a theory or project is finalized while it is still evolving;
- decorative complexity that competes with the content.

### Central narrative

Kevin works across disciplines to understand complicated systems, identify what
is actually limiting them, and build useful improvements. The IMF, data science,
restaurant operations, structural integration, KitchenPi, and Self-Taught
Scholar should be presented as evidence of that same working method.

## Implementation notes

- Canonical current website styles begin under `/* Current portfolio styles */`
  in `css/main.css`.
- When the stylesheet is next refactored, move the core color and spacing values
  into CSS custom properties matching the tokens in this document.
- Review this file whenever a new page, project card, résumé variant, or major
  visual component is added.
