# AI writing patterns

Catalog adapted from [Wikipedia:Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing).
Descriptive, not a ban list. Fix only patterns that actually appear.

## Content patterns

### 1. Undue emphasis on significance, legacy, and broader trends

**Words to watch:** stands/serves as, is a testament/reminder, crucial/pivotal/
vital/significant/key role/moment, underscores/highlights its importance,
reflects broader, symbolizing its ongoing/enduring/lasting, contributing to the,
setting the stage for, marking/shaping the, represents/marks a shift, key turning
point, evolving landscape, focal point, indelible mark, deeply rooted,
"distinction matters because..."

**Problem:** LLMs puff up importance and tie mundane facts to sweeping themes.
They may even hedge that the topic is minor, then lecture about its importance
anyway. In biology/ecology text, they over-connect species to "the ecosystem"
and belabor conservation when nothing specific is known.

**Before:**
> The Statistical Institute of Catalonia was officially established in 1989,
> marking a pivotal moment in the evolution of regional statistics in Spain.
> This initiative was part of a broader movement across Spain to decentralize
> administrative functions and enhance regional governance.

**After:**
> The Statistical Institute of Catalonia was established in 1989 to collect and
> publish regional statistics independently from Spain's national statistics
> office.

### 2. Claims of shaping discussions or debates

**Words to watch:** has/have shaped conversations/discussions/debate about,
prompted broader reflection, remains part of debates

**Problem:** The model situates the subject in vague public "discussions" about
adjacent topics, often with a rule-of-three list of lofty themes
(authenticity, consent, dignity...).

**Before:**
> The phenomenon has generated debate about authenticity, consent, and the
> psychological effects of digitally extending personhood.

**After:**
> Critics have asked whether a chatbot trained on someone's texts can consent
> to speak as them after they die.

### 3. Undue emphasis on notability, media coverage, and source type

**Words to watch:** independent coverage, local/regional/national media outlets,
trade publications, cited/featured/profiled in, music/business/tech outlets

**Problem:** The text proves importance by name-dropping outlets and dwelling on
what kind of sources exist, instead of saying what those sources actually report.

**Before:**
> Her views have been cited in The New York Times, BBC, Financial Times, and
> The Hindu. She maintains an active social media presence with over 500,000
> followers.

**After:**
> In a 2024 New York Times interview, she argued that AI regulation should focus
> on outcomes rather than methods.

### 4. Undue emphasis on how sources "identify" the subject

**Words to watch:** databases/records/listings/filings identify/list/describe
[subject] as, was identified by [source] as, is listed in, professional profile
lists

**Problem:** Common in mid-2026+ output. Primary or tertiary sources get framed
as solemnly "identifying" someone, in stiff formulaic prose.

**Before:**
> His personal website identifies him as a retired IAS officer associated with
> the 1982 batch.

**After:**
> He is a retired IAS officer from the 1982 batch.

### 5. Vague connection or association

**Words to watch:** in connection with/to, connected with/to, in association
with, associated with, particularly/widely associated

**Problem:** Instead of stating the relationship ("was CEO of", "taught at"),
the text says someone was "associated with leadership of" or "connected with"
a field.

**Before:**
> In 2017, sources identified John Doe as being associated with leadership of
> ExampleCorp.

**After:**
> In 2017, John Doe was CEO of ExampleCorp.

### 6. Superficial -ing analyses

**Words to watch:** highlighting/underscoring/emphasizing..., ensuring...,
reflecting/symbolizing..., contributing to..., cultivating/fostering...,
encompassing..., enhancing..., valuable insights, align/resonate with

**Problem:** Present-participle tack-ons add fake depth. With retrieval-augmented
chatbots, these may be pinned on named sources that never said anything of the
sort ("Roger Ebert highlighted the lasting influence").

**Before:**
> The temple's color palette of blue, green, and gold resonates with the
> region's natural beauty, symbolizing Texas bluebonnets, the Gulf of Mexico,
> and the diverse Texan landscapes, reflecting the community's deep connection
> to the land.

**After:**
> The temple uses blue, green, and gold. The architect said these reference
> local bluebonnets and the Gulf coast.

