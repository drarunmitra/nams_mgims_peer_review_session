# AI demo: AI peer review of the synthetic excerpt (raw, unedited)

- Run on: 2026-11-23, one fresh model call (Claude Haiku, via a subagent). No tools, no web, no context.
- The excerpt is in `../excerpt.md` (synthetic, illustrative). It was pasted after the prompt line.
- Model output below is exactly as returned. Nothing was edited.

## Exact prompt

```
You are a peer reviewer. Review this manuscript excerpt.

<excerpt.md pasted here>
```

## Raw output

**Peer review: "Antimicrobial resistance in urinary *Escherichia coli* at a tertiary hospital in Telangana: a cross-sectional study"**

**Recommendation: Major revision.** The data may be useful as a local antibiogram, but the causal conclusion and the prescribing recommendations go beyond what a single-centre cross-sectional study can support. The methods also need substantial reporting detail before the results can be judged.

**Major comments**

1. **Causal language is not supported by the design.** The conclusion states that "prior antibiotic use causes ESBL production." A cross-sectional study with a logistic model can show association only. Replace with "was associated with" throughout, including the abstract and discussion, and discuss residual confounding.

2. **The prescribing recommendations overreach.** "Stop using ceftriaxone for UTI" and "nitrofurantoin should become the first-line drug for all UTIs in Telangana" do not follow from one hospital's isolates. Nitrofurantoin is appropriate for uncomplicated cystitis, not for pyelonephritis, male UTI, urosepsis or catheter-associated infection, and the sample does not show which infection types the isolates came from. Prescribing guidance also needs the local clinical context, the referral population and the antibiogram by specimen type. Recast this as a hypothesis for stewardship review, and limit any generalisation to the study hospital.

3. **The denominator and sampling frame are missing (STROBE items 13 and 14).** Report how many urine cultures were received, how many showed significant growth, how many were E. coli, and how many were excluded and why (STROBE flow diagram). Define "significant growth" (CFU/mL threshold, and whether it differs for catheter specimens). State whether repeat isolates from the same patient during the year were included. If so, the observations are not independent; keep the first isolate per patient or account for clustering.

4. **Patient characteristics are absent.** No table describes the population: age, sex, inpatient or outpatient status, ward, catheter use, diabetes, prior UTI, renal disease, pregnancy, or prior ESBL carriage. Without this, readers cannot judge whether the isolates are representative or whether the ESBL and antibiotic-exposure findings are confounded.

5. **Confounder collection is too thin.** Only age, sex, prior antibiotic use and hospitalisation were collected, all from request forms. Catheterisation, instrumentation, diabetes, urological abnormality and healthcare contact are well-established ESBL risk factors and are not considered. Acknowledge this as a major limitation, or collect them.

6. **Exposure definitions and measurement are unclear.** Define "prior antibiotic use" (any antibiotic or specific classes; prescribed or actually taken; source of information) and "hospitalisation" (current admission, or within a stated look-back period). Request-form data are likely incomplete. Describe how missing exposure data were handled.

7. **The statistical approach is not appropriate as described.**
   - Selecting variables with univariable P < 0.2 is a data-driven method that inflates type I error and biases coefficients. Pre-specify the model based on a causal framework (a DAG is ideal) or include all pre-specified covariates.
   - Only two adjusted odds ratios are reported. Give the full model: all covariates, including age and sex, with 95% confidence intervals.
   - The hospitalisation result (aOR 1.7, P = 0.048) is borderline, and the interval is not given. Interpret it cautiously.
   - Report the number of events per variable, checks for collinearity, and model fit (for example, calibration or the Hosmer-Lemeshow test).
   - Report 95% confidence intervals for all prevalence estimates. For ESBL at 158/312 (50.6%), the interval is roughly 45% to 56%.

8. **Antimicrobial susceptibility testing needs full methods.**
   - Name the CLSI document and edition used, and state which breakpoints apply to each agent. Disc breakpoints for nitrofurantoin and fosfomycin differ by disc content and by infection type (uncomplicated UTI). Specify this.
   - Give the QC strain (for example, ATCC 25922), inoculum standard and medium.
   - Report the number tested for each agent. Agents not tested for every isolate must have their denominators stated.

9. **ESBL confirmation is incomplete.** The combined disc test is a phenotypic screen, and its result depends on the disc set and on the zone-difference criterion. State the criterion (for example, a 5 mm increase in zone with clavulanate). Also state whether AmpC-producing isolates were distinguished, because the combined disc test does not do this reliably.

10. **Internal consistency of the resistance data needs checking.** ESBL is present in 50.6% of isolates, but ceftriaxone resistance is 53.8%. Most ESBL producers are ceftriaxone-resistant, so about 3% of isolates are ceftriaxone-resistant without ESBL. This may reflect AmpC or other mechanisms, or a labelling error. Address it explicitly. A cross-tabulation of ESBL status against ceftriaxone, cefotaxime and ceftazidime results would help.

11. **Ethics and data governance are not described.** The excerpt does not give the ethics committee approval number, the consent waiver (if any), or how request-form data were de-identified and stored.

**Minor comments**

12. **Background:** "resistance in *E. coli* is rising" needs a citation, and ideally local or national trend data. State the gap this study addresses and the explicit study aims.

13. **Laboratory identification:** "standard methods" should name the approach (biochemical tests, MALDI-TOF, or a VITEK-type system).

14. **Reporting guideline:** Follow STROBE and state this in the methods. Consider the reporting checklist for antimicrobial resistance surveillance studies where applicable.

15. **Discussion:** Compare the findings with national or regional data (for example, ICMR antibiogram reports or published Indian UTI resistance studies), and discuss the limitations of a single centre and of request-form data.

16. **Abstract:** Give confidence intervals alongside the odds ratios and the ESBL prevalence. Remove "causes" and the prescribing recommendations from the conclusions.

17. **Data availability:** Provide a data dictionary and, where permitted, the de-identified isolate-level dataset.

**Priority order for revision:** (1) remove causal and prescribing overreach; (2) add the flow of samples, the patient characteristics table and the full model with confidence intervals; (3) make the ESBL and susceptibility methods reproducible; (4) address the independence of repeat isolates; (5) fix the minor points.
