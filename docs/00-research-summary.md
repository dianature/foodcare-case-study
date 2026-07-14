# Research summary: do people 20 to 40 actually need a recipe app?

> Participants are pseudonymised (P3, P6, P9, P10, P11). Raw recordings, transcripts, and chat screenshots are held privately and are not part of this repository.

## How I ran it

I mixed two methods to get both breadth and depth. In total I asked 14 people the core questions, and I went deep with 4 of them: three recorded interviews (P3, P6, P10) and one written chat survey (P9). The interviews I transcribed with Whisper, then read the chat screenshots by hand. The sample is small, so I treat the counts as direction rather than proof, and I lean on what people said in their own words.

**Sample:** 14 people asked, 4 of them in depth. Ages roughly 25 to 40, Ukrainian, several living abroad. Mixed: single, couple, parent.

## The numbers

Across everyone I asked (14):

| Question | Result |
|---|---|
| People asked in total | 14 |
| Ever used a dedicated recipe app | **2 of 14** |
| Still use a recipe app today | **0 of 14** |
| Where they get recipes now | Instagram, TikTok, Google search, ChatGPT or Claude, or cooking what they already know |

From the 4 I went deep with:

| Question | Result |
|---|---|
| Currently use a dedicated recipe app | 0 of 4 |
| Tried a recipe app and dropped it, or refuse outright | 2 of 4 (P3 tried and deleted, P9 refuses) |
| Find recipes on social feeds or AI assistants | 4 of 4 |
| Save recipes somewhere | 1 of 4 (P6, and cannot find them later) |
| Cook around someone else's restriction | 2 of 4 (P3, P6) |
| Order delivery regularly | 0 of 4 |

The headline is blunt. Only 2 of the 14 people had ever used a dedicated recipe app, and none use one today. The recipes themselves are never the missing piece.

## What hurts, in order

1. **The daily decision is the tax, not the cooking.** P6 named it best. The load is deciding, every single day, and it spikes when both partners work.
2. **Saved recipes turn into a graveyard.** P6 saves everything into one phone folder and then cannot find anything among about a hundred items.
3. **People refuse app overload and manual tracking.** P9 will not install more apps and will not keep a food diary, even though she is curious about a FODMAP diet.
4. **Cooking around a restriction is real and unsupported.** P3 buys lactose-free for his wife. P6 cooks around her daughter's fish allergy and around vegetarian friends.
5. **Health goals exist without the patience for logging.** P9 wants to hit her protein, and P10 raised protein and peptide support. Neither wants a diary to get there.

## What people asked for, unprompted

- **Cook from what I have.** P6 and P3 both want "here is my fridge, tell me what to make."
- **Substitutions.** P6's strongest wish was swapping an ingredient or a spice when something is missing.
- **Effort level.** P3 wants to pick recipe difficulty and keep it minimal.
- **Light personal notes on recipes,** with the honest caveat that a bad result is sometimes the cook and not the recipe.
- **Protein-first eating** without a tracker (P9, P10).

## The quotes that moved the design

Interviews were conducted in Russian. Translations are mine.

- P9: "I do not need a recipe app."
- P9: "I am not going to dig through a hundred thousand apps."
- P9: "You have to keep a food diary, and I cannot be bothered."
- P6: "There is a joke about what adult life is: thinking every day about what to cook. When both of you work, it is exhausting."
- P6: "There are about a hundred recipes in there and it takes me ages to find and remember."
- P6: "What can replace an ingredient or a spice when you are out. That is the interesting part."
- P6: "In ChatGPT you can type in your fridge and it tells you what to cook."
- P3: "I search from scratch every time, and that suits me."
- P3: "I open the fridge and decide by what is there."
- P3, on recipe apps: "Looked at it and deleted it, got no convenience from it."

## How this changed my direction

Before these talks I was still holding the generic brief: a recipe app for everyone 20 to 35. The research killed that. A general recipe library solves a problem nobody in my sample has, because recipes are already everywhere and free.

What the data pushed me toward is narrower. I had to build for a specific person with a concrete reason, and remove friction instead of adding another library. Three pulls came through.

- **Decision and repertoire, for busy cooks.** P6 is the case: cut the daily "what do I make" load and make her own hundred saved recipes usable again.
- **Pantry and substitutions.** P6 and P3 both want "cook from my fridge" and "swap what I am missing." That is a concrete assistant, not a feed.
- **Goal or restriction, without a diary.** P9 and P10 want health outcomes but refuse manual logging. P3 and P6 already cook around other people's restrictions. This became the caregiver direction.

One more warning came out of the research. Any of these has to live where people already are, close to social feeds and to tools like ChatGPT, and it cannot ask for another install or a daily diary. P9 drew that line for me in a single message.
