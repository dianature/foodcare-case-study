# FoodCare — Design Process

A short account of how this project moved from a generic brief to a chosen hi-fi UI direction with a full system spec. Working name FoodCare (placeholder). The cook is Eduard, his partner is Iryna, his father is Dad, and Olena is the carer.

## 1. The brief, and the first real move
The brief asked for a recipe app for people roughly 20-35. The first decision was to not design a general recipe app. General recipe apps are a crowded, low-trust category, and "make a recipe app" is not a problem, it is a format. So the first move was to find a specific person with a real reason to need the product.

## 2. Research, and how I narrowed the niche
I ran the research in passes and let each one cut the scope.

**Desk pass.** I looked at market size and, more usefully, at how people actually find and drop recipe apps. Reddit voice-of-customer said the same thing a hundred ways: people do not lack recipes, they lack a reason to open one more app.

**Primary pass.** I asked 14 people the core questions and went deep with four of them: three recorded interviews (P6, P3, P10) and a written chat survey (P9, P11). I transcribed the audio and read the chat by hand. The numbers were blunt. Only 2 of the 14 had ever used a dedicated recipe app, none used one now, and every person got recipes from Instagram, TikTok, Google, ChatGPT or Claude, or simply cooked what they already knew. P6 named the real tax herself, deciding what to cook every day, worst when both partners work. P3 cooks by opening the fridge and going from what is there. P9 would not install another app at all.

**The cut.** That closed the generic brief. A general recipe library answers a problem nobody in my sample had. So I stopped looking at discovery and looked for the pain with no good answer. It was cooking for more than one diet in the same kitchen, and cooking for someone who cannot give feedback. P3 already buys lactose-free for his wife. P6 cooks around her daughter's fish allergy and around vegetarian friends. The load falls on one person, and no single-user app helps them carry it.

**The white space.** That pointed at the caregiver, the person doing the cooking, not the patient. I ran further in-depth interviews on that situation to sharpen the pains, then built research personas to hold the findings and keep the design honest to real people. Two pains stood out because no single-user app touches them: a per-person safety check when two diets conflict, and a way to hand cooking to a carer while still seeing that the person actually ate.

## 3. The product truth
Everything after this answers to one line: "Someone remembers, so you don't have to." The user is the caregiver, 25-35, cooking for someone they care for, tired, and quietly worried. The stakes are medical, since a wrong plate can hospitalize someone, but the tone has to stay warm, not clinical. The ownable position sits between busy appetite-bait recipe apps and cold spreadsheet trackers: calm, human, and safety-first.

One rule carried into every screen: safety is shown by a word and an icon and a shape, never by color alone, so it survives grayscale and colorblindness.

## 4. From flow to wireframes
Before pixels, every screen was planned: what content sits on it, how it is placed, and the exact copy. Then I built the low-fi wireframes in Figma, about 21 phone screens, on a real system rather than loose frames:
- green color variables, text styles, and reusable components (status bar, caregiver tab bar, and the shape-coded SAFE / MODIFY / AVOID tokens).
- low-fi on purpose: titles only, green only, and everything else as placeholder bars, so the review stayed about structure and not decoration.

The set covers the whole product: onboarding, the daily loop, the hand-off to a carer, the separate carer app, and the reassurance moment. The four hard states are drawn too: the flare toggle, the wrong-plate guard, the "didn't eat" alert, and the first-run empty state.

## 5. The two hero moments, and honest product logic
Two screens carry the product.

**Whose plate** answers "can this food go to this person right now." It gives a per-person verdict with a plain reason. During review, two real questions sharpened it:
- Input should not be limited to search. It also takes a photo, a barcode scan, a pick from a meal the app already knows, and voice. A photo has to show what it thinks it saw before it gives a verdict, because a wrong guess here is a safety verdict on the wrong food.
- The wrong-plate warning cannot be magic. The app only knows a plate is headed to the wrong person when something says so: you are in that person's context, or you scanned a labeled container. So the guard was reframed as context-triggered, "logging Dad's lunch, this looks like Iryna's, avoid," instead of pretending the app watches your hands.

**Tonight** is cook once, split safely. One base meal, then the exact per-person change, each with its safety token.

Because it is still a recipe app, I added a recipe-explore screen, adapted to the model: you filter by who is in your household, and every recipe card carries a household safety strip, so you never browse recipes in the abstract.

