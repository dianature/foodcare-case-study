# FoodCare — Full UI Design Spec & Generation Prompt
*Direction: "Calm Bento". Palette derived from `ui-ref-01` (green darkened). Working name FoodCare (placeholder).*

> **How to use this with Claude / Claude Design.** Paste this whole file as the brief. Ask Claude to build screens on the Figma `OLD` page via the Figma MCP (`use_figma`), reusing the tokens and components below. Build one screen per pass, screenshot, verify against the Guardrails, then continue. Food photos: `curl` Unsplash/Pexels to disk, then `upload_assets` onto the target photo node (`createImageAsync` from a URL is NOT supported in this environment). Icons: Phosphor (Regular) via the Iconify Figma plugin; the safety marks (check / tilde / cross) and person dots are custom-drawn so the word+icon+shape encoding stays exact.

---

## 1. Product & audience
FoodCare quietly carries a whole household's food rules so one cook can feed several diets from one base meal, safely. **"Someone remembers, so you don't have to."**
- **User = the caregiver**, 25–35, cooking for someone they care for (partner, parent, roommate, friend). Mobile-native, design-literate, emotionally spent, judged "in one tired evening with dirty hands."
- **Stakes are medical** (a wrong plate can hospitalize) but the tone is warm and reassuring, never clinical or gamified.
- **Ownable position:** calm, human, safety-first — between busy appetite-bait recipe apps and cold spreadsheet trackers.

## 2. Visual direction — "Calm Bento"
Soft, humanist, low-density. Light ground, near-black ink, one darkened lime-green accent, and appetizing food photography on recipe surfaces. Rounded bento modules, generous whitespace, gentle motion. **Design dials: variance 5, motion 3, density 3.**

## 3. Design tokens

### Color (semantic — never raw hex in components)
| Role | Hex | Use |
|---|---|---|
| `bg/canvas` | `#F4F5EF` | App background (near-white, faint green) |
| `bg/surface` | `#FFFFFF` | Cards, sheets |
| `bg/soft` | `#ECF0DE` | Hero tint, icon chips, illustration grounds |
| `text/ink` | `#191C17` | Headlines, primary text |
| `text/body` | `#696E64` | Body, secondary |
| `text/muted` | `#8A8F84` | Captions, section labels |
| `line` | `#E7E8E0` | Hairlines, dividers, light borders |
| `green/accent` | `#6F8A26` | Brand accent: icons, dots, illustration, small fills |
| `green/ink` | `#4F6417` | Green **text** on light (AA-safe) |
| `green/deep` | `#55671C` | Pressed / emphasis |
| `btn/dark` | `#1B1E17` | Primary CTA fill (near-black, ui-ref-01 style), white label + lime icon |

**Safety ramp (traffic-light, always word + icon + shape, never color alone):**
| State | Base | Text-on-tint | Tint bg | Icon / shape |
|---|---|---|---|---|
| SAFE | `#7B9A2E` | `#4F6417` | `#E9EFD5` | check / circle |
| MODIFY | `#E8B43C` | `#8A6410` | `#FBF1D2` | tilde / square |
| AVOID | `#E8705C` | `#A8463A` | `#F8DED7` | cross / triangle |

**Person dots (categorical identity, one color each, reused everywhere they appear):** You `#8C9182`, partner (Iryna) `#6F8A26`, parent (Dad) `#3F4A53`. Photo optional, never required.

### Typography — Manrope (one family, weight contrast)
- Screen title / H1: ExtraBold, 30, tracking -1%
- Section header: SemiBold 16–19
- Card / person title: Bold 14–19
- Body: Regular 13–15, line-height ~135%
- Label / caption: Medium 12–13
- Token label: SemiBold 11, uppercase, tracking +2%
- Numbers: Bold, tabular figures where columns align

### Spacing, radius, elevation
- Spacing scale (4/8): 4, 8, 12, 16, 20, 24, 32.
- Radius: card 18, stat tile 18, hero 26, pill/token/button-round 999, sheet top 26, phone 44, small 12. **One scale, applied consistently.**
- Elevation: flat by default; cards read via fill + 1px `line` border, not heavy shadows. If a shadow is used, tint it to the canvas hue, low opacity.
- Touch targets ≥ 44pt, ≥ 8px apart. Safe-area padding on fixed bars.

### Icons
Phosphor, **Regular** weight (≈2px stroke), 20–24px, one family throughout. Safety marks + person dots stay custom.

## 4. Core components
- **Status bar** — time + battery, ink on light.
- **Nav bar** — round back button (surface + `line`), screen title (SemiBold 16–17), optional round action button right.
- **Tab bar (caregiver)** — 4 tabs (Today, Cook, Shop, Care), icon + label, active tab in `green/accent`. Carer app has no tab bar.
- **Bento card / person card** — surface, radius 18, 1px `line`, padding 12–16. Never nested. Use only when grouping earns it; otherwise dividers/whitespace.
- **Hero module** — `bg/soft` card, radius 26, illustration-in-circle + title + person-dot row.
- **Stat tile** — surface pill card, icon-chip (`bg/soft`) + value (Bold) + label (Medium).
- **Safety token** — tinted pill, custom shape-icon + uppercase word, per the safety ramp.
- **Buttons** — Primary: `btn/dark` fill, white label, lime icon, radius 16. Secondary: surface + `green/accent` 1.5px border, `green/ink` label. One primary CTA per screen, thumb-zone.
- **Ingredient stepper** (from ui-ref-07) — label + `–  value  +` with round steppers, for shopping/quantities.
- **Chips / filters** — pill, `line` border; selected = `bg/soft` fill + `green/accent` dot; person filters carry the person dot.
- **Toggle** — 46×28 track, `green/accent` when on.
- **Photo frame** — rounded, `clipsContent`, image FILL; food photography only.
- **Illustration frame** — rounded 2-color line world in `green/accent` on `bg/soft`, for people, empty states, the daily breath.
- **States** — every list/data view ships loading (skeleton, not spinner), empty (message + action), error (inline + retry), success (brief confirm).

