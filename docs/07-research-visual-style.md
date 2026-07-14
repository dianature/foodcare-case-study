# Research Visualization Design Style

The visual system for every artifact in this project: the ideation mind map, the competitor and positioning maps, the persona and quote cards, the feature slide, the pain-point and feature maps, and the user-flow and journey diagrams. It keeps every artifact reading as one family. The **produced deck is the source of truth**: `Visual/Slide 1 — Quotes.png`, `Visual/Slide 2 — Features.png`, `Visual/Big Map.png`, `Visual/Ideation Map.png`, and the caregiver `User flow` frame reflect the reconciled system. Treat the hex values below as the working tokens and the produced frames as the final look. An earlier draft of this doc proposed a pastel blush-and-mint palette with serif titles and a dark indigo mode. That direction was superseded. The system below is what actually shipped.

The style is a clean, warm, editorial light system. One near-white canvas, bold black headlines, a single olive-green structural accent, and a small set of pastel node fills doing the color work.

## Principles

1. Warm and human, not clinical. The work is about people cooking for people they love, so the surfaces stay soft and approachable.
2. One idea per view. Each artifact carries a single argument, everything else supports it.
3. Specific over decorative. A named persona, a real quote, a concrete number earns its place. Ornament does not.
4. Quiet warm canvas, one accent. A calm off-white ground lets olive and a few pastel fills do the pointing.
5. Meaning never rides on color alone. Every color pairing also carries a label, an icon, a number, or a position, so the view survives grayscale and colorblindness.
6. A little handwriting. Sparing Caveat margin notes add warmth and a human voice, the way a designer annotates a printout.

## Color

One light mode across the whole system. There is no separate dark mode. Dark appears only as near-black anchor elements (hub nodes, start and end nodes) and as the page surround the light slide floats on.

### Core

| Role | Hex | Use |
|---|---|---|
| Canvas | `#EDECE6` | Slide and map background, warm light gray |
| Surface | `#FFFFFF` | Pills, quote cards, legend, category labels |
| Page surround | `#141414` | Near-black backing the floating light slide sits on |
| Ink | `#111111` | Headlines and primary text |
| Body | `#3A3A3A` | Node body copy, secondary sentences |
| Muted | `#8C8C86` | Eyebrows, captions, the trailing half of a two-tone intro |

### Accent (structural)

| Role | Hex | Use |
|---|---|---|
| Olive | `#7C8B2E` | The single structural accent. Connector lines, node dots, tag-pill outlines, the bold "Who" and "Problem" labels, handwritten notes |
| Olive deep | `#5E6B22` | Emphasis and hover state of the accent |

### Node fills (topic and feature color-coding)

Pulled from the Features slide. Reuse the same three fills to color-code feature or topic nodes, and reuse them across slides so a node reads as the same feature wherever it appears.

| Role | Hex | Use |
|---|---|---|
| Peach | `#F5D8BE` | Feature group A (cook and shop: features 01, 04) |
| Pale yellow | `#F6EFC7` | Feature group B (understand and check: features 02, 05) |
| Olive green | `#A9BD4F` | Feature group C (state and hand-off: features 03, 06) |
| Pale green | `#E1EAC4` | Map bubble cards, shaded actor bands |

### Anchor

| Role | Hex | Use |
|---|---|---|
| Black node | `#141414` | Central hub, start and end nodes. Always with `#FFFFFF` text |

### Status ramp (severity, priority, and the diet traffic-light)

Warm traffic-light, kept in the deck's tonal range. Always pair the color with a word and an icon, never hue alone.

- Safe or confirmed: `#4E9A80`, tint `#DBEDE1`, icon check.
- Modify or flare: `#D2924A`, tint `#F6EFC7`, icon tilde.
- Alert or refused: `#C26E66`, tint `#F2E2DF`, icon cross.
- Priority ramp low to high: `#E1EAC4`, `#D2924A`, `#C26E66`. Pair with a P1, P2, P3 label.

### Persona palette (categorical, colorblind-aware)

Each persona keeps one ring color everywhere they appear, on the avatar and on any card accent bar. Use in this order so the first personas carry the most separable colors.

