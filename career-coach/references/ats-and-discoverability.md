# ATS and discoverability

Load for ATS mode or when formatting/searchability is the ask.

## Separate five concerns

Do not collapse these into one “ATS score.”

1. **Document parsing** — can software extract name, contact, jobs, education?
2. **Keyword / recruiter search** — can humans find the profile with Boolean/filters?
3. **JD relevance** — does language overlap real experience?
4. **Human evaluation** — does a person understand impact?
5. **AI-assisted search** — systems that match prose competencies (e.g. LinkedIn
   Recruiter AI Search)—still not a candidate-facing score.

## Parsing hygiene

### Greenhouse-documented risks

Source: Greenhouse “Unsuccessful resume parse.” Prefer citing this for layout.

Common failure modes:

- File too large (Greenhouse documents a size limit)
- Graphics, photos, word art
- Uploaded as an image rather than real text PDF/DOCX
- Tables, headers/footers, text boxes
- Columned layouts
- Unclear/inconsistent sections
- Contact info only in header/footer
- Letters spaced apart (looks fine to eyes, breaks parsers)
- Placeholder/fake data patterns that parsers skip

### Lever (certainty: official vs practice)

**Documented:** supported file types (Word, PDF, RTF, HTML, ODF, etc.); cannot
parse image files; selectable-text test; extracts profile fields such as name,
organization, contact.

**Not well documented officially:** exact column/table behavior. Treat
single-column, body contact, standard headings as **general parseable-layout
practice** (reinforced by Greenhouse), not as Lever-guaranteed rules.

### Practical defaults

- Single column, real text, standard section names
- Contact in document body
- Consistent dates; complete titles where possible
- PDF or DOCX with selectable text
- Skills and titles that are true

## Keyword and LinkedIn discoverability

From LinkedIn Help / Recruiter docs:

- Profile fields matter: headline, About, experience, skills, location
- Boolean: `AND` / `OR` / `NOT`, `"phrases"`, `(groups)`—put real synonym
  coverage in titles/skills/prose
- AI Search can match traits described in prose, not only skill chips

**Do:** honest title variants and tools you actually used.
**Don’t:** stuffing, white text, fake skills, “All-Star = ranked #1” claims.

## Myths to refuse

| Myth | Reality |
|------|---------|
| Universal ATS % pass mark | Employer systems don’t share one public score |
| Keyword density wins | Context + truth beat repetition |
| Fancy PDF always rejected | Overstated; prefer parseable layout; humans still decide |
| Completeness meter = hire | Usability ≠ ranking algorithm |

## Output shape

```text
Parsing risks (with certainty tags)
Search / synonym gaps (true terms only)
Human skim issues
Recommended format changes
What we will not claim
```
