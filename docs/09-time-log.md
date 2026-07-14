# Project Log: Time and Stages

Awesomic test task, recipe app for people 20-35.

Work ran across five working days, July 1-7, 2026 (July 4-5 off). Hours are a working estimate based on the artifacts produced.

**Estimated total: about 40.5 hours over five working days.**

| Block | Days | Time |
|---|---|---|
| Research and strategy | July 1-2 | ~13 h |
| Caregiver niche deep-dive | July 3 | ~5 h |
| Wireframes, hi-fi direction, and build | July 6-7 | ~22.5 h |

---

## July 1-2: Research and strategy (~13 h)

| # | Stage | What happened | Artifacts | Est. time |
|---|---|---|---|---|
| 1 | Brief intake and framing | Read the generic brief, decided the real first move was to narrow to a specific person, not design a general app | notes | 0.5 h |
| 2 | Desk and market research | Market size, voice-of-customer, how people find and abandon recipe apps | strategy doc (market section) | 2.0 h |
| 3 | Ideation | Generated niche directions, including unconventional and clinical ones, then a shortlist of directions | strategy doc (ideation, shortlist) | 1.5 h |
| 4 | Competitor and gap analysis | Tiering, review mining, positioning map, and the "why not" verdict per idea | strategy doc (competitor audit), competitor table | 2.0 h |
| 5 | USP and narrowing | Differentiation framework, chose the directions worth building | strategy doc (USP), decision guide | 1.0 h |
| 6 | Visualization in Figma | Ideation mind map, competitor gaps table with sources, and the Selected Directions map, plus palette and avatar iterations | Figma page "OLD" | 2.5 h |
| 7 | Primary research prep | Built the interview guide for men 30-40 | interview guide | 0.5 h |
| 8 | Primary research | Ran 3 recorded interviews and 1 Telegram chat survey | audio files, chat screenshots | 1.5 h |
| 9 | Transcription and reading | Transcribed audio with Whisper, read the chat screenshots | transcripts, raw transcriptions file | 0.5 h |
| 10 | Synthesis | Combined numbers and quotes, wrote up what the research changed | research summary | 1.0 h |

**Subtotal: about 13 hours over two days.**

---

## July 3: Caregiver niche deep-dive and visualization prep (~5 h)

| # | Stage | What happened | Artifacts | Est. time |
|---|---|---|---|---|
| 11 | Voice profiling | Analyzed a psychologist's interview transcripts and built a tone-of-voice profile so persona speech would read like a real person | Iryna tone-of-voice profile | 0.75 h |
| 12 | Persona building (caregiver white space) | Built research personas for the caregiver and multiple-restriction direction, using the persona method | Iryna, Eduard, and Natalia persona docs | 1.0 h |
| 13 | Simulated depth interviews | Ran bilingual persona interviews to surface caregiver pain points, one joint couple interview and one single, plus a reusable question set | 2 interview transcripts, Iryna question set | 1.5 h |
| 14 | Pain-point synthesis and feature ideas | Ranked the pains and mapped candidate features to them: a per-person conflict-detector for conflicting diets, and a delegation with visibility loop for a non-communicative dependent | 2 pain-and-feature docs | 1.25 h |
| 15 | Visualization design style | Defined the visual system for the research visualizations, grounded in the mind-map and process-map references | design style doc | 0.5 h |

**Subtotal: about 5 hours. Running total: about 18 hours over three days.**

---

## July 6-7: Wireframes, hi-fi direction, and the high-fidelity build (~22.5 h)

