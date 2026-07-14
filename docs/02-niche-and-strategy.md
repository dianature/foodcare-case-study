# Recipe App — Niche & USP Strategy (Pre-Design Audit)

## Context

The brief ("food recipe app for men/women 20-35, suggest a USP that drives engagement") is
too generic to design against. A recipe app for "everyone 20-35" fights well-funded
generalists head-on and loses. This document does the upstream work: find specific,
underserved people who would actually download and *keep using* the app, audit 5-7 niche
directions honestly, run a structured competitor audit, and derive the ownable USP.

- **Market:** US (largest, ~28% global share; also most contested, so niche precision matters).
- **Scope:** strategy + USP only. No UI/UX yet. Team picks the final niche.
- **Method (skills applied):** built on the `ai-marketing-claude` `/market competitors`
  framework — competitor tiering (direct / indirect / aspirational), review mining, a 2×2
  positioning map, per-competitor SWOT, and its Differentiation Framework
  (Category / Audience / Feature / Philosophy / Experience) to derive the USP. Voice-of-customer
  from Reddit + App-Store review signal. `gstack scrape` and `/market competitors <url>` are
  the tools to pull live competitor data once a landing page / concept URL exists (see
  Execution). Note: neither skill is registered as an invocable `/command` in this session,
  so their methodologies were applied by hand rather than auto-run.

## Market snapshot (US, 2025-2026)

- US recipe-app market ~$440M (2025) → ~$943M (2033); global ~$6.4B → ~$14B.
- Crowded with generalists; discovery + import + grocery lists are commoditized.
- Field-wide weaknesses (market reports + VOC):
  - **Decision fatigue** is the #1 emotional pain, not lack of recipes.
  - Apps **assume tidy linear planning**; real people repeat 1-2 dishes, improvise, substitute.
  - **Grocery lists are inaccurate**; "apps just save recipes and populate a bad list."
  - **UGC recipe quality** is inconsistent (wrong measurements, vague steps) — trust gap.
  - Weeknight recipes are **overcomplicated** for the time/energy people actually have.

**Strategic read:** the wedge is *psychographic* (a specific relationship to cooking), not more
content. Retention comes from reducing daily mental load.

## Voice-of-customer evidence (US, primary signal)

- r/adhdwomen: "make it take as little executive function as possible."
- r/Cooking "I hate all meal-planning apps": "they don't actually help you plan… just save
  recipes and populate an inaccurate grocery list."
- r/mealprep / r/MealPrepSunday: people "mostly eat the same stuff," improvise with leftovers,
  quit apps that are "just another thing to manage."
- r/simpleliving: recipe generators fail because "no easy way to update memory… assumes I have
  things I don't."

## Ideation — directions considered

Reduce mental load (executive function) · skill-building for non-cooks · money/waste pressure ·
body/performance goals · behavior-honest tools (embrace repeat + improvise) · shared kitchens ·
life-stage/occupation (shift workers, new movers).

## Shortlist — 6 niches audited

### Scoring (1-5, directional; higher = better)

| # | Niche | Who-downloads clarity | Pain intensity | US size (20-35) | White space | Retention loop | Build feasibility | Total |
|---|-------|:--:|:--:|:--:|:--:|:--:|:--:|:--:|
| 1 | ADHD / low-executive-function cooks | 5 | 5 | 4 | 5 | 5 | 4 | **28** |
| 5 | Repertoire rotation ("your 15 meals") | 3 | 3 | 5 | 5 | 4 | 4 | 24 |
| 2 | First-apartment / can't-cook solos | 5 | 4 | 4 | 3 | 3 | 4 | 23 |
| 3 | Pantry-first anti-waste | 4 | 4 | 4 | 3 | 4 | 3 | 22 |
| 4 | Gym high-protein-on-a-budget | 4 | 4 | 4 | 2 | 4 | 3 | 21 |
| 6 | Two-goal shared kitchen (couples) | 4 | 3 | 3 | 4 | 3 | 3 | 20 |

