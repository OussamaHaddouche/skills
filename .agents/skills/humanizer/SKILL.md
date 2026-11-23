---
name: humanizer
version: 1.2.0
description: >-
  Remove AI writing tells from English or French prose. Use when editing or
  reviewing text that sounds generic, inflated, chatbot-like, clever-for-show,
  or like French management boilerplate (langue de bois), so it reads as
  natural human writing. Triggers: humanize, strip AI-isms, detect AI patterns,
  enlever les IA-ismes, réécrire moins IA, mémo / LinkedIn FR qui sonne ChatGPT.
license: MIT
metadata:
  author: Oussama Haddouche <oussama1haddouche2@gmail.com>
  tags:
    - writing
    - editing
    - prose
    - style
    - french
    - français
---

# Humanizer

Strip AI writing patterns and restore natural voice. English catalog based on
[Wikipedia:Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing),
plus later social/LLM tells. French catalog is language-native (not a
translation); see `references/patterns-fr.md` and `references/sources-fr.md`.

Pattern lists are descriptive, not ban lists. Do not accuse the author of using
AI. Make the text sound like a person wrote it on purpose.

## Purpose

Rewrite or audit drafts that sound machine-generated: inflated significance,
vague attributions, AI vocabulary clusters, chatbot manners, soulless
neutrality, French managerial boilerplate when relevant, and related tells.
Preserve meaning and facts. Match the genre's register. Stay in the source
language.

## Prerequisites

- Source text from the user (paste, selection, or file path)
- No API keys, tools, or network access required
- Optional: mode (`rewrite` / `detect`); language (`en` / `fr`); voice
  (`casual` / `professional` / `technical` / `warm` / `blunt`); register hint

## Modes

- **`rewrite`** (default) — fix justified patterns; return one final version
- **`detect`** — flag patterns only (clear problem vs judgment call); no rewrite

Trigger detect when the user says detect, flag only, audit only, scan,
seulement flaguer, juste vérifier, or similar.

## Severity (triage)

When time is short or the doc is long, fix in this order (see catalogs for
per-pattern grades where marked):

| Tier | Meaning | Examples |
| --- | --- | --- |
| **P0** | Credibility killers — always fix | Chatbot openers, sycophancy, cutoff disclaimers, generic "future looks bright" closers, placeholder leftovers, hashtag stuffing |
| **P1** | Obvious AI smell — fix before publish | Vocab clusters, significance inflation, vague experts, copula avoidance, synonym cycling, narrated candor, integrity theater |
| **P2** | Polish / context-dependent | Em-dash habit, rule of three, Title Case headings, isolated Tier-2 words |

Quick pass = P0+P1. Full pass = all three.

## Instructions

1. Validate input: if the user gave no text (and no file path to read), ask for
   the draft before rewriting. If a path is missing or unreadable, report that
   and stop; do not invent a substitute draft.
2. Read the full input. Decide mode (`rewrite` vs `detect`).
3. Choose language catalog:
   - Explicit `fr` / "en français" / "IA-ismes" → French
   - Explicit `en` / "in English" → English
   - Else: majority language of the draft (French function words and accents →
     `fr`; otherwise `en`). Mixed drafts: edit each span in its own language;
     do not translate.
   - **English:** load `references/patterns.md`
   - **French:** load `references/patterns-fr.md`
   Note which patterns actually appear. Do not "fix" absent problems.
4. Optional voice overlay (only if the user asked): `casual` / `professional` /
   `technical` / `warm` / `blunt`. Voice may recast how existing stance is
   expressed; it must not invent opinions, experience, or facts. With no voice
   request, preserve the source register.
5. Decide genre policy:
   - Essays, posts, narrative: restore personality where it fits (see Voice).
   - Neutral docs, reference, procedural, READMEs, product blurbs, mémos
     opérationnels: cut slop only; do not inject personality, wit, or "trust me"
     theater.
   - **French extra:** passif, nominalisation, and registre soutenu alone are
     not AI tells. Flag them only with other patterns or abnormal density.
6. Protected content: leave quotations, code, tables, URLs, paths, identifiers,
   and frontmatter unchanged unless the user explicitly includes them in scope.
   Report findings inside protected spans instead of rewriting them.
7. If mode is `detect`: return Issues found (by severity) + Assessment (clear
   vs judgment call). Stop. Do not rewrite.
8. If mode is `rewrite`: edit for concrete meaning and natural rhythm. Prefer
   specific claims over significance padding. Use plain predicates (EN: is/has;
   FR: est/a/fait). Prefer ordinary words for ordinary things. For blurbs: say
   what it does and when to use it. Delete lines that only prove cleverness or
   integrity.
