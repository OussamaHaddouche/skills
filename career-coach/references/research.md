# Career coach — research report

Research freeze for the `career-coach` skill. Sources inspected; principles adopted;
limitations noted. This file is for humans and maintainers. Agents use
`library.md` at runtime.

## Purpose of the skill

Help professionals present their value clearly to recruiters and hiring managers:
discover real achievements, audit CV / LinkedIn / portfolio / interview assets,
improve discoverability without ATS myths, and align materials to target roles—
without inventing facts or hardcoding a profession, market, or seniority.

## Sources inspected

### Achievement writing

| Source | Status | Core teaching |
|--------|--------|---------------|
| [Yale — Impactful resume bullets](https://ocs.yale.edu/resources/writing-impactful-resume-bullets/) | Live | Action + Project + Result; X measured by Y by doing Z; responsibility→impact prompts |
| [MIT CAPD — Writing about skills](https://capd.mit.edu/resources/resumes-writing-about-your-skills/) | Live | PAR; quantify via money, %, quantity/scale |
| [UC Davis — Accomplishment statements](https://careercenter.ucdavis.edu/resumes-and-materials/resumes/accomplishment-statements) | Live | Action + Context = Results; extraction questions |
| [Princeton — ACE statements](https://careerdevelopment.princeton.edu/resume-guide/action-oriented-accomplishment-statements) | Live | Action, Context, End result; strong verbs |
| [Europass CV](https://europass.europa.eu/en/create-europass-cv?lang=en) | Live | Reverse chrono, tailor, readability; EU mobility |

### Progression and impact

| Source | Status | Core teaching |
|--------|--------|---------------|
| [Dropbox career framework](https://dropbox.github.io/dbx-career-framework/) | Live | Impact compass; archetypes; Results/Direction/Talent/Culture |
| [Dropbox — What is impact?](https://dropbox.github.io/dbx-career-framework/what_is_impact.html) | Live | Consistency, Velocity, Accountability; impact levers |
| [Monzo progression (GitHub)](https://github.com/monzo/progression-framework) | Partial | Mastery/Impact/Influence/Comms/Leadership; compass not GPS |
| [Monzo eng framework PDF v3](https://monzo.com/documents/engineering-progression-framework-v3-0.pdf) | Live | Scope ladder; anti-checklist; multi-path senior shapes |
| [GitLab eng career matrix](https://handbook.gitlab.com/handbook/engineering/careers/matrix/) | Live | Cumulative levels; scope of decision rights |

### Selection and interviews

| Source | Status | Core teaching |
|--------|--------|---------------|
| [CIPD — Selection methods](https://www.cipd.org/en/knowledge/factsheets/selection-factsheet/) | Live | Structured selection; job-related criteria; fairness |
| [OPM — Structured interviews](https://www.opm.gov/policy-data-oversight/assessment-and-selection/structured-interviews/) | Live | Job analysis; behavioral/situational; rating anchors |
| [Yale — Behavioral interview](https://ocs.yale.edu/channels/the-behavioral-interview/) | Live (channel URL; old path 404) | STAR |

### ATS and discoverability

| Source | Status | Core teaching |
|--------|--------|---------------|
| [Greenhouse — Unsuccessful resume parse](https://support.greenhouse.io/hc/en-us/articles/200989175-Unsuccessful-resume-parse) | Live | Size, graphics, columns, tables, headers/footers, text boxes, image uploads |
| [Lever — Resume parsing](https://help.lever.co/hc/en-us/articles/20087345054749-Understanding-resume-parsing) | Live (URL moved) | Selectable text; supported file types; no image files |
| [LinkedIn — Good profile](https://www.linkedin.com/help/linkedin/answer/a554351) | Live | Completeness: headline, About, experience, skills |
| [LinkedIn Recruiter — Boolean](https://www.linkedin.com/help/recruiter/answer/a524335) | Live | AND/OR/NOT, phrases, grouping |
| [LinkedIn Recruiter — AI Search](https://www.linkedin.com/help/recruiter/answer/a1659757) | Live | NL→filters; prose evidence of soft competencies |

### Portfolios

| Source | Status | Core teaching |
|--------|--------|---------------|
| [Intuit — SWE portfolio](https://www.intuit.com/blog/global-stories/software-engineer-portfolio/) | Live | 3–5 projects; problem→result; living doc |
| [NYU Tandon — Building a portfolio](https://engineering.nyu.edu/life-tandon/experiential-learning-center/building-portfolio) | Live | Recruiter skim vs HM craft; quality>quantity; case studies; land the interview |

### Regional (supplementary)

- France: [service-public.fr CV](https://www.service-public.gouv.fr/particuliers/vosdroits/F33336); CNIL job-relevant data only
- UK/US: university careers guidance (CV vs resume naming, length, no photo/age)
- Morocco / North Africa: thinner official documentation—treat as common-practice notes with certainty labels

## Community signal (non-primary)

r/careeradvice threads (2024–2026) used only as **hiring folklore / failure modes**,
not as citations that override Yale/MIT/Greenhouse/etc.:

- Debrief rooms often avoid risk; “safe pair of hands” beats highlight reel; overqualified ≈ flight risk
- CV↔LinkedIn mismatches + interview panic destroy trust
- Gaps/short stints: clean page, brief honest oral explanation; no date fiction
- Credential/title ambiguity fails verification
- AI-generic resume language is actively disliked
- Cold response can mean wrong market packaging (same evidence, different buyer)

Logged for maintainers; agents should prefer `library.md` primary sources at runtime.

## Adopted principles

1. **Evidence over claims.** Accomplishment statements (PAR/ACE) and STAR stories beat duty lists.
2. **Discovery before rewrite.** Many people cannot name their impact; ask before inventing polish.
3. **Six-dimension Achievement Discovery Model (ADM)** — proposed methodology: Problem, Contribution, Judgment, Scope, Outcome, Evidence. Maps to PAR/ACE for CVs and STAR for interviews.
4. **Evidence hierarchy.** Measured quantitative → measured scope → documented qualitative → verified delivery → contribution without outcome → intended → unsupported (remove/qualify).
5. **Two evaluation lenses + risk.** Recruiter/HR ≠ hiring manager; both matter. Also: reduce unanswered risk so saying yes is easy.
6. **Portable seniority axes.** Scope, Influence, Autonomy, Complexity, Outcomes—not company level labels as certification.
7. **Asset system.** One achievement inventory → adapted for CV, LinkedIn, portfolio, interview.
8. **Market-local conventions.** Never assume one country’s CV rules apply everywhere.
9. **No ATS score theater.** Optimize parseability and honest keyword coverage; refuse universal scores.
10. **Speech + anti–AI-slop assets.** Coach like a sharp peer; strip AI tells; drafts stay specific and human; never invent facts to sound human.
11. **Verification-safe identity.** Exact education status; official titles; timeline honesty across assets.

## Disagreements and tensions

| Tension | Resolution in skill |
|---------|---------------------|
| “Quantify everything” vs no metrics available | Prefer quantification when real; accept scope/qualitative; never invent |
| Europass familiarity vs private-employer local CVs | Offer Europass when EU programs ask; else market-local format |
| LinkedIn completeness meter vs Recruiter search | Optimize real fields/synonyms; do not promise ranking from strength meter |
| Greenhouse layout risks vs Lever sparse official layout docs | Cite Greenhouse for layout; Lever for file types/selectable text; label certainty |
| Engineering frameworks vs non-eng users | Extract portable axes; domain packs are swappable |
| Photo common in some Maghreb practice vs FR/UK/US anti-bias norms | Ask target market; do not universalize |
| “Be impressive” vs risk-averse debriefs | Prefer clear fit + evidence; don’t peacock into flight-risk reads |
| Community Reddit tips vs primary sources | Use Reddit as failure-mode signal only; keep library.md authoritative |

## Limitations

- Maghreb guidance is weaker authority than FR/UK/US government/university sources.
- Lever does not officially document column/table failure modes in the same detail as Greenhouse.
- Company career frameworks are not universal promotion systems.
- Selection research is employer-facing; candidate branding is inferred application.
- LinkedIn ranking algorithms are not publicly documented—do not invent them.
- The ADM is a design hypothesis grounded in PAR/STAR/impact frameworks, not an academic standard.
- Reddit/community threads are anecdotal and selection-biased; never cite them as proof of employer policy.

## Design implications

- One skill (`career-coach`), mode router, progressive references—not one file per buzzword.
- Hard integrity + Speech rules in `SKILL.md`.
- Human eval suite (scenarios A–M) tests questions, reasoning, risk framing, timeline honesty, and speech—not only pretty bullets.
- Synthetic fixtures only; no personal history of the skill author.
