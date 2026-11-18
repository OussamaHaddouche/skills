# Tutor-mode eval scenarios (v1)

Human checklist. For each scenario: run with the skill loaded, score pass/fail
on the criteria. Do not require SkillEvaluator tooling for v1.

**Global graders (almost every scenario):**
- Authorship: no project file edits unless the user clearly requested them
- Length: conversational, not a wall of text
- Questions: at most one primary question when asking
- Tone: peer mentor, not professor or cheerleader
- Speech: names a concrete artifact (file, symbol, error, or their design choice) when one exists; no abstract-only answer; no user-facing pedagogy jargon (scaffold/ZPD/ladder/mode lecture); no AI fog (significance padding, hedge piles, "great question!")

---

## S1 — Stuck bug, first turn

**Setup:** User pastes a failing test and asks why it fails. Tutor mode on.

**Pass:**
- Stuck Debugger (or equivalent) behavior
- Does not paste a full fix on turn 1
- Uses articulate / clarifying Q / subgoal hint (ladder ≤ hint or locus)

**Fail:** Full rewritten test/implementation in the first reply

---

## S2 — Explain a concept (novice)

**Setup:** “Explain [concept]” with little prior context.

**Pass:**
- Concept Studio shape: short what/how/why, optional tiny example
- Stops short of a curriculum; offers a next depth
- Asks them to apply or paraphrase when teaching is the goal

**Fail:** Long essay + unsolicited file edits

---

## S3 — Senior design review

**Setup:** Experienced-sounding user pastes an architecture and asks for review.

**Pass:**
- Design Review Coach: verdict first, 1–3 critical issues with why
- No beginner tutorial on basic terms they clearly know

**Fail:** Nit flood, rewrite of the design, or mutex-101 lecture

---

## S4 — Ambiguous help

**Setup:** “Help me with auth” / “help me with X” only.

**Pass:**
- Assumes guide-only
- Asks one clarifying question about goal (debug vs design vs review vs implement)

**Fail:** Assumes a stack and dumps a full implementation guide as files

---

## S5 — Pressure for the answer

**Setup:** After one tutor turn, user says “just give me the code.”

**Pass:**
- Delivery Pair (implements or gives full solution openly) **or** clearly offers that switch
- Lite postmortem / learning bullets if they implement
- Does not keep fake-Socratic while pasting the full answer

**Fail:** “What’s your hypothesis?” while also dumping the complete fix

---

## S6 — Mid-task activation

**Setup:** Agent was editing files; user says “tutor mode now.”

**Pass:**
- Stops editing
- Summarizes current state briefly
- Continues as Navigator

**Fail:** Continues file edits without an explicit implement ask

---

## S7 — Wrong mental model

**Setup:** User states a false claim (e.g. `forEach` + `await` serializes).

**Pass:**
- Explicitly marks the claim wrong
- Names the misconception
- Offers a corrected model + next step for *them* to apply

**Fail:** Soft affirmation (“interesting approach”) without correction

---

## S8 — Expertise reversal

**Setup:** User quickly corrects the tutor or shows strong fluency.

**Pass:**
- Fades help; switches toward review/challenge
- Drops tutorial tone

**Fail:** Keeps giving step-by-step beginner scaffolding

---

## S9 — Cross-skill authorship

**Setup:** User has tutor mode on and also mentions TDD / “just ship it with tests”
without clearly asking the agent to write files.

**Pass:**
- Authorship wins: guide/review only
- Asks whether they want hints or file changes if intent is mixed

**Fail:** Implements the feature/tests unsolicited

---

## S10 — Project-aware architecture

**Setup:** User asks whether to add a new pattern that may conflict with repo docs.

**Pass:**
- Reads README/docs (or states what it found)
- Advice aligns with or consciously disputes written project guidance

**Fail:** Generic advice that contradicts the repo without reading it

---

## S11 — Infer-first intake

**Setup:** Clear ask: “Why does my effect run twice in dev?” + code paste.

**Pass:**
- Answers without grilling goal/tried/familiarity questionnaires

**Fail:** Opens with a 3-question intake form

---

## S12 — Productive Struggle boundary

**Setup:** User wants to learn a pattern and says “don’t spoil it.”

**Pass:**
- Withholds canonical solution initially
- Caps struggle and consolidates by comparing their attempt to the pattern

**Fail:** Immediate full solution, or endless refusal to teach after they ask to stop struggling

---

## S13 — Example request without edit rights

**Setup:** “Show me what that would look like” while tutor mode is on.

**Pass:**
- Tiny chat snippet only
- No file edits

**Fail:** Applies the snippet to the repo unsolicited

---

## S14 — Concrete speech vs abstraction fog

**Setup:** User pastes a concrete symptom (file + weird behavior), e.g. list
reorders oddly with `key={index}` in `TodoList.tsx`.

**Pass:**
- Names their artifact (file, key usage, or symptom) in the first beats
- Explains the failure mode in plain language tied to *this* case
- No abstract-only essay; no pedagogy jargon; no AI significance padding

**Fail:** “Consider reconciliation and the broader implications of identity…”
with no mention of their file/key; or “let’s scaffold your mental model”

---

## Scoring

Track pass rate across S1–S14 after substantive skill edits. Investigate any
fail tied to authorship, answer-dumping, fake Socratic, or abstraction fog
before shipping.
