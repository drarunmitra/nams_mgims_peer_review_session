# AI review tally (9 runs)

Runs: `ai_demo/review_prompt_and_output.md` (Haiku, first run), `review_haiku_1..5.md`, `review_opus_1..3.md`. Same prompt and excerpt (`../excerpt.md`), fresh call each, no tools, 2026-11-23. Each file holds the raw, unedited output.

Method: keyword search of each file for the planted problem, then read to confirm. A "catch" means the review names the problem and asks for a fix. One passing remark counts, but is labelled.

| Problem | Planted? | Runs that caught it |
|---|---|---|
| Causal conclusion from cross-sectional design | yes | 9 of 9 |
| Policy recommendation not supported | yes | 9 of 9 |
| Unit of analysis / repeat isolates | yes | 9 of 9 |
| CLSI/EUCAST version not stated | yes | 9 of 9 (all name "edition") |
| No ethics statement | yes | 9 of 9 |
| P values without CIs | yes | 9 of 9 |
| No sample-size justification | yes | **1 of 9**: haiku_1, a minor comment ("report the reason for the sample size of 312"). opus_3 called the sample size "reasonable for the question" |
| Variable selection by univariable P < 0.2 | no | 9 of 9 |
| Ceftriaxone 53.8% vs ESBL 50.6% gap | no | 6 of 9 (first run, haiku_1, haiku_3, haiku_4, haiku_5, opus_3) |
| AmpC | no | 5 of 9 (first run, haiku_1, opus_1, opus_2, opus_3) |
| Percentages "agree with" n = 312 | no | 5 of 9 said so (haiku_1, haiku_4, haiku_5, opus_1, opus_2). The excerpt gives no per-drug denominators |

Recommendation: all nine said major revision.

## Things the AI got wrong or made up
- **Invented problem (1 of 9):** haiku_2, minor comment 12: "the text mixes 'hospitalisation' (British) with 'hospitalization' conventions". The excerpt contains only "hospitalisation" (checked: 0 occurrences of "hospitalization").
- **Assumed detail (1 of 9):** opus_3 says the model was "adjusted for only age, sex and hospitalisation". The excerpt does not say what entered the model.
- **Excerpt-blind requests:** several runs ask for items a 300-word excerpt would not hold (flow diagram, patient characteristics table, ethics approval number, a limitations section, a data dictionary in the first run). haiku_3 says "I reviewed only the excerpt provided".
- **Not checked:** the first run's line that nitrofurantoin and fosfomycin "disc breakpoints differ by disc content" was not checked against CLSI.
- **References:** the reviews contain no reference lists, so no reference could be fabricated. They name real standards (STROBE item 13, CLSI M39 and M100, ICMR AMRSN); I did not verify every technical statement (for example mCIM/eCIM, ATCC 700603).

## Limits
Nine runs of two small-to-large Claude models on one excerpt. Keyword counts can miss paraphrases, and I read for confirmation, not blind. Other tools, prompts or days will differ.
