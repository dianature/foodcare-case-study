# Wireframes — Sage, the caregiver cooking app (low-fi, phone-first)

## Context

Built on the approved **user-flow graph** (nodes N1 to N14) and the **Sage visual direction** (warmth and dignity, illustration-led, "Safe Hands bones, Quiet Kitchen skin"). Before any hi-fi design these low-fidelity wireframes lock, per screen: what content is on it, how it is placed, and the exact copy. Wireframes stay low-fidelity (a muted green tonal skin) and structural on purpose; color, illustration, and type come later from the style tile.

This pass covers the **full caregiver flow plus the separate carer app** (about 17 screens), built in Figma on the `OLD` page beside the user-flow poster.

**Sample household used in all copy (concrete, warm):** *You* (the cook), *Iryna* (partner, ulcerative colitis, rules change in a flare), *Dad* (kidney/CKD, lives alone, meals delivered, later handed to a carer named *Olena*). **Use "dad", never "Papa"**, everywhere.

## UX principles these wireframes must honor

Applied on every screen, not just stated:
1. **Reassurance before restriction (dignity).** The first thing on a screen is what is safe or that dad is okay, never a red wall. On the home screen, "dad ate, he's okay" sits above tonight's task.
2. **One primary action per screen**, placed in the bottom thumb-zone; secondary actions are quieter.
3. **People before conditions.** A person appears as a name with a chosen color or a friendly pre-offered illustration (a photo only if they choose to add one), and their medical rules as quiet metadata, never as "Profile 2 / CKD".
4. **Progressive disclosure.** Safety verdicts are one line; the "why" is a tap away in a sheet. Never a nutrient table on the surface.
5. **Redundant encoding.** Every safety state carries a word and a shape (SAFE / MODIFY / AVOID token), never color alone, so it survives grayscale and colorblindness.
6. **Glanceable and tired-proof.** Big targets, short lines, high contrast, one-handed reach, minimal steps. Judged "in one tired evening with dirty hands."
7. **No diary, ever.** Every input is a tap or a chip. The carer confirms in two taps.

## Design intelligence applied (ui-ux-pro-max, impeccable, taste)

- **Product register (ui-ux-pro-max).** The app sits at the intersection of *Recipe & Cooking* (warm food tones: sage, cream, terracotta) and *Medication reminder / caregiver health* (register: **Accessible & Ethical + Trust & Authority**; semantic **green = safe, red = alert; calm**). We **deliberately reject** the engine's generic recipe-app default (Claymorphism, "vibrant, no muted colors", purple-gradient buttons, haptic squish); that playful children's-app energy is wrong for a medical, dignity-led caregiver product. This validates the Sage direction and names the anti-pattern to avoid.
- **Candidate UI faces:** Figtree + Noto Sans (flagged "medical, clean, accessible, trustworthy") for the functional layer; the warm serif (Fraunces) stays for the human voice. Confirm at hi-fi.
- **Craft bar (impeccable):** WCAG 2.1 AA, contrast checked not eyeballed, visible keyboard focus, reduced-motion respected, copy at an **8th-grade reading level**, and **no hedging** ("This one's safe", never "This might be okay"). Purposeful restraint: every element earns its place.
- **Anti-slop dials (taste):** low **density** (one thing per screen, spacious), low **motion** (calm, no bounce), structured **variance** (a utility health app, not an experimental site), and a **hard em-dash ban in all UI copy** (matches the project writing rules).

## Wireframe conventions (the kit)

