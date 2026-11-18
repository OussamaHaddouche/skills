# Reference library

Annotated for agent behavior. Claim → implication → source. Not a syllabus dump.

---

## Learning science

**Cognitive apprenticeship (Collins, Brown, Holum)** — Expert thinking is mostly
invisible; teaching must model, coach, scaffold/fade, then articulate/reflect/explore.
→ Use mode phases and narrated thin slices; fade after success.
→ https://www.aft.org/ae/winter1991/collins_brown_holum

**Scaffolding (Wood, Bruner, Ross)** — Contingent support: reduce freedom, mark
critical features, control frustration, then withdraw.
→ Help ladder rungs; least support that unblocks.
→ Classic 1976 paper; summarized in scaffolding histories and CA materials.

**ZPD (Vygotsky)** — Teach in the gap between solo and assisted performance.
→ Infer familiarity; avoid busywork below and answer-dumps above.

**Worked examples + fading (Sweller; Gray et al. in programming)** — Novices learn
schemas from worked/faded examples; pure problem-solving overloads early.
→ Concept Studio sequence; tiny snippets as worked slices.
→ https://dl.acm.org/doi/10.1145/1288580.1288594

**Expertise reversal (Kalyuga)** — Heavy guidance that helps novices can hurt experts.
→ Seniors get review/challenge, not tutorials.

**Self-explanation (Chi et al.)** — Learners who explain steps to principles outperform
skimmers; tutoring works partly by eliciting explanations.
→ Articulate / paraphrase checks beat monologues.

**Productive failure (Kapur)** — Generation before instruction can improve transfer
when followed by consolidation.
→ Productive Struggle mode only; always consolidate.
→ https://onlinelibrary.wiley.com/doi/full/10.1111/cogs.12107

**Feedback model (Hattie & Timperley)** — Effective feedback: where going, how going,
where next — at task/process/self-regulation levels.
→ Verdict + why + next strategy; skip empty praise.
→ https://assess.ucr.edu/sites/default/files/2019-02/hattietimperley_2007.pdf

**AutoTutor dialog moves (Graesser et al.)** — Pumps, prompts, hints, corrections,
summaries outperform vague questioning.
→ One grounded dialog move per turn.

---

## Computing education

**Notional machines (du Boulay; Sorva)** — Novices need an accurate runtime mental model.
→ Predict/trace before rewrite when constructs are new.
→ https://dl.acm.org/doi/10.1145/2483710.2483713

**PRIMM (Sentance et al.)** — Predict → Run → Investigate → Modify → Make.
→ Read/predict/modify before greenfield Make in Concept Studio / onboarding.

**Socratic code tutors** — Leveled feedback and misconception detection improve
comprehension more than open chat dumps.
→ Escalating ladder; explicit correction.
→ https://pmc.ncbi.nlm.nih.gov/articles/PMC7334736/

**Worked examples in programming (TOCE review)** — Evidence base for example-based
instruction in CS.
→ https://dl.acm.org/doi/full/10.1145/3560266

**Debugging interventions (TOCE SLR)** — Teach systematic strategies, not only fixes.
→ Name bisect/minimize/oracle moves in Stuck Debugger.
→ https://dl.acm.org/doi/10.1145/3690652

---

## Software engineering practice

**Apprenticeship Patterns (Hoover & Oshineye)** — Craft learning: find mentors, be the
worst, breakable toys, dig deeper, share what you learn.
→ Short craft tips and practice suggestions; learner keeps agency.
→ https://www.oreilly.com/library/view/apprenticeship-patterns/9780596806842/

**The Staff Engineer’s Path, influence chapter (Reilly)** — Advice vs teaching vs
coaching vs guardrails vs opportunity.
→ Label advice as experience; default coach; review as guardrail.

**Google eng-practices — review comments** — Kindness, explain why, balance pointing
out problems vs prescribing fixes; reinforce what is good.
→ https://google.github.io/eng-practices/review/reviewer/comments.html

**Effective teaching through code reviews (ACM)** — Explanatory rationale and
constructive tone teach; harsh/nitty/nonpragmatic reviews do not.
→ `feedback.md` patterns.
→ https://dl.acm.org/doi/10.1145/3660764

**Microsoft code-review guidance** — Prefer questions; prefix nits; focus on
correctness and design over ego.
→ https://microsoft.github.io/code-with-engineering-playbook/code-reviews/process-guidance/reviewer-guidance/

---

## AI tutoring policy

**Pedagogical harm / multi-turn collapse** — LLM tutors often degrade into answer
supply across turns, especially under student pressure.
→ Early-turn stinginess; honest Delivery Pair escape.

**Answer leakage under pressure** — Solution leakage concentrates early when users push.
→ Do not drip full fixes while claiming Navigator mode.

**Scaffolded error correction > lecture** — Guided retry after naming the error beats
ever-more-personalized explanations alone.
→ Correct explicitly, then next attempt on the ladder.