### 1. ADHD / low-executive-function cooks
- **Who:** 22-35, diagnosed/self-identifying ADHD or "low-spoons" cooks; vocal, community-clustered (r/adhdwomen ~600k).
- **Problem:** cooking fails at the *decision + initiation* step; standard apps add choices and admin, making it worse.
- **Why download & retain:** daily relief from a daily pain = habit loop; strong emotional identification drives word-of-mouth.
- **Good:** owns an emotional position nobody markets to; high retention; defensible brand; cheap community-led reach.
- **Bad / risk:** "ADHD app" framing risks feeling medicalized (avoid clinical claims); TAM *perceived* narrow (it's a beachhead, expandable to all overwhelmed cooks).
- **Candidate USP / engagement feature:** **"Decide for me" mode** — one tap serves tonight's meal from a small rotating set tuned to your energy ("low-spoons" vs "up for it"), fewest steps/tools/ingredients; learns and shrinks decisions over time.

### 5. Repertoire rotation ("your 15 meals")
- **Who:** 25-35 who openly "eat the same stuff" and are fine with it — the silent majority VOC keeps describing.
- **Problem:** every app pushes *discovery* (more choice); real behavior is *rotation* (perfect + cycle a small set). No app is built for this.
- **Why download & retain:** low-pressure, matches actual habit → low churn; doesn't fight the user.
- **Good:** huge latent TAM; wide-open white space; simple to build (curate, not generate).
- **Bad / risk:** benefit is subtle to market ("an app for meals I already make?"); needs sharp positioning to feel like a product, not a note in Notes.
- **Candidate USP:** **auto-rotating meal wheel** — bank ~15 dishes; it builds the week from them, spaces repeats to prevent fatigue, suggests *one* new dish only when you're bored.

### 2. First-apartment / can't-cook solos
- **Who:** 21-27, just moved out, tiny kitchen, 4-5 tools, real ingredient anxiety.
- **Problem:** apps assume competence + equipment; they inspire, don't teach.
- **Good:** clear persona; strong onboarding story; CPG-sponsor friendly.
- **Bad / risk:** users churn as skills grow (lifecycle problem); content-heavy build; competes with free TikTok/YouTube.
- **Candidate USP:** **"minimum-viable-kitchen" mode** — every recipe doable with 5 tools + a beginner skill tree; substitutions taught inline to build confidence.

### 3. Pantry-first anti-waste
- **Who:** 24-35, cost-of-living conscious, hate throwing food out.
- **Problem:** "cook before it spoils"; existing pantry apps have weak UX and stale inventory.
- **Good:** concrete ROI story ($ saved); timely macro tailwind.
- **Bad / risk:** pantry data entry is the graveyard of these apps — dies unless input is near-zero (receipt/photo scan), which is hard to build.
- **Candidate USP:** **"use-it-up" engine** — rank recipes by what's expiring first; frictionless inventory via receipt/photo scan; weekly "rescue" nudge.

### 4. Gym high-protein-on-a-budget
- **Who:** 20-32, lifting/body-recomp, want protein + macros without MyFitnessPal tedium.
- **Problem:** macro apps are spreadsheets; recipe apps ignore macros; nobody optimizes protein-per-dollar.
- **Good:** monetizes well; measurable outcomes.
- **Bad / risk:** **most contested space** (MacroFactor, Eat This Much, MyFitnessPal); hard to out-execute funded incumbents.
- **Candidate USP:** **protein-per-dollar ranking** + auto-scaled macro portions — a real gap, but a feature more than a moat.

### 6. Two-goal shared kitchen (couples / roommates)
- **Who:** 24-35 couples where one bulks / one cuts, or mismatched diets, cooking one base meal.
- **Problem:** apps are single-user; shared planning + "don't cook what my partner won't eat" is unsolved.
- **Good:** shared = stickier (two users, network lock-in); built-in virality (invite partner).
- **Bad / risk:** two-goal-one-meal logic is complex; smaller/older-skewing; onboarding needs both people.
- **Candidate USP:** **one base recipe, two macro splits** — cook once, portion/adjust per person's goal automatically.

### Also-ran ideas (cut, noted for completeness)
- **Shift workers (nurses/hospitality):** specific and real, but hard to reach as a marketing segment.
- **Diaspora heritage cooking w/ US-supermarket substitutions:** emotionally strong but fragmented across cuisines; better as a feature than a beachhead.

## Competitor audit (`/market competitors` framework, US)

Here the "target" is the *concept* being defined; competitors are audited to find its ownable gap.

### Competitor tiers
| Tier | Players | Role |
|---|---|---|
| **Direct** | Samsung Food (ex-Whisk), Mealime, SideChef, Paprika | Same product/audience; own discovery, import, guided cook, grocery lists |
| **Indirect** | SuperCook / Cooklist (pantry), Eat This Much / MacroFactor (macros), AnyList / Cozi (lists) | Solve one adjacent slice of the problem |
| **Aspirational** | Tasty, Allrecipes | Category-defining reach and brand |

### Review-mining matrix (real signal)
| Competitor | Positioning | Top praise | Top complaint / gap |
|---|---|---|---|
| Samsung Food | Broad free planner + AI | Generous free tier, import, meal plan | Best features (recipe scan, **cook mode**) behind paywall; generic/overwhelming |
| Mealime | Frictionless quick weeknight dinners | Fast, auto grocery list, "don't know how I managed without it" | **Limited library; no import of own recipes;** "quick," not "brainless"/adaptive |
| SideChef | Guided step cook + grocery partners | Step-by-step, Walmart/AmazonFresh checkout | Assumes a capable cook; feature-heavy; discovery ≠ decision |
| Paprika | Recipe manager, one-time buy | Reliable storage, no subscription | No discovery, no planning intelligence, **no rotation logic** |
| SuperCook | Ingredient/pantry search, free | 11M recipes by what you have | Weak UX, stale inventory, high input friction |
| Eat This Much / MacroFactor | Macro automation | Automated macro plans | Spreadsheet feel; not recipe-first or budget-first |

### Positioning map
```
                     GENERIC / MASS MARKET
                              |
        Samsung Food •        |        • SideChef
        Allrecipes •          |        • Tasty
   MORE CONTENT  ─────────────┼───────────── LESS THINKING
   (discovery)      Paprika • | • Mealime      (decision/execution)
                              |
                              |   ← ← WHITE SPACE → →
                              |   (Ideas 1 & 5 live here)
                    SPECIFIC PERSON / IDENTITY
```
Nobody occupies **"less thinking × specific identity"** — the bottom-right. Every incumbent
either adds content or stays generic. That quadrant is the wedge.

### Target-concept SWOT (aggregate)
- **Strengths:** owns an emotional/behavioral position; daily habit loop; community seedable.
- **Weaknesses:** no content library or brand at launch; perceived-narrow TAM.
- **Opportunities:** four unclaimed white spaces (below); incumbents' best features are paywalled or generic.
- **Threats:** a generalist (esp. Samsung Food, free) could bolt on a "decide for me" feature; free TikTok/YouTube substitutes.

### Four unclaimed white spaces
1. **Executive-load reduction** — "brainless cooking." (Idea 1) — *most defensible.*
2. **Behavior-honest tools** — embrace repeat + improvise + substitute. (Ideas 1, 5)
3. **Recipe trust** — tested/verified over UGC slop. (cross-cutting)
4. **Real-life flexibility** — skip sides, swap ingredients, use leftovers. (Ideas 1, 3, 5)

## USP derivation — Differentiation Framework

Testing each axis for the strongest niches:

| Axis | Best play | Verdict |
|---|---|---|
| **Category** | Create "the anti-decision cooking app" sub-category | **Ownable** — no incumbent claims it |
| **Audience** | Own overwhelmed / low-executive-function cooks (beachhead: ADHD) | **Ownable** — competitors are generic |
| **Feature** | "Decide for me" energy-tuned meal + rotation engine | Strong, but copyable — needs Category+Audience to defend |
| **Philosophy** | "Less thinking, not more recipes"; honor repeat + improvise | **Ownable** — opposite of the whole category's instinct |
| **Experience** | Only ever tested recipes; frictionless daily loop | Reinforcing trust layer |

**Recommended USP (whichever niche wins):** position on **Category + Audience + Philosophy**,
not on a feature —
> **"The app that makes the decision, not more decisions."**
> An adaptive engine that shrinks tonight's cooking to one confident choice, honors that people
> repeat and improvise, and only ever surfaces tested recipes.

The concrete engagement feature is the chosen niche's candidate USP (e.g., **"Decide for me /
low-spoons mode"** for Idea 1; **auto-rotating meal wheel** for Idea 5).

## Steal-worthy tactics (from the audit)
- SideChef's **guided cook mode** (behind Samsung Food's paywall) — offer it free as the retention hook.
- Mealime's **auto grocery list** — but make it *accurate*, the field's recurring complaint.
- SideChef's **grocery-partner checkout** (Walmart/AmazonFresh) — a monetization + convenience lever.
- Paprika's **one-time-buy trust** — consider vs subscription fatigue in the pricing test.

