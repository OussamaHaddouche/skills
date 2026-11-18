---
name: humanizer
version: 1.0.0
description: >-
  Remove AI writing tells from text. Use when editing or reviewing prose that
  sounds generic, inflated, or chatbot-like so it reads as natural human writing.
license: MIT
metadata:
  author: Oussama Haddouche <oussama1haddouche2@gmail.com>
  tags:
    - writing
    - editing
    - prose
    - style
---

# Humanizer

Strip AI writing patterns and restore natural voice. Based on
[Wikipedia:Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing),
adapted for general prose (not Wikipedia detection).

The Wikipedia list is descriptive, not a ban list. Many patterns also appear in
human editorial and PR writing. Do not accuse the author of using AI. Make the
text sound like a person wrote it on purpose.

## Purpose

Rewrite drafts that sound machine-generated: inflated significance, vague
attributions, AI vocabulary clusters, chatbot manners, soulless neutrality, and
related tells. Preserve meaning and facts. Match the genre's register.

## Prerequisites

- Source text from the user (paste, selection, or file path)
- No API keys, tools, or network access required
- Optional: user states the target register (formal docs, essay, casual post)

## Instructions

1. Validate input: if the user gave no text (and no file path to read), ask for
   the draft before rewriting. If a path is missing or unreadable, report that
   and stop; do not invent a substitute draft.
2. Read the full input.
3. Load `references/patterns.md` and note which patterns actually appear.
   Do not "fix" absent problems.
4. Decide voice policy from genre:
   - Essays, posts, narrative: restore personality where it fits (see Voice).
   - Neutral docs, reference, procedural: cut slop only; do not inject personality.
5. Rewrite for concrete meaning and natural rhythm. Prefer specific claims over
   significance padding. Use "is"/"has"/plain verbs where a human would.
6. Replace curly quotes with straight quotes (" ').
7. Check the result:
   - Sounds natural read aloud; sentence length varies
   - Specific details beat vague importance claims
   - Tone matches the genre
   - No chatbot manners, placeholders, or source-disclaimer theater
8. Return the rewritten text, plus an optional brief change summary if the user
   is learning the patterns.
9. Do not mention this skill unless asked.

For a full before/after walkthrough, see `references/example.md`.

## Voice

Avoiding AI patterns is half the job. Sterile, voiceless prose is another tell.

**Soulless signs:** same sentence length throughout; only neutral reportage; no
mixed feelings; no first person when the genre allows it; no humor or texture;
reads like a press release.

**When the genre allows voice:** have opinions; vary rhythm; acknowledge
complexity ("impressive and a little unsettling"); use "I" when it fits; let
some mess in; be specific about feelings.

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

Consult `references/patterns.md` for words-to-watch, problems, and before/afters.

| # | Pattern |
|---|---------|
| 1 | Significance / legacy inflation |
| 2 | Vague "shaped the debate" claims |
| 3 | Notability via outlet name-drops |
| 4 | Sources "identify" the subject |
| 5 | Vague "associated with" links |
| 6 | Superficial -ing analyses |
| 7 | Vague experts / opinion laundering |
| 8 | Challenges + upbeat outlook endings |
| 9 | Canned awards/recognition blocks |
| 10 | AI vocabulary clusters (by era) |
| 11 | Copula avoidance (serves as / boasts) |
| 12 | Negative parallelisms (not X, but Y) |
| 13 | Rule of three |
| 14 | Elegant variation / synonym cycling |
| 15 | False ranges (from X to Y) |
| 16 | Formulaic em dashes |
| 17 | Mechanical boldface |
| 18 | `**Label:**` vertical lists |
| 19 | Title Case headings |
| 20 | Emoji decoration |
| 21 | Curly quotes |
| 22 | Chatbot collaborative voice |
| 23 | Knowledge/source hedging theater |
| 24 | Sycophantic tone |
| 25 | Placeholder / template leftovers |
| 26 | Filler phrases |
| 27 | Excessive hedging |
| 28 | Generic positive endings |

Also fix weaker signals when present: travel-brochure adjectives, knowledge-cutoff
one-liners, prompt-refusal leftovers.

## Examples

### Short rewrite

**Before:**
> Additionally, the platform serves as a vital hub, fostering alignment and
> showcasing innovative solutions in today's evolving landscape.

**After:**
> The platform is a hub where teams share tools and post new work.

### Full essay rewrite

See `references/example.md` for a multi-paragraph before/after with a change list.

## Output format

1. The rewritten text
2. Optional: a brief change summary (pattern names fixed, not a lecture)

## Limitations

- Does not prove or detect whether a human used AI; it edits style only
- Will not invent facts, quotes, citations, or anecdotes to sound more human
- Neutral/technical docs get cleanup, not personality injection
- One or two "AI vocabulary" words alone are not enough to rewrite; fix clusters
- Wikipedia-specific artifacts (wikitext, AfC boilerplate, DOI hallucinations)
  are out of scope unless the user is editing Wikipedia content
- Overlap with broader prose skills (for example Clarity): use this skill when
  the ask is specifically to strip AI tells / humanize machine-sounding text

## Troubleshooting

| Problem | Cause | Fix |
|---------|-------|-----|
| No draft to edit | User invoked the skill without text or a path | Ask for the source text; do not generate filler |
| Output still sounds flat | Only deleted AI words; left press-release rhythm | Restore voice for the genre; vary sentence length |
| Output feels fake-casual | Injected slang, typos, or personality into neutral docs | Cut slop only; match the original register |
| Meaning drifted | Significance padding replaced with new claims | Preserve facts; delete fluff instead of inventing detail |
| Over-edited | Treated the pattern list as a ban list | Fix only patterns that appear; leave clean sentences alone |
| User wanted feedback only | Rewrote when they asked for a review | Return notes keyed to pattern names; do not rewrite |

## Reference

- Pattern catalog: `references/patterns.md`
- Full example: `references/example.md`
- Upstream: [Wikipedia:Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing)

Wikipedia's core insight still holds: LLMs regress toward the statistically safe
sentence. Specific, uneven, slightly imperfect human prose is the goal.