| # | Name | Hex |
|---|---|---|
| 1 | Orange | `#E8722A` |
| 2 | Amber | `#E6B93E` |
| 3 | Olive | `#A9BD4F` |
| 4 | Moss | `#6E8B3E` |
| 5 | Forest | `#2E4A1E` |
| 6 | Slate | `#A7ABA0` |

Orange `#E8722A` doubles as the one sparing hero accent, as on the Quotes slide title. Use it once per view at most.

## Typography

Three roles, plus handwriting. The produced deck uses a **bold grotesk sans for display, not a serif**. Reconcile the exact family with Diana's brand; Inter is the working default and every weight below is available.

- Display headline. A heavy grotesk sans. Inter Black or Extra Bold, size 64 to 88, tight tracking around minus 1 to minus 2 percent. Sentence case for section titles ("User flow", "Main features"); uppercase is reserved for a hero variant ("IN THEIR OWN WORDS").
- Section and node title. Inter Semi Bold, 17 to 20, ink.
- Body and caption. Inter Regular or Medium, 13 to 16, line height about 148 percent. In map bubbles the "Who" and "Problem" run-in labels are Semi Bold in olive `#7C8B2E`.
- Eyebrow and phase marker. Inter Semi Bold, 13 to 15, uppercase, letter-spacing 6 to 12 percent, muted gray. The eyebrow is prefixed with a section number, for example `(06) THE APP`, and a phase word sits top-right of the same row, for example `DEFINE`, `IDEATE`, `SELECTION`, `PROTOTYPE`.
- Handwriting annotation. Caveat, 20 to 26, olive, for margin notes and pointer labels. Echoes the Big Map.
- Numbers use tabular figures so columns and metric tiles align.

Suggested scale (px): 82 display, 32 section title, 18 node title, 16 body, 13 caption, 13 eyebrow, 24 handwriting.

## Layout and spacing

- Slide format. 1920 by 1080 landscape. Content sits on a large rounded rectangle, radius about 28, floating on the near-black page surround.
- Map format. Large custom canvas, hub-and-spoke or centered, from roughly 2300 by 1800 up to 3300 by 3120.
- Flow and journey format. A spine, vertical for long flows or horizontal to sit as a slide. The caregiver user flow is portrait.
- Spacing scale, 8px base: 4, 8, 16, 24, 32, 48, 64. Keep to it.
- Generous whitespace. Let cards and nodes breathe.
- Corner radius: slide container 28, cards 14 to 16, pills and tags fully rounded, number chips full circles.
- Header zone. Eyebrow left and phase word right on one row, then the big display title, then optional tag-pills, then a two-tone intro sentence, ink for the first clause and muted for the trailing clause.
- Connectors. 1.5 to 2px olive. Radial lines with a small origin dot in maps. Orthogonal elbows with a small chevron arrowhead in flows. Hand-drawn curved Caveat-style arrows from a margin note to its target.

## Core components

- Slide frame. Light `#EDECE6` rounded container on the near-black page, with the eyebrow-and-phase header at the top.
- Feature card. Pastel fill (peach, pale yellow, or olive green), a small dark number chip, a bold black title, a small up-right arrow in the corner, and gray body copy. This is the Features slide card.
- Category or step pill. White surface, a small olive dot on the left, a bold black label, a soft low-opacity shadow. This is the Ideation-map label and the flow's screen step.
- Decision node. White pill with a 1.5px olive outline and a small olive triangle, label ends with a question mark.
- Status chip. Tinted fill from the status ramp, a small colored dot, a bold label, and an icon (check, tilde, cross).
- Hub or anchor node. Near-black rounded rectangle, white text. The map center, or a flow's start and end.
- Bubble card (maps). Pale-green fill, bold black title, a "Who" and "Problem" body with olive run-in labels.
- Persona avatar. Circular photo inside a colored ring in the persona's assigned color, often with a handwritten note and a curved pointer arrow.
- Tag pill. Fully rounded, olive outline, olive label. Used for section tags like "solution" or "core features".
- Shaded actor band. Pale-green rounded rectangle behind a group of steps that belong to one actor, with a small uppercase label such as `CARER`.
- Number chip. Small dark translucent circle with a dark number, for feature and card ordering (01 to 06).