## 5. Voice & copy
Plain, calm, second person, about the person never the chart. 8th-grade reading level, no hedging.
- Sounds like: "This one's safe for both of them." · "Dad ate lunch. He's okay." · "Hold the salt for dad, add an egg for Iryna."
- Never: "Meal compliant with Profile 2 restrictions." · "Potassium threshold exceeded."
- Buttons = verb + object ("Start cooking", "Add to shopping list", "Send invite").
- **No em dashes** anywhere in UI copy. No marketing buzzwords.

## 6. Imagery
- **Food photography** on recipe/Tonight/Cook surfaces (Unsplash/Pexels: "home-cooked plate", "chicken rice greens", "healthy dinner"). Warm, real, un-glossy.
- **Illustration** for people, onboarding, empty states, the daily-breath warmth.
- **One candid hero photo** = the carer's plate (proof, homey, imperfect).

## 7. Screens to build (full app)
Reassurance-first order on every screen; one primary action in the thumb zone.

**Onboarding**
- **W1 Welcome** — brand mark + "FoodCare"; illustration; value line; primary "Set things up"; text link "Log in".
- **W1b Log in** — providers stacked; "Forgot password?".
- **W2 Household** — "Who do you cook for?"; quick-add role cards (Just me / Partner / Parent / Child / Someone else); added people as person chips; "Continue".
- **W3 Quick profile (sheet)** — name (optional, pre-filled), "Pick a look" (dots/illustration/photo optional), condition search + plain-language chips + "Add your own", flare/remote toggles; "Done".
- **W3b Create account** — deferred save; providers; "Maybe later".

**Daily loop**
- **W4 Today** — greeting; hero "Dad ate lunch. He's okay." + carer plate photo; "Tonight" card + "See tonight's meal"; people-state row (Iryna flare toggle, Dad kidney diet). Empty + alert variants.
- **W5 Iryna profile** — segmented Remission / Flare; "what changes" preview with tokens. Both states.
- **W6 / "Tonight"** (signature) — food-photo/illustration hero, dish name, one-base steps, per-person split rows with SAFE/MODIFY/AVOID, "Why these splits?", primary "Start cooking" + "Add to shopping list". *(Built — this is the reference screen.)*
- **W7 Whose plate?** (signature) — input row (type / photo / scan / pick-from-meal / voice); result: item + per-person tokens + one-line reasons + "Why?". **Mismatch variant** = context-triggered banner ("Logging dad's lunch → this is Iryna's → AVOID → Got it").
- **W8 Why this rule (sheet)** — one plain-language reason, optional "instead try", "Close".
- **Cook / Explore** — search + household filters (person dots); "cook once, split safely" featured card; recipe grid where each card carries a household safety strip (person dots + one token).

**Hand-off**
- **W9 Shopping** — auto list, per-person tags, a flagged clash row (AVOID), steppers, "Share list". Shop tab.
- **W10 Dad's care hub** — status header + SAFE; this-week plan (day rows + tokens); carer card; recent check-ins; "Plan dad's meals". Care tab.
- **W11 Assign a carer** — "Hand off the cooking, keep the menu"; carer invite; approved meals; permission note; "Send invite".

**Carer app (no tab bar, big targets)**
- **W12 Today for dad** — meal card + short steps + "no salt · soft" reminder; big "Cooked it, check in".
- **W13 Meal check-in** — photo capture; three big status choices (Ate well / Ate a little / Didn't eat); note; "Send". Refused variant reveals a gentle line.

**Reassurance**
- **W14 Daily breath** (signature) — big reassurance line + carer plate photo + time; day timeline (breakfast/lunch/dinner). **Alert variant** flips to "Dad hasn't eaten lunch yet. Olena's been reminded." + "Call dad".

## 8. Accessibility checklist
- Body ≥ 4.5:1, large/UI ≥ 3:1, verified by measurement (not by eye).
- Safety always word + icon + shape (survives grayscale / colorblindness).
- Targets ≥ 44pt, ≥ 8px apart; visible focus; safe areas.
- Reduced motion + Dynamic Type respected; real labels above inputs; inline validation.

## 9. Guardrails (anti-slop — from impeccable / taste-skill / ui-ux-pro-max)
- No cream/beige body background; no `#EBE7DB`-family warm neutrals.
- Display font is Manrope (a sans) — **never Fraunces / Instrument Serif**.
- One accent (`green/accent`), locked page-wide. Warmth via imagery + type, not a second brand hue (amber/coral are functional status colors only).
- No eyebrow/kicker above every section (max ~1 per 3 sections). No identical card grids. No gradient text. Glassmorphism only if purposeful. Cards only when elevation earns it; never nested.
- One radius scale; one icon family/weight; semantic tokens, no raw hex in components.
- One primary CTA per screen; skeletons over spinners.

## 10. Build order
1. Tokens (variables) + Manrope text styles + radius scale.
2. Components (section 4).
3. The **3 signature screens** first: Tonight, Whose plate?, Daily breath — with real Unsplash photography.
4. Extend to the full set reusing the library; wire the prototype (see the earlier prototype note: overlays for sheets, smart-animate for the flare toggle, the W13→W14 device-jump for the hand-off).
