# Visual Direction — "Sage"

The chosen visual identity for the caregiver cooking app. Working name **Sage** (herb + wisdom/memory + the green). This document is the design north star; the interactive style tile and the wireframes are built against it.

## Concept, in one line

**"Someone remembers, so you don't have to."** A cooking companion that quietly carries a whole household's food rules, and treats everyone in it (the person cooking and the person being fed) as a whole human, not a chart of restrictions.

## Who we design for, and the market gap

- **The buyer and daily user is the caregiver**, not the patient. Skews 30s to 50s, chronically depleted, and judges the app "in one tired evening with dirty hands." The stakes are medical (a wrong plate can hospitalize someone), but the user is emotionally spent and quietly guilty, not a data analyst.
- **The central tension the visuals must hold:** trustworthy enough to bet a kidney patient's health on, and warm enough that an exhausted person feels held, not audited.
- **The white space.** Generic recipe apps are busy and appetite-baiting; clinical and tracker apps are cold and spreadsheety. Nobody designs for the caregiver's exhaustion. The ownable position is *calm, human, reassuring*, an app that visibly takes care of the person doing the caring.

## The feeling: warmth and dignity

The one feeling everything answers to is **warmth and dignity**. Five rules keep it honest; every screen has to pass them.

1. **People before conditions.** You care for *Dad*, with his name and a look he chose. The kidney rules are quiet metadata behind a whole person, never the headline.
2. **Reassurance before restriction.** Lead with what works and what is safe. The first thing you feel is relief, not a red wall of forbidden foods.
3. **The cook is competent.** No nagging, no guilt, no broken streaks. It quietly confirms the care is happening and stays on your side.
4. **Red is rationed and calm.** A wrong-plate warning is a hand on your arm, not a hospital monitor. Warm clay, never fire-engine red.
5. **Plain human language.** "His kidneys can't clear the potassium", never a phosphorus table. Explained the way you would tell a friend.

## The direction: Safe Hands bones, Quiet Kitchen skin

Trustworthy clinical-calm structure (the safety system is the hero UI element) wearing warm, homey skin. Illustration-led, so the warmth is carried by drawing rather than photography; a warm drawn world sidesteps stocky photos of sick relatives and keeps everyone rendered gently and consistently.

## Color

Green leads, because green is the app's soul: safe, calm, growing, *he's okay*. It sits on a warm, faintly green-biased ground rather than the usual cream. Terracotta is a small warmth accent, not the star. The safety colors are semantic and always carry an icon and a word.

| Role | Hex | Use |
|---|---|---|
| Garden sage | `#5E8C6A` | Primary accent, brand, "safe" |
| Deep herb | `#2C4534` | Headings, brand ink |
| Terracotta | `#CE7A57` | Warmth accent, sparing |
| Warm putty | `#EBE7DB` | Ground, green-biased |
| Ivory | `#F6F3EA` | Cards, surfaces |
| Warm ink | `#242017` | Body text |
| Ink soft / taupe | `#57513F` / `#8A8072` | Secondary text, captions |

**Safety traffic-light (warm-tuned, always with a word and an icon):**

- Safe or confirmed: `#5E8C6A` (check)
- Modify or flare: `#D8952F` (tilde)
- Avoid or alert: `#BE5843` (cross), clay, calm not alarming

**Warm dark mode** for real midnight cooking: a deep warm charcoal ground, not cold black; sage and terracotta carry through.

## Typography

Two voices, the hybrid made literal.

- **Reassurance serif** (the human voice, headings, "Dad ate lunch. He's okay."). Production intent **Fraunces**, old-style, warm, optical. Never used for dense UI.
- **Working sans** (the functional layer: safety chips, buttons, split instructions, where clarity is the trust). Candidates **Figtree** or **Inter** / a humanist grotesk. The ui-ux-pro-max engine flagged Figtree + Noto Sans as "medical, clean, accessible, trustworthy", which fits the functional layer. Large sizes, high legibility, tired-eye and one-handed friendly.

## Illustration language

- A rounded, gentle, two-color line world; deep herb strokes with sage and clay fills. Food stays appetising and people stay dignified without ever looking clinical or stocky.
- **Rules:** 2.2px rounded strokes in deep herb; two fills only, sage and clay; soft, slightly imperfect shapes; nothing outlined in red; people drawn with warmth and never reduced to their diagnosis.
- Photos are optional, never required. People are represented by a chosen color or a pre-offered illustration. **The one photograph in the whole app is the carer's plate**, because there realism earns its place as proof.

## Voice

Plain, calm, second person, always about the person and never the chart. No hedging, 8th-grade reading level.

- **Sounds like us:** "This one's safe for both of them." / "Dad ate lunch. He's okay." / "Hold the salt for dad, add an egg for Iryna."
- **Never this:** "Meal compliant with Profile 2 restrictions." / "Patient 2: intake logged 13:10." / "Warning: potassium threshold exceeded."

## Signature moments to design first

- **"Whose plate?"** A dish with each eater's dot (sage / honey / clay) and one plain-language reason. The trust-earning hero.
- **"Tonight."** One warm illustration, one meal, the per-person split underneath. Cook once, decide once.
- **The daily breath.** "Dad ate lunch. He's okay.", with the carer's plate photo. The emotional peak, and the whole reason someone keeps the app.

## Design intelligence behind the choices (ui-ux-pro-max, impeccable, taste)

- **Product register.** The app is *Recipe & Cooking* (warm food tones) crossed with *Medication reminder / caregiver health* (Accessible & Ethical + Trust & Authority; green = safe, red = alert; calm). We **deliberately reject** the generic recipe-app default of vibrant claymorphism, "no muted colors", and purple-gradient buttons; that playful children's-app energy is wrong for a medical, dignity-led product. This is exactly why the palette is muted and green-led, not bright.
- **Craft bar.** WCAG 2.1 AA, contrast verified not eyeballed, visible focus, reduced-motion respected, purposeful restraint (every element earns its place).
- **Anti-slop dials.** Low density (one thing per screen), low motion (calm, no bounce), structured variance (a utility health app, not an experimental site). Hard em-dash ban in all UI copy.

## Relationship to the research deck

The research and strategy artifacts use a separate light editorial system (documented in `Research-Visualization-Design-Style.md`): warm light-gray canvas, bold grotesk headlines, olive as the structural accent, peach/yellow/olive topic cards. That system is for the *case-study presentation*. **Sage is the product's own identity**: warmer, greener, quieter, and built around the safety-dot system and the reassurance voice. The two share DNA (warmth, green, human) but serve different jobs.

## Deliverables and next steps

- **Style tile (built):** the interactive board covering palette, type, the safety-dot system, illustration set, component mocks, and voice.
- **Wireframes (in progress):** low-fi phone screens in a muted green tonal skin (see `Wireframes-Plan.md`).
- **Next:** hi-fi of the hero "Whose plate?" screen and the daily-reassurance moment, then extend the illustration set.