### 7. Vague attributions and opinion laundering

**Words to watch:** observers/critics/experts/scholars/reviewers note/argue/
believe (with no names), industry reports, several sources (when few are cited),
widely interpreted as

**Problem:** Opinions get attributed to vague authorities, or one source is
inflated into a chorus.

**Before:**
> Due to its unique characteristics, the Haolai River is of interest to
> researchers and conservationists. Experts believe it plays a crucial role in
> the regional ecosystem.

**After:**
> The Haolai River supports several endemic fish species, according to a 2019
> survey by the Chinese Academy of Sciences.

### 8. Formulaic challenges / future outlook endings

**Words to watch:** Despite its... faces several challenges, Despite these
challenges, Challenges and Legacy, Future Outlook, continues to thrive,
positions them as critical

**Problem:** Rigid outline leftover: challenges paragraph, then a vaguely
upbeat pivot. Fix the formula, not the mere mention of real problems.

**Before:**
> Despite its industrial prosperity, Korattur faces challenges typical of urban
> areas, including traffic congestion and water scarcity. Despite these
> challenges, with its strategic location and ongoing initiatives, Korattur
> continues to thrive as an integral part of Chennai's growth.

**After:**
> Traffic congestion increased after 2015 when three new IT parks opened. The
> municipal corporation began a stormwater drainage project in 2022 to address
> recurring floods.

### 9. "Awards and recognition" as a canned prestige block

**Problem:** An "Awards and recognition" (or bare "Recognition") section that
mostly proves legacy via accolades and vague "coverage," rather than explaining
what the subject did.

**Fix:** Keep notable awards if they matter. Cut the rest or fold one or two
concrete wins into the narrative. Do not keep a trophy shelf for its own sake.

## Language and grammar

### 10. High density of AI vocabulary

One or two of these words can be coincidence. A cluster is a tell. Prefer plain
synonyms. Do not assume every synonym of an AI word is also tainted; the research
is about specific tokens.

**Era cheat sheet (approximate):**

| Period | Overused words |
|--------|----------------|
| 2023–mid-2024 | Additionally, boasts, bolstered, crucial, delve, emphasizing, enduring, garner, intricate/intricacies, interplay, key, landscape, meticulously, pivotal, underscore, tapestry, testament, valuable, vibrant |
| Mid-2024–mid-2025 | align with, bolstered, crucial, emphasizing, enhance, enduring, fostering, highlighting, pivotal, showcasing, underscore, vibrant |
| Mid-2025–mid-2026 | emphasizing, enhance, highlighting, showcasing (plus notability/attribution canned phrases) |
| Mid-2026+ | challenge, clearer, dependable, echoed, foster, leverage, matters, multifaceted, practical, prioritize, quietly, steady, universally; often shorter sentences and heavier comma/period use |
| Grok-ish extras | causal, empirical, correlate, underscore |

**Before:**
> Additionally, a distinctive feature of Somali cuisine is the incorporation of
> camel meat. An enduring testament to Italian colonial influence is the
> widespread adoption of pasta in the local culinary landscape, showcasing how
> these dishes have integrated into the traditional diet.

**After:**
> Somali cuisine also includes camel meat, considered a delicacy. Pasta dishes
> introduced during Italian colonization remain common, especially in the south.

### 11. Copula avoidance (evading "is" / "are")

**Words to watch:** serves as, stands as, marks, represents, boasts, features,
offers, refers to (for things that simply are), ventured into... as,
began... as (when "was" would do)

**Problem:** Simple predicates get replaced with marketing verbs or elaborate
workarounds. In definitions, "X refers to..." is used when "X is..." is clearer.

**Before:**
> Gallery 825 serves as LAAA's exhibition space for contemporary art. The
> gallery features four separate spaces and boasts over 3,000 square feet.

**After:**
> Gallery 825 is LAAA's exhibition space for contemporary art. The gallery has
> four rooms totaling 3,000 square feet.

### 12. Negative parallelisms

**Forms:**
- Not only X, but also Y
- It's not just X, it's Y
- Not X, but Y / no X, no Y, just Z
- Y rather than X (common in newer output)
- Product-copy cousins: "No fake metrics, no inflated titles, no AI slop"