## 6. Choosing the hi-fi look
The hi-fi visual direction was treated as its own study, not inherited from the wireframe skin. Audience was set to 25-35 cooking for someone. Three design skills were applied (impeccable, taste, and ui-ux-pro-max), which also corrected two easy defaults: no cream-and-terracotta palette, and no Fraunces serif, both of which read as AI defaults.

Three directions were built at hi-fi on the same screen, Tonight, each with real stock food photography:
- **Editorial Nutrition:** light, big confident grotesk, food-photo hero, line-icon tiles.
- **Committed Color:** a drenched deep-green screen with the photo title overlaid, amber accent.
- **Calm Bento:** soft, humanist, illustration and bento tiles, the quietest and most care-forward.

Calm Bento won. It was then reskinned to a picked palette taken from a reference (light ground, near-black ink, a darkened lime-green accent, and green / amber / coral mapped onto the safety tokens). A style tile was built beside it.

## 7. The system and the spec
The picked direction is written up as a full generation spec (FoodCare-UI-Design-Spec.md): tokens (color, Manrope type scale, spacing, radius), the icon system (Phosphor), the safety-token system, every core component, the screen-by-screen build, the voice rules, an accessibility checklist, and the anti-cliche guardrails. It is the single source of truth so the rest of the hi-fi work stays consistent, whoever builds it.

## 8. Building the hi-fi app
With the spec as the source of truth, I built the whole app in Figma, 18 screens plus a design system on the OLD page. A few decisions shaped it:
- **The account holder is Eduard.** The person using the app is the cook, so his name is on it, and Olena stays as the carer he can hand off to. That keeps the two roles from blurring.
- **Real food photography replaced the placeholder illustrations.** The welcome hero and every recipe surface now carry real stock plates, warm and un-glossy, so appetite shows up where it earns its place. People stay as colored initials, not photos, so no one is reduced to a picture of a sick relative.
- **A more vibrant onboarding.** I pushed the accents from the muted olive toward the color-palette references: a brighter Kiwi as the primary, with Carrot and Sunshine as warm counter-tones, so the setup flow feels alive rather than clinical.
- **My own color pass.** I warmed the identity palette, You in khaki, Iryna in olive, Dad in orange, on the Kiwi accent, and carried it across every screen so the three people stay distinct at a glance.

The build covers the full product: onboarding, the daily loop, the signature Tonight, Whose plate and Daily breath, the Why this rule sheet, cook and shopping, Dad's care hub, assigning a carer, and the separate carer app.

**The prototype is wired end to end, then checked.** Every screen connects: onboarding into the app, the four-tab bar across Today, Cook, Shop and Care, the Why this rule sheet floating over a dimmed Tonight, and the hand-off from the family app into the carer's. After wiring I ran a reachability pass over every link, which caught a few dead ends left from moving the file around, a tab bar that went nowhere, a screen nothing pointed to, a back button aimed at the wrong step, and I fixed them. All 18 screens are now reachable from the first screen with no orphans, and the flow starts at Welcome.

**Two smaller passes sharpened it.** I tightened the recipe cards so each keeps its title and its per-person safety strip, added a flagged "table salt" row to the shopping list so the clash banner points at a real item, and gave Dad his own quick-profile so both people get set up in onboarding.

Two things I held to for hand-off quality:
- **Real structure, not spacers.** Every screen uses grouped auto-layout sections, so the rhythm comes from the layout and not from filler frames.
- **A documented system, in flow order.** The palette, the Manrope type scale, and the components (safety tokens, buttons, chips, avatars, person dots, toggle, stepper) sit on one design-system board, and the screens are renamed and reordered so they read as a real product flow.

## 9. Where it stands
The research is closed, the low-fi set is built, and the hi-fi app is built, wired and checked: 18 screens plus a design system, in the Calm Bento direction and my warmed palette, with real food photography throughout and a clickable prototype that runs the full flow from onboarding through the daily loop to the carer hand-off, verified so every screen is reachable. What remains is the case-study writeup for the submission, an accessibility and contrast QA pass, and developer hand-off notes.

## Method note
Research combined desk analysis, a 14-person study with recorded interviews and a chat survey, and a caregiver deep-dive backed by research personas. Figma work was done through a plugin API, which made the design system, the components, and the many state variants fast and consistent. Food photography is real stock, placed on the recipe surfaces where appetite earns its place, while people and empty states stay as illustration so no one is reduced to a photo of a sick relative.