## Round 2 — unconventional & clinical directions (researched)

The team proposed a second wave of ideas. Researched for real market worthiness below. **Blunt
takeaway: several "no competitor does this" claims are false** — the space is more built-out
than the source notes suggested. Verdicts: ✅ worth it · 🔁 fold into an existing niche · 🧩
feature not a niche · ⚠️ risky/off-brief · ❌ already owned.

### A. Unconventional consumer ideas

| Idea | Evidence found | Verdict |
|---|---|---|
| **Bachelors / single men** | Bachelor Cooking, "One-Pan Cookbook for Men," "easy meals for single guys" — plentiful, and overlaps Mealime/SideChef | 🔁 **Fold into Idea 2** as a persona/marketing skin; gendered framing only shrinks TAM |
| **Fandom / "magic" recipes** (fantasy books/films/games) | The Geeky Chef (blog + 4 published cookbooks: LOTR, Harry Potter, Zelda, GoT), many unofficial fan cookbooks — but **no polished app** | 🧩 High *engagement*, low daily *utility* (you don't cook Butterbeer on a Tuesday). **IP/licensing risk** (WB/Nintendo/Disney). Best as viral **theme packs / content-marketing layer** on a real app, not the core |
| **Voice narration + voice input** (hands-free) | Live category: Voicipe, Cookie, Suvio, CookAI + Alexa/Google Assistant; voice-appliance market $20B→$70B by 2032 | 🧩 **Feature, not a niche.** Powerful *accessibility* multiplier — pairs best with low-executive-function (Idea 1), seniors, low-vision |
| **Lab-result-adaptive recipes** (scan blood panel → raise iron/potassium/etc.) | InsideTracker (48 biomarkers), ZOE (gut/glucose), January AI — premium, coaching/supplement-first, **not recipe-first** | ⚠️ Real white space (consumer-priced, recipe-first) but **high trust/regulatory cost**; not an MVP. Premium feature for a health niche later |

### B. Clinical / dietary-restriction cluster

| Audience | Reality check | Verdict |
|---|---|---|
| **CKD / kidney** | **KidneyPal already does it** — CKD-stage/dialysis-personalized limits **and** "import any recipe → kidney-safe in seconds," plus KidneyDiet.com, "Kidney Diet Friendly Recipes" | ❌ **Not white space** — saturated by focused players |
| **IBS / low-FODMAP** | Monash FODMAP owns the data (reference-first); many low-FODMAP recipe resources exist | ⚠️ Recipe-first gap is real-ish but contested; **hits 20-35** (on-brief) |
| **Histamine intolerance** | Only **Fig** (multi-intolerance scanner) + blogs/PDFs; no recipe-first app | ✅ Genuinely early — but **tiny TAM**; viable only as part of a broader restriction platform |
| **Post-bariatric** | Baritastic / Bariatric Fusion are **tracker-first, recipe bolted-on** | ✅/⚠️ Real gap (post-op eating mechanics), but **skews older, off the 20-35 brief** |
| **Diabetic / pre-diabetic** | Large market, but heavily served by tracker-first apps + many diabetic recipe resources | ⚠️ Big but contested; partly on-brief |
| **Caregivers cooking for someone else** | No app centralizes managing *another person's* restrictions remotely | ✅ **Strongest clinical white space** — but multi-user + health-data complexity |
| **Compound / multiple restrictions** | Partly served: Fig (multi-intolerance), NumYum markets "multiple diets" — but the **clinical overlap** (CKD + diabetic + low-sodium) is under-served | ✅/⚠️ Genuine gap for *clinical* stacking; commoditized for lifestyle diets |
| **Seniors (low-vision/dexterity)** | Flagged underserved; pairs with voice | ⚠️ Real but **outside 20-35 brief**; distinct UX |

### C. The five cross-cutting features

| Feature | Verdict |
|---|---|
| 1. "Make this safe" universal converter | ❌ **Not novel** — Honeydew, Nori, Ollie AI, NumYum, KidneyPal all do AI recipe adaptation/import. Commoditizing; table stakes, not a moat |
| 2. Symptom-to-recipe feedback loop | ✅ **Most differentiated feature** — per-recipe symptom correlation (IBS/histamine) is rarer than generic charts; merges tracker + recipe book |
| 3. Compound-restriction filtering | 🧩 Useful, partly served; strongest for *clinical* overlap |
| 4. Caregiver mode | ✅ **Genuinely underserved**; strongest of the five as a wedge |
| 5. Lab-result-aware thresholds | ⚠️ Exists at premium (InsideTracker/ZOE); high-trust signal but heavy to build |

### Round 2 synthesis — two coherent paths

The clinical ideas mostly **break the original 20-35 brief** (CKD/bariatric/seniors skew older) and
carry health-claim/regulatory caution. Two internally consistent strategies emerge:

- **Path A — Engagement-led, on-brief (20-35):** decision-reduction beachhead (Idea 1 / overwhelmed
  cooks) + **voice** as an accessibility feature + optional **fandom "theme packs"** as a viral
  marketing layer. Stays in the brief, defensible, cheap to seed. *Recommended default.*
- **Path B — Health-led, off original brief:** pick ONE condition that still hits 20-35
  (**low-FODMAP/IBS** or **diabetic**) *or* the **caregiver** white space; differentiate with the
  **symptom-feedback loop** (feature #2) + clinical **compound-restriction** stacking (#3). Higher
  willingness-to-pay, but multi-user/health-data complexity and regulatory caution, and it widens
  the audience beyond the brief.

**Do not** build the "make this safe" converter as the differentiator (feature #1) — it's already
table stakes.

## How to choose (decision guide for the team)
- **Most defensible, highest-retention, seedable community?** → **Idea 1 (ADHD / low-executive-function).**
- **Biggest latent audience, almost no direct competitor?** → **Idea 5 (Repertoire rotation).**
- **Clear monetization, measurable outcomes, accept a crowded field?** → **Idea 4 (Gym budget-protein).**
- **Highest willingness-to-pay, willing to go off-brief + handle health-data/regulatory?** →
  **Path B**: low-FODMAP/IBS or diabetic (still 20-35), or the **caregiver** white space, differentiated
  by the symptom-feedback loop + clinical compound-restriction stacking.
- **Avoid** leading with Idea 4, the generic "make this safe" converter, or a generalist position —
  each is where incumbents already win.
- **Directional lean (not a mandate):** **Path A** — Idea 1 as beachhead, with Idea 5 + trust/flexibility
  white spaces as reinforcing features, voice as an accessibility multiplier, and fandom theme packs as a
  viral marketing layer; expand outward to all "overwhelmed cooks." It best satisfies the original
  20-35 brief while owning the clearest emotional white space.

## Execution & verification (validate before designing)

Strategy work → market-facing validation, and this is where the skills run live:
1. **Live competitor pull:** stand up a one-page concept/landing, then run `/market competitors <url>`
   and `gstack scrape` against Samsung Food / Mealime / SideChef pages + App-Store listings to
   refresh the review-mining and pricing matrices with current data.
2. **Demand test:** 3-4 landing/concept-ad variants (Ideas 1, 5, 4), compare signup/CTR — let the market pick.
3. **VOC interviews:** 5-8 users from the target subreddit/community per finalist niche; confirm the pain + "would-download" trigger.
4. **Competitor teardown:** install the 2 closest competitors for the chosen niche, map the exact UX moment they fail the persona — that failure is the USP wedge to design around.
5. **Positioning test:** message-test the USP line against the incumbent's tagline with the target community before committing to UI.

## Notes / caveats
- Both `ai-marketing-claude` and `gstack` are installed; their methodologies were applied by hand
  (not auto-invoked) because neither is registered as a `/command` in this session and plan mode
  is read-only. The `/market competitors <url>` command and `gstack scrape` should be run in an
  interactive session once a target URL exists.
- Market-size figures are directional (varying analyst methodologies) — use for relative scale.