**Problem:** Fake correction of a misconception the reader never had. In blurbs,
stacked "no/won't" lines often pair with pattern 29 (performing cleverness).

**Before:**
> It's not just about the beat riding under the vocals; it's part of the
> aggression and atmosphere. It's not merely a song, it's a statement.

**After:**
> The heavy beat adds to the aggressive tone.

### 13. Rule of three

**Problem:** Ideas forced into triads to sound complete: adjectives, noun
phrases, or "innovation, inspiration, and industry insights."

**Before:**
> The event features keynote sessions, panel discussions, and networking
> opportunities. Attendees can expect innovation, inspiration, and industry
> insights.

**After:**
> The event includes talks and panels, with time to talk between sessions.

### 14. Elegant variation (synonym cycling)

**Problem:** Older models with repetition penalties cycle synonyms so hard that
reference tracking breaks ("protagonist" / "main character" / "central figure" /
"hero").

**Before:**
> The protagonist faces many challenges. The main character must overcome
> obstacles. The central figure eventually triumphs. The hero returns home.

**After:**
> The protagonist faces many challenges but eventually triumphs and returns
> home.

### 15. False ranges

**Problem:** "From X to Y" where X and Y are not endpoints on a real scale.

**Before:**
> Our journey through the universe has taken us from the singularity of the Big
> Bang to the grand cosmic web, from the birth and death of stars to the
> enigmatic dance of dark matter.

**After:**
> The book covers the Big Bang, star formation, and current theories about dark
> matter.

## Style and formatting

### 16. Em dashes

**Problem:** Formulaic em-dash rhythm that mimics punchy sales copy, often with
spaces around the dash. Useful together with other tells, not alone.

**Note (as of late 2026):** Some newer models are steered to avoid em dashes
almost entirely. That can produce the opposite artifact: sentences glued only
with commas and periods, with little punctuation variety. Do not strip every
em dash on principle. Fix the mechanical ones; keep an em dash if a human
writer would actually want it.

**Before:**
> The term is primarily promoted by Dutch institutions — not by the people
> themselves. You don't say "Netherlands, Europe" as an address — yet this
> mislabeling continues — even in official documents.

**After:**
> The term is primarily promoted by Dutch institutions, not by the people
> themselves. You don't say "Netherlands, Europe" as an address, yet this
> mislabeling continues in official documents.

### 17. Boldface for emphasis

**Problem:** Mechanical bold on phrases or on every list label.

**Before:**
> It blends **OKRs (Objectives and Key Results)**, **KPIs (Key Performance
> Indicators)**, and visual strategy tools such as the **Business Model Canvas**.

**After:**
> It blends OKRs, KPIs, and visual strategy tools like the Business Model Canvas.

### 18. Inline-header vertical lists

**Problem:** Bullet lists where every item is `**Label:** explanation`.

**Before:**
> - **User Experience:** The user experience has been significantly improved
>   with a new interface.
> - **Performance:** Performance has been enhanced through optimized algorithms.
> - **Security:** Security has been strengthened with end-to-end encryption.

**After:**
> The update improves the interface, speeds up load times, and adds end-to-end
> encryption.

### 19. Title Case headings

**Problem:** Section titles in Title Case Like A Marketing Brochure.

**Before:**
> ## Strategic Negotiations And Global Partnerships

**After:**
> ## Strategic negotiations and global partnerships

### 20. Emoji decoration

**Problem:** Emoji prefixes on headings or bullets as fake structure.

**Before:**
> Launch Phase: The product launches in Q3
> Key Insight: Users prefer simplicity

**After:**
> The product launches in Q3. User research showed a preference for simplicity.

### 21. Curly quotes

