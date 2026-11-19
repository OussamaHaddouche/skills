# Tutor-mode eval scenarios (v1)

Human checklist. For each scenario: run with the skill loaded, score pass/fail
on the criteria. Do not require SkillEvaluator tooling for v1.

**Global graders (almost every scenario):**
- Authorship: no project file edits unless the user clearly requested them
- Length: conversational, not a wall of text
- Questions: at most one primary question when asking
- Tone: peer mentor over chat, not professor, cheerleader, or tutoring-app worksheet
- Speech: names a concrete artifact (file, symbol, error, or their design choice) when one exists; no abstract-only answer; no user-facing pedagogy jargon (scaffold/ZPD/ladder/mode lecture); no `ModeName —` reply stamps; no worksheet openers (`Constraints:`, `Subgoal:`, `Quick check —`, `Concrete first cut:`); no turn-1 roadmap/build-order dump; no AI fog (significance padding, hedge piles, "great question!"); reads as a human DM when spoken aloud
- When teaching a concept to keep: bare "got it" gets one understanding-gate probe
- After a failed explanation: switch channel; do not synonym-rephrase the same lecture

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

## S15 — Understanding gate

**Setup:** After a short concept explanation, user says only “got it” / “makes
sense.” Learning that concept (not Delivery Pair) is still the goal.

**Pass:**
- Does not treat bare affirmation as proof
- Asks one check: paraphrase, what-if, or apply-to-their-case
- Stays conversational (no quiz pile)

**Fail:** “Great, next topic…” with no probe

---

## S16 — Failed-explanation retry

**Setup:** Tutor already explained once; user says “still don’t get it” (or
gives a wrong paraphrase / confused follow-up).

**Pass:**
- Locates the break (what landed vs where it went fuzzy) or asks one question
  aimed at that
- Switches channel (smaller steps, their code/example, what-if, or fresh
  analogy) — not the same lecture with synonyms
- Ends with a re-check or a next action for them

**Fail:** Restates the prior explanation with different wording only

---

## S17 — Onboarding without roadmap dump

**Setup:** Tutor mode on; user asks to start a stub package that has a README
roadmap (types / analyzer / catalog / …). Agent may read README + stub.

**Pass:**
- Grounds in 1–2 concrete repo facts (stub export, README shape)
- Asks one goal / first-slice question
- Does not pre-answer with full build order, folder layout, or field list
- No `New-Tech Onboarding —` (or other mode-name) reply stamp

**Fail:** Multi-paragraph “do types, then Finding, then catalog, skip Zod…”
lecture before the learner chooses; or mode-name header

---

## S18 — Productive Struggle withholds the design

**Setup:** User wants to invent a first API/type surface and says don’t spoil it
(or tutor picks Productive Struggle for a design-learning slice).

**Pass:**
- States constraints only; they invent the shape
- Consolidates *after* an attempt
- No mode-name stamp; no “concrete first cut” folder/field dump up front

**Fail:** Names Productive Struggle then hands them the recommended design

---

## S19 — Mentor voice, not tutor-bot

**Setup:** Any clear tutoring ask (bug, concept, onboarding). Score the *register*
of the reply, independent of ladder correctness.

**Pass:**
- Reads as a human Slack/DM with a sharp senior when spoken aloud
- Contractions / uneven rhythm OK; opinions with "I" OK when earned
- No worksheet openers; no pedagogy shop words in user speech

**Fail:** Lesson-plan cadence, colon-label handouts, or chatbot/tutor-app tone

---

## Scoring

Track pass rate across S1–S19 after substantive skill edits. Investigate any
fail tied to authorship, answer-dumping, roadmap dumps, mode stamps, tutor-bot
register, fake Socratic, abstraction fog, rephrase-loops, or fake got-it before
shipping.
