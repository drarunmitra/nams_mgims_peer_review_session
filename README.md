# Value of Peer Review: Human and AI-Assisted (45-minute session)

Quarto Reveal.js deck for **Session 11 – Value of Peer Review: Human and AI-Assisted**.

- Workshop: *Workshop on AI in Health Research* (NAMS, MGIMS Sevagram)
- When: Day 2, 24 November 2026, 16:15–17:00 (45 min)
- Presenter: Dr Rahul Narang, Dean and Professor & Head, Microbiology, AIIMS Bibinagar
- Builds on the 14:00 abstract peer-feedback group work and Session 10 (rejection). Does not repeat rejection reasons.

## Timing plan

| Min | Block |
|---|---|
| 0–4 | Why peer review: models and reviewer duties |
| 4–9 | A structured review: format, checklist, tone |
| 9–20 | Activity: Review this (pairs, synthetic excerpt, answer key) |
| 20–30 | Human vs AI review: side by side, who caught what |
| 30–36 | Rules for AI in peer review (ICMJE) and AI pre-review of your own draft |
| 36–41 | Responding to reviewers: basics, good vs poor, disagreeing |
| 41–45 | AI appraisal checklist, take-home, questions |

## Files

| File | Purpose |
|---|---|
| `index.qmd` / `index.html` | Deck source and self-contained deck (press `S` for speaker view) |
| `Peer_Review_Session11.pdf` | PDF export (no speaker notes; tabs print as separate pages) |
| `excerpt.md` | The synthetic manuscript excerpt |
| `handout.qmd` → `handout.pdf`, `handout.docx` | 2-page handout: excerpt, review template, AI appraisal checklist. No answers |
| `ai_demo/review_prompt_and_output.md` | Exact prompt and raw, unedited AI review |
| `style.css`, `_extensions/` | House style and tabset plugin |

## Render

```bash
quarto render index.qmd
quarto render handout.qmd --to typst   # PDF
quarto render handout.qmd --to docx
```

## What is synthetic

- The manuscript excerpt, the running example (312 urinary *E. coli* isolates), all numbers and the seven planted problems are synthetic.
- **The "human-style" review is not from a human.** The assistant that prepared the deck wrote it after planting the problems, so it catches all seven by design. **Dr Narang: replace it with your own review.** The comparison table is therefore not a measure of human reviewers.
- The good and poor author replies, with their page and line numbers, are written for teaching.
- The AI review is **real and unedited**: one call to a small Claude model (Haiku), no tools, on 23 Nov 2026. It caught 6 of 7 planted problems and missed the sample-size justification. It invented no reference and did not flatter. Other tools and runs will differ.

## Verified and not verified

- Verified (fetched): ICMJE Section V.B "Use of AI by Reviewers" (quote of 12 words on the slide); ICMJE Section V.A (authors); COPE Ethical Guidelines for Peer Reviewers v1 (March 2013), read from a copy of the PDF because publicationethics.org blocked automated access.
- Not verified: the current COPE version (v2, 2017) was not opened; the ICMJE "II.C.2.c" confidentiality section was cited only through the V.B text; the AI's remark that nitrofurantoin and fosfomycin disc breakpoints "differ by disc content" was not checked against CLSI.