| # | Stage | What happened | Artifacts | Est. time |
|---|---|---|---|---|
| 16 | Visual direction and wireframe plan | Locked the product identity (green, warmth, dignity, the per-person safety system, the reassurance voice) and planned every screen: content, layout, and exact copy before any pixels | Visual-Direction doc, Wireframes-Plan | 1.5 h |
| 17 | Low-fi wireframes build | Built about 21 phone screens in Figma on the OLD page, on a real system: green color variables, text styles, and components (status bar, caregiver tab bar, shape-coded SAFE / MODIFY / AVOID tokens). Low-fi on purpose: titles only, green only, everything else as placeholder bars | Figma OLD page, wireframe set | 3.0 h |
| 18 | Product logic detailing | Worked out how "Whose plate" takes input (type, photo, scan, pick from a meal, voice) and reframed the wrong-plate warning as a context-triggered guard, then added the recipe-explore screen with per-person safety on every card | updated W7 and Cook screens | 1.0 h |
| 19 | Competitive and reference scan | Reviewed the current popular recipe apps and analyzed 10 UI references, to place FoodCare between busy recipe apps and cold trackers and to avoid category clichés | notes | 1.0 h |
| 20 | Hi-fi direction exploration | Set the audience to 25-35 cooking for someone, applied three design skills (impeccable, taste, ui-ux-pro-max), and built three distinct hi-fi "Tonight" directions with real stock food photography: Editorial Nutrition, Committed Color, and Calm Bento | Figma OLD, D1 / D2 / D3 | 2.0 h |
| 21 | Direction lock and system spec | Chose Calm Bento, reskinned it to the picked palette (from ui-ref-01, green darkened), built a style tile, and wrote the full UI generation spec covering tokens, components, screens, voice, and accessibility | Figma OLD, FoodCare-UI-Design-Spec | 1.5 h |
| 22 | Design import and token setup | Brought the Calm Bento hi-fi into Figma from the Claude Design handoff bundle, then set up the FoodCare color tokens (canvas, surface, soft, ink, the SAFE / MODIFY / AVOID ramp, and the vibrant Kiwi, Carrot and Sunshine accents) and the Manrope type ramp on the OLD page | FoodCare variables | 0.75 h |
| 23 | Onboarding, hi-fi | Built the six onboarding screens with the account holder set to Eduard and Olena kept as the carer, a real stock-photo hero in place of the CSS illustration, and the more vibrant accents from the color-palette references | Welcome, Log in, Household, Quick profile (Iryna), Quick profile (Dad), Create account | 2.0 h |
| 24 | Daily loop and signature screens | Built Today, the Iryna condition profile, and the signature Tonight, Whose plate and Daily breath, plus the Why this rule sheet, all with real food photography instead of the placeholder illustrations | 6 screens | 2.5 h |
| 25 | Cook and hand-off | Built Cook with a recipe grid that carries per-person safety on every card, Shopping with a flagged clash row and steppers, Dad's care hub, and Assign a carer | 4 screens | 2.0 h |
| 26 | Carer app | Built the carer side, Today for Dad and the Meal check-in, with big targets and no tab bar | 2 screens | 0.75 h |
| 27 | Color pass | Warmed the identity palette to my own version, You in khaki, Iryna in olive, Dad in orange, on the vibrant Kiwi accent, and carried it across every screen | palette update | 0.5 h |
| 28 | Clickable prototype | Wired the full flow: onboarding into the app, the four-tab bar, the Why this rule sheet over a dimmed Tonight, and the carer hand-off, all with dissolve transitions | Figma prototype | 1.25 h |
| 29 | Review and refinement | Tightened the Cook recipe cards, added the Table salt row so the clash banner reads true, added Dad's quick profile, and fixed the sizing and clipping issues I caught in review | fixes | 1.0 h |
| 30 | Structure and naming cleanup | Refactored every screen from spacer frames to grouped auto-layout sections so spacing comes from real structure, then renamed and reordered all screens into logical flow order for hand-off | clean layer tree | 1.0 h |
| 31 | Design system frame | Built a design-system board documenting the palette, the Manrope ramp, and the components: safety tokens, buttons, chips, avatars, person dots, toggle and stepper | Design System frame | 0.75 h |

**Subtotal: about 22.5 hours over two days.**

---

**Estimated total: about 40.5 hours over five working days (July 1, 2, 3, 6, 7).**