Replace curly quotes (“ ” ‘ ’) with straight quotes (" ').

## Communication artifacts (chatbot paste leftovers)

### 22. Collaborative / assistant voice

**Words to watch:** I hope this helps, Of course!, Certainly!, Great question!,
You're absolutely right!, Would you like..., Let me know if..., Here is a...,
Happy to help, as an AI language model

**Problem:** User-facing chatbot manners pasted into content.

**Before:**
> Here is an overview of the French Revolution. I hope this helps! Let me know
> if you'd like me to expand on any section.

**After:**
> The French Revolution began in 1789 when financial crisis and food shortages
> led to widespread unrest.

### 23. Hedging disclaimers about sources and knowledge

**Words to watch:**
- While specific details are limited/scarce/not widely available...
- based on available information / in the provided sources / search results
- maintains a low profile / keeps personal details private (when speculative)
- should be treated/presented as... rather than...
- does not by itself establish...
- should not be confused with...
- Up to my last knowledge update / as of my last training update

**Problem:** The model narrates its uncertainty, source gaps, or "corrective
framing" instead of writing the claim or omitting it. Mid-2026+ output often
adds "treat as X rather than Y" disclaimers.

**Before:**
> While specific details about the company's founding are not extensively
> documented in readily available sources, it appears to have been established
> sometime in the 1990s.

**After:**
> The company was founded in 1994, according to its registration documents.

(Or delete the sentence if you do not have a source.)

### 24. Sycophantic tone

**Before:**
> Great question! You're absolutely right that this is a complex topic. That's
> an excellent point about the economic factors.

**After:**
> The economic factors you mentioned matter here.

### 25. Phrasal templates and placeholders

**Words to watch:** `[Insert ...]`, `[Your Name]`, `TODO`, `TBD`,
`INSERT_SOURCE_URL`, `example.com/source1`, `2025-XX-XX`, fill-in-the-blank
Mad Libs sentences left unfilled

**Problem:** Draft scaffolding leaked into final prose.

**Fix:** Fill with real content or remove. Never leave bracket placeholders in
output you are asked to finalize.

## Filler and hedging

### 26. Filler phrases

| Cut | Prefer |
|-----|--------|
| In order to achieve this goal | To achieve this |
| Due to the fact that | Because |
| At this point in time | Now |
| In the event that | If |
| Has the ability to | Can |
| It is important to note that | (just state the thing) |
| In summary / In conclusion / Overall | (delete, or say the actual point) |

### 27. Excessive hedging

**Before:**
> It could potentially possibly be argued that the policy might have some effect
> on outcomes.

**After:**
> The policy may affect outcomes.

### 28. Generic positive endings

**Before:**
> The future looks bright. Exciting times lie ahead as they continue their
> journey toward excellence.

**After:**
> The company plans to open two more locations next year.

### 29. Performing cleverness / integrity theater

**Forms:**
- Stacked refusals: "No X, no Y, no Z" / "Won't A. Won't B. Won't C."
- Mini anti-examples that stage a fake dialogue: turn "I helped" into "I led"
- Quippy proof of virtue in product blurbs / READMEs / skill descriptions
- Out-of-scope trailers on short blurbs: "Not for life advice or salary
  negotiation." / "This is not legal advice." when siblings only say what the
  thing *is* for
- "Rewrites only what you can defend/back up" virtue clauses that add no product
  fact
- Lines that exist to sound sharp or trustworthy, not to add information

**Problem:** After cutting classic AI fog, models often replace it with a
different tell: performed wit and integrity. The reader of a README blurb
wanted what it does and when to open it. Scope refusals belong in the skill
body (or docs), not as a punchy closer. Humans writing a short blurb usually
say what the thing does and stop.

**Before:**
> Digs for real achievements and rewrites only what you can defend. No fake
> metrics, no "I led it" when you didn't. Not for life advice or salary
> negotiation.

**After:**
> Works on CVs, LinkedIn, and portfolios. Helps turn vague job lines into clear
> achievements a recruiter can understand.

**Keep when real:** a concrete behavior note that changes how you use the tool
("Won't edit your files unless you ask it to implement"). Cut when it's only
branding a boundary.

**Also watch:** parenthetical laundry lists of edge cases jammed into one
sentence ("including risk and timeline trust, overqualified vibes, and…") when
the surrounding blurbs stay short and plain.

### 30. Unnecessary fancy / shop words

**Problem:** The model picks a slightly elevated or in-group word when a plain
one would do. Reads as trying to sound like a writer or an expert in a context
that is just a README, UI string, or casual note.

**Words to watch (when the audience doesn't need the term):**
prose, bullets (for resume lines), leverage, utilize, facilitate, articulate,
narrative, artifact, surface (as a verb), unpack, craft, delve, landscape,
space (as in "in the X space"), messaging, framing, cadence, register (outside
linguistics docs), "materials" when "CV" or "profile" is clearer

**Keep when earned:** technical docs talking to practitioners ("ATS parse",
"Boolean search"), or when the precise term prevents ambiguity.

**Before:**
> Rewrites prose so vague bullets become clear achievements.

**After:**
> Fixes writing so vague job lines become clear achievements.

**Test:** Is this the normal word for this context, or a fancier synonym? If
you'd swap mid-sentence for a simpler one, use the simpler one.

### 31. Fake casual / forced colloquialism

**Problem:** After being told to sound human, the model overcorrects. It swaps
plain words for quirky informal ones to *perform* casualness. That is still a
tell—especially in READMEs, docs, and product blurbs, where real humans use
boring accurate words.

**Opposite of pattern 30:** 30 is prestige elevation; 31 is thesaurus-slang
dress-down. Both avoid the ordinary word.

**Words / moves to watch:**
puffed up (for inflated), mush (for vague), vibes (for tone/feel), crunchy,
juicy, spicy (as metaphor for emphasis), "hits different", "low-key", "high-key",
forced "weirdly X" stacks, cute metaphors that the surrounding copy never uses

**Before:**
> Reach for it when a draft feels generic, puffed up, or weirdly polite. When
> your LinkedIn is mush.

**After:**
> Reach for it when a draft feels generic, inflated, or oddly polite. When your
> LinkedIn is vague.

**Keep when earned:** the writer's real voice in a personal essay, chatty blog,
or dialogue—where that slang already fits the piece. Do not paste it onto
neutral docs as a finishing coat.

**Test:** Would this word appear in a careful human README, or only in a model
trying not to sound like a model? Prefer the boring accurate word.

## Historical / weaker signals

Still fix these when they appear, but do not treat them as proof of AI on their
own. Frequency has dropped in newer models unless the user asked for hype.

### Promotional / travel-brochure language (common 2023–2025)

**Words to watch:** boasts a, vibrant, rich (figurative), profound, nestled,
in the heart of, groundbreaking, renowned, breathtaking, must-visit, stunning,
diverse array, seamless, commitment to

**Before:**
> Nestled within the breathtaking region of Gonder in Ethiopia, Alamata Raya
> Kobo stands as a vibrant town with a rich cultural heritage and stunning
> natural beauty.

**After:**
> Alamata Raya Kobo is a town in the Gonder region of Ethiopia, known for its
> weekly market and 18th-century church.

### Knowledge-cutoff one-liners (mostly 2022–2023)

Remove lines like "As of my last knowledge update in January 2022..."

### Prompt-refusal leftovers

Remove "As an AI language model, I cannot..." scaffolding if it leaked into
draft content.

## Prefer human-like syntax

When rewriting, lean toward constructions that are common in human writing and
underrepresented in LLM output:

- Simple predicates: "is", "are", "has"
- Plain verbs: wrote, moved, used, tried, died (not authored/relocated/utilized/
  attempted/passed away unless that register is earned)
- Ordinary nouns for ordinary things (see pattern 30): writing not prose, job
  lines not bullets, unless the precise term earns its place
- Ordinary register for the genre (see pattern 31): inflated not puffed up;
  vague not mush—unless that slang already belongs in the piece
- Occasional blunt superlatives or specifics when true: "the only", "the first"
- Natural qualifiers where you actually mean them: very, perhaps, tends to
- Direct relationships over "associated with"

Do not mechanically reverse every formal word. Stop chasing elegant variation,
prestige vocabulary, *and* quirky casual synonyms for their own sake.

## Wikipedia-only (out of scope)

Handle only if the user is editing Wikipedia content: wikitext/markdown
irregularities, citation DOI hallucinations, AI edit-summary formulae, AfC
submission artifacts, user-page boilerplate, and permissions-gaming signals.