9. Source fidelity: do not invent facts, names, dates, metrics, or first-person
   experience absent from the source. If a fix needs a missing concrete detail,
   cut the vague claim or flag the gap—do not fabricate.
10. Never inject (even to "sound human"): fabricated speaker perspective,
    manufactured stakes, forced contrarianism, performed candor ("let's be
    honest", "real talk"), em-dash theatrics, staccato fragment chopping, or
    unsupported specifics.
11. Replace curly quotes with straight quotes (" ') in editable prose (not
    inside protected quotations preserved verbatim).
12. Cold read, then optional second pass (max two editing passes total):
    - Sounds natural read aloud; sentence length varies
    - Specific details beat vague importance claims
    - Tone matches genre and sibling blurbs when editing a list
    - No chatbot manners, placeholders, or source-disclaimer theater
    - You did not swap one tell for another (rule-of-three, negative
      parallelism, performing cleverness / théâtre d'intégrité, fancy words,
      fake casual). If a line exists only to sound sharp or "more human," cut it.
    - Stop early when no justified in-scope edit remains.
13. Return the rewritten text in the source language, plus an optional brief
    change summary if the user is learning the patterns. Keep the reply focused
    on the rewrite; skip process narration.

For full walkthroughs: `references/example.md` (EN), `references/example-fr.md`
(FR).

## Voice

Avoiding AI patterns is half the job. Sterile, voiceless writing is another tell.
Overcorrecting into quirky slang is a third.

**Soulless signs:** same sentence length throughout; only neutral reportage; no
mixed feelings; no first person when the genre allows it; no humor or texture;
reads like a press release / note de direction vide.

**Fake-casual signs:** thesaurus colloquialisms nobody in this genre would pick
(EN: "puffed up", "mush", "vibes"; FR: *carrément*, *grave*, *vibes* collés dans
un mémo); forced slang in READMEs and docs; personality pasted on to prove the
text is human.

**When the genre allows voice:** have opinions; vary rhythm; acknowledge
complexity; use "I" / « je » when it fits and the source already has a speaker;
let some mess in. Personality must fit the piece—not be pasted on as a
humanizer finish.

**Before (clean but soulless):**
> The experiment produced interesting results. The agents generated 3 million
> lines of code. Some developers were impressed while others were skeptical.
> The implications remain unclear.

**After (has a pulse):**
> I genuinely don't know how to feel about this one. 3 million lines of code,
> generated while the humans presumably slept. Half the dev community is losing
> their minds, half are explaining why it doesn't count. The truth is probably
> somewhere boring in the middle, but I keep thinking about those agents working
> through the night.

## Pattern index

### English — `references/patterns.md`

| #   | Pattern                                   |
| --- | ----------------------------------------- |
| 1   | Significance / legacy inflation           |
| 2   | Vague "shaped the debate" claims          |
| 3   | Notability via outlet name-drops          |
| 4   | Sources "identify" the subject            |
| 5   | Vague "associated with" links             |
| 6   | Superficial -ing analyses                 |
| 7   | Vague experts / opinion laundering        |
| 8   | Challenges + upbeat outlook endings       |
| 9   | Canned awards/recognition blocks          |
| 10  | AI vocabulary clusters (by era)           |
| 11  | Copula avoidance (serves as / boasts)     |
| 12  | Negative parallelisms (not X, but Y)      |
| 13  | Rule of three                             |
| 14  | Elegant variation / synonym cycling       |
| 15  | False ranges (from X to Y)                |
| 16  | Formulaic em dashes                       |
| 17  | Mechanical boldface                       |
| 18  | `**Label:**` vertical lists               |
| 19  | Title Case headings                       |
| 20  | Emoji decoration                          |
| 21  | Curly quotes                              |
| 22  | Chatbot collaborative voice               |
| 23  | Knowledge/source hedging theater          |
| 24  | Sycophantic tone                          |
| 25  | Placeholder / template leftovers          |
| 26  | Filler phrases                            |
| 27  | Excessive hedging                         |
| 28  | Generic positive endings                  |
| 29  | Performing cleverness / integrity theater |
| 30  | Unnecessary fancy / shop words            |
| 31  | Fake casual / forced colloquialism        |
| 32  | Narrated candor / performed honesty       |
| 33  | Lingering-attention / share-post openers  |
| 34  | Hedge-stacked predictions                 |
| 35  | Infomercial engagement hooks              |
| 36  | AI-tool fingerprints (citations, UTM)     |
| 37  | Hashtag stuffing                          |
| 38  | Bare noun-phrase bullet dumps             |

Also fix weaker EN signals when present: travel-brochure adjectives,
knowledge-cutoff one-liners, prompt-refusal leftovers.

### French — `references/patterns-fr.md`

Load the FR file for the full list (tiers + before/afters). Headline groups:

- Vocabulaire Tier 1 / 2 / 3 (*crucial*, *réinventé*, *Dans le paysage actuel…*)
- Contenu: inflation de sens, sources vagues, défis formulaïques
- Langue: évitement de copule (*s'inscrit dans*), transitions, hedges
- Structure: uniformité, puces nominales, trilogie forcée
- Communication: ouvertures chatbot, « Plongeons dans… », clôtures génériques
- Spécifique FR: langue de bois managériale, formules impersonnelles
  (*Il s'avère que…*), hashtag stuffing, listes de substantifs managériaux
- Humanisation ratée: théâtre d'intégrité, mots savants inutiles, faux décontracté

## Examples

### Short rewrite (EN)

**Before:**
> Additionally, the platform serves as a vital hub, fostering alignment and
> showcasing innovative solutions in today's evolving landscape.

**After:**
> The platform is a hub where teams share tools and post new work.

### Short rewrite (FR)

**Before:**
> Dans le paysage actuel de la transformation digitale, il est crucial de noter
> que notre solution s'inscrit dans une démarche innovante au cœur de
> l'écosystème.

**After:**
> Notre outil centralise les tickets d'incident pour les équipes support à Lyon.

### Product / README blurb (EN)

**Before:**
> Rewrites prose and vague bullets. No fake metrics, no "I led it" when you
> didn't. Not for life advice or salary negotiation.

**After:**
> Works on CVs, LinkedIn, and portfolios. Helps turn vague job lines into clear
> achievements a recruiter can understand.

### Full rewrites

- EN: `references/example.md`
- FR: `references/example-fr.md`

## Output format

### Rewrite mode

1. The rewritten text (same language as the source)
2. Optional: brief change summary (pattern names fixed, not a lecture)

### Detect mode

1. **Issues found** — bulleted findings with quoted spans, grouped P0 / P1 / P2
2. **Assessment** — clear problems vs judgment calls; say if the text is clean

## Limitations

- Does not prove or detect whether a human used AI; it edits style only
- Will not invent facts, quotes, citations, or anecdotes to sound more human
- Neutral/technical docs get cleanup, not personality injection
- One or two "AI vocabulary" words alone are not enough to rewrite; fix clusters
- French passif / nominalisation / registre soutenu alone are out of scope as
  AI tells
- Wikipedia-specific artifacts are out of scope unless the user is editing
  Wikipedia content
- Overlap with broader prose skills (for example Clarity): use this skill when
  the ask is specifically to strip AI tells / humanize machine-sounding text

## Troubleshooting

| Problem                       | Cause                                                             | Fix                                                         |
| ----------------------------- | ----------------------------------------------------------------- | ----------------------------------------------------------- |
| No draft to edit              | User invoked the skill without text or a path                     | Ask for the source text; do not generate filler             |
| Used EN catalog on FR text    | Language routing skipped                                          | Reload `patterns-fr.md`; do not translate EN rules          |
| Flagged passif as AI (FR)     | Treated English heuristics as universal                           | Passif/nominalisation alone are not FR AI tells             |
| Output still sounds flat      | Only deleted AI words; left press-release rhythm                  | Restore voice for the genre; vary sentence length           |
| Output feels fake-casual      | Injected slang or personality into neutral docs                   | Use the ordinary word; cut slop only                        |
| Output still "AI but sharper" | Swapped inflation for clever won't-lists / mini anti-examples     | Cut performing cleverness / théâtre d'intégrité             |
| Output still sounds "smart"   | Replaced fog with shop words                                      | Use the ordinary word unless precision needs the term       |
| Invented metrics / anecdotes  | "Humanized" by fabricating detail                                 | Cut fluff or ask; never invent facts                        |
| Blurb doesn't match siblings  | Over-edited one entry into a different voice                      | Match nearby register; same length energy                   |
| Meaning drifted               | Significance padding replaced with new claims                     | Preserve facts; delete fluff instead of inventing detail    |
| Over-edited                   | Treated the pattern list as a ban list                            | Fix only patterns that appear; leave clean sentences alone  |
| User wanted feedback only     | Rewrote when they asked for a review                              | Use detect mode; notes only                                 |

## Reference

- English patterns: `references/patterns.md`
- French patterns: `references/patterns-fr.md`
- French sources: `references/sources-fr.md`
- Examples: `references/example.md`, `references/example-fr.md`
- EN upstream: [Wikipedia:Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing)
- EN practice inspiration: [avoid-ai-writing](https://github.com/conorbronsdon/avoid-ai-writing)
- FR pattern research (MIT, adapted): [avoid-ai-writing-multilingual](https://github.com/jurigis/avoid-ai-writing-multilingual)

LLMs regress toward the statistically safe sentence in every language.
Specific, uneven, slightly imperfect human prose is the goal.
