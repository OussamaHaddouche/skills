# Feedback and review craft

Use in **Design Review Coach**, postmortems, and any critique turn.
Patterns align with strong code-review teaching practice; details in `library.md`.

---

## Structure a critique turn

1. **Verdict first** — “This is fine” / “Change X” / “Blocked on Y.”
2. **Why** — mechanism or risk, not taste alone.
3. **Better default** — one preferred alternative when it matters.
4. **Scope** — 1–3 critical items; park nits or label them `nit:`.
5. **Hand back** — they propose or apply the fix; you react.

Reinforce what worked (specific behavior), not generic praise.

---

## Comment patterns that teach

| Pattern | Example shape |
| --- | --- |
| Explanatory rationale | “This breaks when Z because …” |
| Standard-backed alternative | “Prefer A here — matches how this repo does B.” |
| Open question first | “What happens to retries if the lock expires?” |
| Point problem, leave fix (default) | “Error path swallows the cause — surface it.” |
| Direct guidance when stuck/novice | “Extract the parse step; here’s a 6-line sketch.” |
| Constraint-aware | “Given your latency budget, caching beats another hop.” |

---

## Anti-patterns in review

| Anti-pattern | Do instead |
| --- | --- |
| Harsh / personal tone | Critique the code path; keep peer tone |
| Nit flood | Cap criticals; batch nits or skip |
| Nonpragmatic (ignore constraints) | Restate constraints; advise inside them |
| Rewrite their PR unsolicited | Coach the change; Delivery Pair only if asked |
| “LGTM” with no read | Say what you actually checked |
| Vague “this is messy” | Name the smell and the risk |
| Only negatives | Name one concrete strength when present |

---

## Severity language

- **Must** — correctness, security, data loss, broken contract
- **Should** — maintainability or clarity that will hurt soon
- **Nit** — style/preference; never block on nits alone in tutor mode

---

## Feed-forward close

End useful reviews with one forward move:

- “Next: pressure-test the failure path.”
- “Reusable heuristic: validate at the boundary, trust inside.”
- Optional short drill if they want practice — not a syllabus.
