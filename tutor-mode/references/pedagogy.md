# Pedagogy → agent moves

Dense cards. Use to choose *moves*, not to lecture the learner about theory.
Sources and links: `library.md`.

---

## Cognitive apprenticeship

Make invisible expert thinking visible, then hand control back.

| Phase | Agent move |
| --- | --- |
| Model | Narrate one thin slice: cues, decision, prediction |
| Coach | Watch their attempt; one task-specific nudge |
| Scaffold | Reduce degrees of freedom on the blocked subtask only |
| Articulate | “Explain your model of X before we change code” |
| Reflect | Diff their process vs the expert process after a win |
| Explore | Transfer prompt with less help |

---

## ZPD + contingent scaffolding

Help only what they cannot yet do alone. Least support that unblocks.

Wood-style moves: recruit attention → reduce options → keep the goal in view →
mark a critical feature → manage frustration → demonstrate a *slice*.

Exit: they succeed with less help than last turn → **fade**.

---

## Worked / faded examples + expertise reversal

| Learner signal | Guidance |
| --- | --- |
| Novice / new tech | Worked example → completion → faded steps → solo |
| Intermediate | Example–problem pairs; self-explain *why* |
| Expert / flying | Skip tutorials; challenge, review, or problem-first |

If heavy guidance is ignored or they correct you, drop guidance immediately.

---

## Self-explanation

Their construction beats your monologue.

- After a short example: “Why does this line belong? What breaks if removed?”
- On error: expected vs observed before your diagnosis.
- **Understanding gate:** reject bare “got it” / “makes sense.” One probe when
  the concept must stick: paraphrase, what-if, or apply-to-their-case.

---

## Failed-explanation retry

First explanation missed → do **not** synonym-dump the same lecture.

1. Locate the break (what landed vs where it went fuzzy) — one question.
2. Switch channel: smaller steps, different example from *their* artifact,
   what-if / before-after, or one fresh analogy — pick *one* new channel.
3. Re-check with an understanding-gate probe; hand the next action back.

Still stuck after a couple of retries → escalate the help ladder or offer
Delivery Pair. Practitioner consensus (tutor communities): teach-back to find
the break, then a *different* representation.

---

## Dialog moves (AutoTutor-shaped)

Use in order as needed; **one** primary move per turn:

1. **Pump** — “Say more about that.”
2. **Prompt** — ask for the missing piece tied to their code/claim.
3. **Hint** — subgoal, not full answer.
4. **Correct** — name the misconception explicitly when detected.
5. **Summarize** — mirror their correct reasoning; set next micro-goal.

Fake Socratic (vague questions, then dump) is a failure — see `anti-patterns.md`.

---

## Feedback (Hattie & Timperley)

Answer three questions at the right level:

- **Feed-up:** What does good look like for this micro-goal?
- **Feed-back:** How are they going relative to that?
- **Feed-forward:** What strategy next?

Prefer **task** and **process** feedback. Weak: empty praise / ability labels.

---

## Productive failure

Only for concept learning with time. Generation → consolidation comparing their
attempts to canonical. Never skip consolidation. Not for hotfix Delivery Pair.

---

## Notional machines + PRIMM-ish flow

Many stuck states are wrong runtime models, not missing API trivia.

- Predict before edit when teaching a construct.
- Trace state; fix the model, then the code.
- Prefer modify-existing over greenfield while learning.
- Watch classics: assignment/copy, loop bounds, async timing, reference vs value,
  effect/lifecycle timing.

---

## Pair roles

| Role | Use |
| --- | --- |
| Navigator (default) | Questions, hypotheses, “what would you type next?” |
| Driver-model | Short demo of one decision / tiny snippet, then hand back |
| Duck | They explain while you stay quiet of hints for a beat |

Label the role when switching so ownership of the next action is obvious.

---

## SE mentor moves (craft, not career)

From staff/mentor practice: advice (labeled experience), teaching (close a
knowledge gap with an artifact), coaching (questions), guardrails (review risks).

Short practice tips OK. Career paths, promo strategy, and therapy: out of scope.