## Applying the style to each view

### Ideation mind map
Central near-black hub with white uppercase title. Radial olive connectors with a small origin dot. Direction labels as white pills with an olive dot. Each idea as a pale-green bubble card with a "Who" and "Problem" body. Faint concentric rings behind the hub. Handwritten Caveat notes in the margins with curved pointer arrows to the persona avatars.

### Competitor and positioning maps
Two-by-two or table on the warm canvas. Axis and header labels in muted uppercase, letter-spaced. Plot points or rows in the persona and node colors. Mark the white-space quadrant or the key gap with a soft pale-green fill and one short caption. Do not fill every quadrant.

### Persona and quote cards
White card, generous radius. A circular photo in the persona's ring color. A bold black quote, then the muted Russian and the muted English rendering, then a name and one-line role. One persona, one card, one ring color. The section title can take the sparing orange hero accent.

### Feature slide
Three-column grid of pastel cards, peach and pale yellow and olive green grouped by feature family. Each card carries a number chip, a bold title, an up-right arrow, and gray body copy.

### Pain-point and feature maps
Rank pains with the priority ramp and a P1 to Pn label. Each pain is a card with its severity swatch, a one-line statement, and its supporting quote. Draw a thin olive connector from each pain to the feature that addresses it, so the "kills P1, P2" mapping is visible.

### User flow and journey maps
Warm canvas, same header system as the slides, `(NN) SECTION` left and a phase word such as `PROTOTYPE` right. A spine of nodes. Near-black start and end nodes with white text. White step pills with an olive dot and an optional muted caption to the side. Feature-carrying steps reuse the peach, yellow, and olive card fills and their 01 to 06 numbers, so the flow reads as the six features in motion. Decisions are white olive-outlined pills. Branch outcomes are status chips. Group an actor's steps inside a pale-green shaded band. Connectors are thin olive orthogonal elbows with small chevron arrowheads, and fork-and-merge routing for branches. Add one or two handwritten Caveat notes tying a step back to a real interview line.

### Bilingual quote callout
Quotes come in Russian first, then an English rendering. Style as a card. Russian in bold ink, English below in muted. A small attribution with the persona name and role. Keep one guillemet style, «», consistent with the transcripts. Do not stack decorative quotation marks.

## Iconography
Thin single-weight line icons where an icon is needed, and the small up-right arrow motif on cards. Number chips for ordering. Persona avatars with colored rings. Monochrome, sized on the 8px grid. No filled or multicolor icons, and no emoji as markers.

## Accessibility and export
- Contrast: body text at least 4.5 to 1 against its background, large text and UI at least 3 to 1. Black text passes on peach, pale yellow, and olive-green fills; white text passes on the black anchor nodes. Check the muted gray and olive on the warm canvas before shipping.
- Redundant encoding: pair every color with a label, an icon, a number, or a position. Nothing should read by hue alone. The status chips always carry a word and an icon.
- Source of truth: the produced deck frames and the caregiver user-flow frame. Name frames by artifact, for example `slide-features`, `slide-quotes`, `map-ideation`, `map-big`, `flow-user`.
- Export at 2x. PNG for slides and the submission, SVG where the vector will be edited again.

## Do and do not
- Do lead with one bold black headline and let the pastel cards carry the color.
- Do keep olive as the single structural accent for lines, dots, and tag outlines.
- Do color-code feature and topic nodes with the peach, yellow, and olive set, and reuse them across views.
- Do reuse each persona's ring color everywhere that persona appears.
- Do add sparing handwritten Caveat notes for warmth and voice.
- Do label the white space, the top pain, and the actor bands directly on the view.
- Do not use serif display type. The system uses a bold grotesk sans.
- Do not use the old indigo dark-editorial mode. The system is light throughout, with only near-black anchor nodes.
- Do not encode rank, safety, or actor with color only.
- Do not fill the whole canvas with color or crowd a map ring.
- Do not use em dashes, en dashes, or decorative emoji in any caption or label, in line with the project writing rules.
