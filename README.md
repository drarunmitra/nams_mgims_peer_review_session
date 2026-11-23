# Value of Peer Review: Human and AI-Assisted (45-minute session)

Quarto Reveal.js deck for **Session 11 – Value of Peer Review: Human and AI-Assisted**.

- Workshop: *Workshop on AI in Health Research* (NAMS, MGIMS Sevagram)
- When: Day 2, 24 November 2026, 16:15–17:00 (45 min)
- Presenter: Dr Rahul Narang, Dean and Professor & Head, Microbiology, AIIMS Bibinagar
- Builds on the 14:00 abstract peer-feedback group work and Session 10 (rejection). Does not repeat rejection reasons.

## Timing plan

| Min | Block |
|---|---|
| 0–4 | Why peer review: more than a gate, models, reviewer duties |
| 4–9 | A structured review: format, checklist, tone |
| 9–20 | Activity: Review this (pairs, synthetic excerpt, answer key) |
| 20–30 | Human vs AI review: side by side, who caught what (nine AI runs) |
| 30–36 | Rules for AI in peer review (ICMJE, journal policies, in practice) and AI pre-review of your own draft |
| 36–41 | Responding to reviewers: basics, good vs poor, disagreeing |
| 41–45 | AI appraisal checklist, take-home, questions |

## Files

| File | Purpose |
|---|---|
| `index.qmd` / `index.html` | Deck source and self-contained deck (31 slides; press `S` for speaker view) |
| `Peer_Review_Session11.pdf` | PDF export (no speaker notes; tabs print as separate pages) |
| `facilitator_guide.html`, `Facilitator_Guide_Session11.pdf` | Facilitator guide: prep checklist, minute-by-minute run of show, answer key, nine-run AI results, what to cut, likely questions, neighbouring sessions, what is verified |
| `excerpt.md` | The synthetic manuscript excerpt |
| `handout.qmd` → `handout.pdf`, `handout.docx` | 2-page handout: excerpt, review template, AI appraisal checklist. No answers |
| `ai_demo/` | Exact prompt and the nine raw, unedited AI reviews (`review_prompt_and_output.md`, `review_haiku_1..5.md`, `review_opus_1..3.md`) |
| `docs/` | Literature review (`lit_A_peer_review_basics.md`, `lit_B_ai_in_review.md`, `lit_C_response_and_appraisal.md`) and `ai_review_tally.md` |
| `style.css`, `_extensions/` | House style and tabset plugin |

## Render

```bash
quarto render index.qmd
quarto render handout.qmd --to typst   # PDF
quarto render handout.qmd --to docx
```

## Revision (23 Nov 2026): literature review

- Every real claim on a slide was fetched and read, unless listed below. Sources and status: `docs/`.
- Added: reviewers-miss-errors evidence (Schroter 2008), peer-review model definitions (Ross-Hellauer 2017), ICMJE peer-reviewer text, STROBE item mapping for the planted problems, a "Journals differ" slide (ICMJE, Elsevier, Springer Nature, Wiley, NIH), tone evidence (Gerwing 2020), sources for the point-by-point response (Noble 2017, PLOS and Frontiers guides), and a note that no validated tool exists for judging AI feedback on manuscripts.
- The AI review demo now uses nine runs, not one. The slide table reports counts across all nine.
- Layout: all 31 slides and both tabsets were checked at 1280x720 for overflow. The side-by-side tab slide now uses two columns. The acknowledgement slide was removed.

## What is synthetic

- The manuscript excerpt, the running example (312 urinary *E. coli* isolates) and the seven planted problems are synthetic.
- **The "human-style" review is not from a human.** The assistant that prepared the deck wrote it after planting the problems, so it catches all seven by design. **Dr Narang: replace it with your own review.** The comparison table is not a measure of human reviewers.
- The good and poor author replies, with their page and line numbers, and Reviewer 2's request are written for teaching.
- The AI reviews are **real and unedited**: nine fresh calls (6 Haiku, 3 Opus) on 23 Nov 2026, no tools, same prompt and excerpt. All nine recommended major revision. Six of the seven planted problems were caught in all nine; the sample-size justification in 1 of 9 (a passing remark; one run called the sample size "reasonable"). One run invented a problem (a "hospitalisation/hospitalization" spelling mix that is not in the text). Counts: `docs/ai_review_tally.md`. Other tools, prompts and days will differ.

## Verified and not verified

- Verified (fetched, read): ICMJE II.C and Section V (authors and reviewers); STROBE cross-sectional checklist items 10, 12, 13, 16; Ross-Hellauer 2017; Hopewell 2014; Kelly 2014; Gerwing 2020; Noble 2017; Frontiers and PLOS author guides; Elsevier, Springer Nature and Wiley reviewer AI policies (accessed 23 Nov 2026); NIH NOT-OD-23-149 (via an archived copy); CLSI M100 and EUCAST version pages.
- Abstract only: Schroter 2008, Jefferson 2007 (Cochrane), Goodman 1994, Liang 2024 (*NEJM AI*), Williams 2004, Sharma 2023.
- **Not verified:** COPE *Ethical Guidelines for Peer Reviewers* v2 (2017); only v1 (March 2013) was read, so no v2 wording is on a slide. No authoritative definition of "post-publication review" was found. JAMA, BMJ and Sage reviewer-AI policies were not opened. No tool validated for judging AI feedback on a manuscript exists (the six-question checklist is a teaching tool). No study counting fabricated references inside AI reviews was found. The first AI run's remark about nitrofurantoin and fosfomycin disc breakpoints was not checked against CLSI.