- **Frame:** 390 x 844 (phone). One screen per frame.
- **Muted green tonal skin (not flat grey, not the saturated brand):** a low-saturation green wireframe ramp so it already breathes the Sage world without committing hi-fi color. Page `#F3F5F1`, section field `#E9EEE7`, box fill `#DDE5DA` / stroke `#C4D0C0`, primary text `#2E3A32`, secondary `#6E7A70`. Primary button = filled deep muted green `#3D4E42` with a light label; secondary = outline in `#6E7A70`. (Wireframe tones, replaced by the real Sage palette at hi-fi.)
- **Placeholders:** illustration zones = a box labeled with the pre-offered illustration it will hold (pot, plate, bowl, sprig from the Sage set). The one real photo in the product is the carer's plate. Real copy everywhere, no lorem.
- **Safety token:** a bordered pill labeled `SAFE`, `MODIFY`, or `AVOID` plus a shape mark (check / tilde / cross), so it never rides on the green tone alone.
- **Person identity (avatars optional):** each person is a color chip or a pre-offered illustration plus their name (for example a sage dot + "Iryna"). The app ships a small set of friendly illustrations and a color palette to pick from; a real photo is never required, only offered.
- **Global nav (caregiver app):** bottom tab bar, 4 tabs: **Today, Cook, Shop, Care**. The carer app has no tab bar (single-purpose).
- **Touch (baked into every frame):** tappable targets at least 44 x 44 px, at least 8 px between them; big primary buttons for tired, one-handed use.
- **Forms (onboarding):** real labels above every field, never placeholder-only; validate on blur; every step has **Back** and, where honest, **Skip**.
- **Feedback and safety:** actions show loading then success or error, never silent; a short confirm step before high-stakes or irreversible actions (changing dad's rules, removing a person, a "didn't eat" report).
- **Empty states carry an action**, never a blank screen (first-run Today, empty Shopping, no carer yet); the active nav tab is clearly marked.

## Screens

Each entry: **purpose, layout (top to bottom), copy, states**. Flow node and feature in brackets.

### Onboarding (one-time)

**Order (value-first sign-up):** Welcome, then set up the household and profiles first with no account required, then create an account to save it. Returning users take the "Log in" path from Welcome and land straight on Today. A new user never hits a sign-up wall before seeing the point.

**W1 — Welcome** [N1]
- *Purpose:* set the warm tone; offer two paths, start setting up (no account yet) or log in.
- *Layout:* top brand mark placeholder + wordmark "Sage"; middle headline + subline; bottom primary button, then a quiet text link.
- *Copy:* H "Someone remembers, so you don't have to." Sub "A calmer way to cook when one kitchen runs more than one diet." Button "Set things up". Link "I already have an account · Log in".

**W1b — Log in (returning users)** [branch of N1]
- *Purpose:* quick return for people who already have an account.
- *Layout:* top bar back; provider or email buttons stacked; a help link.
- *Copy:* H "Welcome back." Buttons "Continue with Apple", "Continue with Google", "Continue with email". Link "Forgot password?". On success, land on Today (W4).

**W2 — Add your household (fast, tap-to-add)** [N2]
- *Purpose:* add everyone you cook for in the fewest possible taps. **Zero mandatory typing**; a person can be added with one tap and refined later.
- *Layout:* top bar "Your household"; one-line intro; a row of quick-add role cards that each create a person with sensible defaults and a suggested illustration/color; added people appear as color/illustration chips + name; bottom primary "Continue", quiet "Skip for now".
- *Copy:* H "Who do you cook for?" Sub "Tap to add. You can change anything later." Quick-add cards "Just me", "Partner", "Parent", "Child", "Someone else". Added-chip example "Iryna (partner)", "Dad (parent)". Button "Continue". Link "Skip for now".
- *Note:* tapping a role opens the quick sheet (W3); tapping "Continue" with defaults is a valid, complete setup.

**W3 — Quick profile sheet** [N3, feature 03 setup]
- *Purpose:* capture a person in the easiest way possible; nothing required, everything optional, editable later. No nutrient entry, no forms.
- *Layout:* bottom sheet. Line 1: **name** (optional, pre-filled with the role). Line 2: **"Pick a look"**, a row of pre-offered color dots and small illustrations, one tap; **"Add a photo" is offered as one option, never required**. Line 3: **"What should we watch for?"**, a **search field** above common plain-language condition chips, plus an **"Add your own"** entry; multi-select, default none. Context toggles appear only if a relevant chip is picked. Primary "Done", quiet "Skip".
- *Copy:* H "A few quick things (all optional)". Look row "Pick a look" (colors, illustrations, or "Add a photo"). Condition search placeholder "Search a condition or a food". Common chips "Kidney (low potassium)", "Low salt", "Ulcerative colitis", "Soft foods only", "No nuts or seeds", and "Add your own". Reassurance under chips "We turn these into safe and avoid for you. No tables to read." Toggle (flaring condition) "Her safe foods change during a flare" + helper "Flip her state in a tap so the list is never out of date." Toggle (parent) "Dad lives in another home" + helper "Lets you hand the cooking to a carer and still see he ate." Button "Done". Link "Skip".

**W3b — Create your account (save the setup)** [after N3]
- *Purpose:* now that the household is set up and the value is visible, create an account so it is saved, syncs across devices, and a carer can be invited later. Deferred to here on purpose.
- *Layout:* top bar back; a one-line "save what you set up" reassurance; provider or email buttons stacked; a quiet escape that keeps the setup on-device for now.
- *Copy:* H "Save your setup." Sub "Create an account so your household is safe and on every device." Buttons "Continue with Apple", "Continue with Google", "Continue with email". Link "Maybe later". On success, land on Today (W4).

### Daily loop (caregiver)

**W4 — Today (home)** [N4/N5]
- *Purpose:* the daily dashboard, reassurance-first, then tonight's decision, then states.
- *Layout:* top bar greeting + date. **Block A (hero, top):** dad status card, reassurance line + small plate-photo placeholder + carer credit. **Block B:** "Tonight" card, one-line safe summary + primary "See tonight's meal". **Block C:** people-state row, Iryna state + flare toggle, Dad "kidney diet". Bottom tab bar (Today active).
- *Copy:* Greeting "Good evening." Hero "Dad ate lunch, 1:10pm. He's okay." caption "photo from Olena, his carer". Tonight "One meal that works for you, Iryna and dad." Button "See tonight's meal". State row "Iryna, remission" (toggle), "Dad, kidney diet".
- *States:* empty (no carer yet), hero reads "Set up dad's check-ins"; alert (missed meal), hero flips to a gentle warning (see W14 alert).

**W5 — Iryna's profile, living rules** [N5, feature 03]
- *Purpose:* view and flip a person's state; show the safe-list recomputing.
- *Layout:* top bar back + "Iryna"; header name/role + current-state pill; large segmented control Remission / Flare; "what changes" preview list; bottom "Done".
- *Copy:* "How is Iryna today?" options "Remission" / "Flare". Helper "Flip this and her safe foods update everywhere, so you never cook the wrong thing." Preview "In a flare, Sage will:" "move tomato, coffee and raw veg to avoid", "push more protein, an extra egg or fish", "keep everything soft". Button "Done".
- *States:* Remission vs Flare (wireframe both; the preview list differs).

**W6 — Tonight, cook once, split safely** [N6, feature 01]
- *Purpose:* one base meal plus the exact per-person split.
- *Layout:* top bar back + "Tonight". **A:** dish hero (illustration placeholder + name + "one base, split two ways" + who-it-serves chips). **B:** "The base", the shared steps. **C:** "For each person", one row per eater: person chip + plain instruction + SAFE token. **D:** quiet link "Why these changes?" to W8. Bottom: primary "Add to shopping list", secondary "Start cooking".
- *Copy:* Dish "Rice, chicken and greens". Sub "One base, split two ways. Safe for everyone tonight." Base "Cook the rice and chicken plain, no salt." Rows: "You, season to taste." / "Iryna (flare), add a second egg for protein, keep it soft." / "Dad, hold the salt, double-boil the potato to cut the potassium." Link "Why these changes?" Buttons "Add to shopping list", "Start cooking".

**W7 — Whose plate?** [N7, feature 02]
- *Purpose:* per-person verdict for any dish or ingredient; guard against the wrong plate.
- *Layout:* top bar "Whose plate?"; search/scan entry at top; result card, item name + one row per eater (person chip + SAFE/MODIFY/AVOID token + one-line reason + "Why?" link).
- *Copy:* Search "Check a dish or ingredient". Item "Banana". Rows "Iryna, SAFE. Gentle in a flare." / "Dad, AVOID. Too much potassium for his kidneys." Row link "Why?".
- *States:* **Mismatch guard** (variant), a warning banner when a dish is headed to the wrong person: "Hold on, this container is Iryna's, not dad's." Button "Got it".

**W8 — Why this rule** [N8, feature 05], bottom sheet
- *Purpose:* the plain-language body reason, never a table.
- *Layout:* bottom sheet over W6/W7; header item + person; one or two sentence reason; optional "instead, try..."; close.
- *Copy:* H "Why dad can't have banana". Body "Bananas are high in potassium. Dad's kidneys can't clear the extra, so it builds up in his blood and strains his heart." Instead "Try apple or berries, much lower potassium." Button "Close".

**W9 — Shopping** [N9, feature 04]
- *Purpose:* auto-built list, each item tagged whose diet, clashes flagged before buying.
- *Layout:* top bar "Shopping" + week selector; list rows (checkbox + item + person tag(s)); a flagged row with a warning treatment; bottom "Share list" + add-item.
- *Copy:* Rows "Rice, everyone", "Bananas, Iryna only", "Low-salt stock, dad", flagged "Ready-made soup, check: too salty for dad". Button "Share list".

### Hand-off (caregiver)

**W10 — Dad's care hub** [N10]
- *Purpose:* run the remote person; this week's batch, the carer, the check-in history.
- *Layout:* top bar "Dad" (Care tab). Header name + "kidney diet" + today's status. **A:** "This week for dad", meals labeled by day, each with a SAFE token. **B:** carer card, "Olena cooks to your menu" + last check-in + "Manage carer" to W11. **C:** recent check-ins list. Bottom primary "Plan dad's meals".
- *Copy:* Header "Dad, kidney diet". Batch "This week for dad": "Mon, soft chicken and rice", "Tue, fish and mash", each "kidney-safe". Carer "Olena cooks to your menu" sub "you decide what, she cooks and checks in". Recent "Tue lunch, ate well", "Mon dinner, ate a little". Button "Plan dad's meals".

**W11 — Assign a carer, keep the menu** [N11]
- *Purpose:* invite a carer; split control-of-*what* from the labor.
- *Layout:* top bar back + "Dad's carer"; the split explained; carer contact/invite row; "Dad's approved meals" list you control; a permission line; bottom "Send invite" / "Save".
- *Copy:* H "Hand off the cooking, keep the menu." Sub "You decide what dad eats. Your carer cooks to it and shows you he ate." Carer row "Olena, invited". Section "Dad's approved meals". Permission "Olena can see the menu and check off meals. She can't change dad's rules." Buttons "Send invite", "Save".

### Carer app (separate, single-purpose, big targets)

**W12 — Today for dad (carer)** [N12]
- *Purpose:* dead-simple "what to cook today, to the caregiver's menu".
- *Layout:* top bar "Today for dad"; today's meal card(s), dish + short steps + a "no salt · soft" reminder; big primary "Cooked it, check in". No tab bar.
- *Copy:* H "Today for dad". Card "Lunch, soft chicken and rice", steps short, note "no salt · soft". Button "Cooked it, check in".

**W13 — Meal check-in (carer)** [N13, feature 06]
- *Purpose:* photo + one-tap status; two taps, no diary.
- *Layout:* top bar "How was lunch?"; large "add a photo of the plate" capture (placeholder); three big status buttons; optional note; bottom "Send".
- *Copy:* H "How was lunch?" Photo "Add a photo of the plate". Statuses "Ate well" / "Ate a little" / "Didn't eat". Note "Anything to add? (optional)". Button "Send to Natalia".
- *States:* **Refused** (variant), picking "Didn't eat" reveals a gentle line "We'll let Natalia know so she can check on him." before send.

### Reassurance (caregiver)

**W14 — Dad today (the daily breath)** [N14, feature 06 payoff]
- *Purpose:* the caregiver's calm; dad ate and is okay, without a call or a drive. The emotional peak.
- *Layout:* top: big reassurance line (serif at hi-fi) + plate-photo placeholder + time + carer; below: a simple day timeline (breakfast / lunch / dinner statuses).
- *Copy:* Hero "Dad ate lunch. He's okay." caption "1:10pm · photo from Olena". Timeline "Breakfast, ate well", "Lunch, ate well", "Dinner, coming up".
- *States:* **Alert** (variant), hero flips to "Dad hasn't eaten lunch yet. Olena's been reminded." + secondary "Call dad". The safety escalation, kept calm (clay, not alarm).

## States to wireframe explicitly (the interactive core)

- **Flare toggle:** W4 + W5 in remission vs flare (safe-list and split differ).
- **Whose plate:** safe verdict vs mismatch-guard banner (W7).
- **Carer status:** "ate well" (confirmed) vs "didn't eat" to caregiver alert (W13 to W14 alert).
- **First-run / empty:** W4 before any carer or check-in exists.

## Figma build plan

- **File / page:** `9Xer8M3pRsXMgMHLBKNUTa`, page **OLD** (`299:1410`), placed in a clear region below the user-flow poster (`385:1470`).
- **Frames:** about 17 phone frames (390 x 844) in the muted green tonal kit above. Arrange in labeled rows by act: *Onboarding, Daily loop, Hand-off, Carer app, Reassurance*, left to right in flow order, with the state variants as sibling frames beside their base screen. Optional thin connectors following the flow order so it reads as a clickable path.
- **Consistency:** the same bottom tab bar component (Today, Cook, Shop, Care) reused across caregiver screens; carer screens omit it.
- **Quota note:** the Figma MCP has a per-plan call limit; if it trips mid-build, resume when it resets. Building about 17 frames takes several batched calls.
- **Progress so far:** W1, W1b, W2, W3b built and verified; W3 and the daily loop, hand-off, carer, and reassurance rows remain.

## Verification

- Every flow node N1 to N14 maps to at least one wireframe; all **six features** are represented (01 W6, 02 W7, 03 W5, 04 W9, 05 W8, 06 W13/W14); the carer app is included.
- Every screen has real, warm copy, no lorem, reassurance-first, and **zero "Papa"** anywhere.
- The four state variants are drawn (flare, mismatch, refused/alert, empty).
- Nav is consistent, one primary action per screen sits in the thumb zone, and every safety state uses a word + shape token, never color, so it survives grayscale and colorblindness.
- **Accessibility baked in:** targets at least 44 px with at least 8 px gaps, real form labels, empty / loading / success / error and confirm states present where the UX rules require them (WCAG AA intent).
- **Copy is 8th-grade, warm, and un-hedged**, with no em dashes; the register stays *Accessible + Trust*, not the vibrant recipe-app default.
- **Wireframes wear a muted green tonal skin** (not flat grey, not the saturated brand); people are identified by a color or a pre-offered illustration with photo optional; and adding a person needs zero mandatory typing.
- **Value-first sign-up:** a new user completes household setup before creating an account (W3b), returning users log in from Welcome (W1b), and conditions are searchable with an "add your own" fallback.
