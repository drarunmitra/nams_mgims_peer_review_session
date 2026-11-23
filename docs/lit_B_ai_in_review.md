# Lit B: AI in peer review - source verification

Checked 2026-11-23. "Opened" = I retrieved the text myself this session. Quotes are verbatim unless marked.

## Summary table

| # | Source | URL / ID | Opened? | Key finding (as stated) | Verdict |
|---|---|---|---|---|---|
| 1 | ICMJE Recommendations, Section V.B "Use of AI by Reviewers" | https://www.icmje.org/recommendations/browse/artificial-intelligence/ai-use-by-reviewers.html | Full page text (curl) | See item 1. Recommendations page footer: "Updated January 2026" | verified |
| 2 | NIH NOT-OD-23-149, released June 23, 2023 | https://grants.nih.gov/grants/guide/notice-files/NOT-OD-23-149.html | Live site blocked (403, Cloudflare). Full text via Wayback snapshot 2026-11-09 | NIH prohibits reviewers using generative AI to analyse or write critiques of grant applications | verified (via Wayback) |
| 3 | Liang W et al. NEJM AI 2024;1(8):AIoa2400196 (arXiv 2310.01783) | doi:10.1056/AIoa2400196; PMID 42932702; https://arxiv.org/abs/2310.01783 | arXiv abstract plus Europe PMC copy of the NEJM AI abstract. NEJM site blocked (403). Full text not read | GPT-4 vs human overlap 30.85% (Nature) / 39.23% (ICLR); two humans 28.58% / 35.25%; 57.4% found feedback helpful/very helpful; 82.4% more beneficial than at least some human reviewers | abstract only |
| 4 | Hosseini M, Horbach SPJM. Res Integr Peer Rev 2023;8:4 | doi:10.1186/s41073-023-00133-5; https://pmc.ncbi.nlm.nih.gov/articles/PMC10191680/ | PMC page via fetch tool (it returned a summary with short quotes) plus Crossref metadata | Disclose LLM use, accept full responsibility, verify accuracy, protect confidentiality, watch for bias | verified (recheck quotes against the PMC page before quoting) |
| 5 | Sharma M et al. arXiv:2310.13548 | https://arxiv.org/abs/2310.13548 | arXiv abstract (v4) | Sycophancy is general across five AI assistants, partly driven by human preference judgments | abstract only (ICLR 2024 venue not confirmed by me) |
| 6a | Elsevier generative AI policy, "For Reviewers". Page says "Policy updated: July 2026" | https://www.elsevier.com/about/policies-and-standards/the-use-of-generative-ai-and-ai-assisted-technologies-in-writing-for-elsevier | Full page text (curl) | Reviewers: no upload, no AI assistance in the review | verified |
| 6b | Springer Nature AI policy | https://www.nature.com/nature/editorial-policies/ai | Full page text (curl) | Risk-based: no upload to unsecured/public AI; disclose; reviewer accountable | verified |
| 6c | Wiley Peer Review Policy | https://authorservices.wiley.com/Reviewers/journal-reviewers/tools-and-resources/review-confidentiality-policy.html | Full page text (curl) | No uploading manuscript parts to GenAI; declare AI used to improve a report | verified |
| 7 | COPE "Authorship and AI tools", 13 Feb 2023 | https://publicationethics.org/guidance/cope-position/authorship-and-ai-tools | Live site blocked (403). Opened via Wayback | Covers authorship and author disclosure only. No peer-review rule | verified (does not cover reviewers) |
| 8 | Du J et al. "LLMs Assist NLP Researchers: Critique Paper (Meta-)Reviewing", EMNLP 2024 (arXiv 2406.16253) | https://arxiv.org/abs/2406.16253 | arXiv abstract plus full PDF text searched | LLM reviews more prone to contradictory and unstated claims | verified (NLP papers, not medicine) |

## Notes per item

### 1. ICMJE Section V.B (reviewers)
Page heading "B. Use of AI by Reviewers", under "V. Use of Artificial Intelligence in Publishing". The page itself has no date. The ICMJE Recommendations page shows "Updated January 2026". Full section text, verbatim:

> "Reviewers must adhere to the journal's stated policy on the use of AI or request permission from the journal prior to using AI technology to facilitate their review. As described in Section II.C.2.c, reviewers must maintain the confidentiality of the manuscript, which may prohibit the uploading of the manuscript to software or other AI technologies where confidentiality cannot be assured unless such use of AI is explicitly permitted by journals. Reviewers who use AI in their review should disclose its use to the journal and ensure the content is appropriate and valid as AI can generate output that can be incorrect, incomplete, or biased."

Mapping: policy/permission = sentence 1; confidentiality/uploading = sentence 2; disclosure and checking output = sentence 3. The source says "adhere to the journal's stated policy ... or request permission", not "and".

V.A (authors), opened: "Authors should carefully review and edit the AI-generated content as the output can be incorrect, incomplete, or biased." Also: "Chatbots (such as ChatGPT) and other AI-assisted tools should not be listed as authors". URL: .../ai-use-by-authors.html.

### 2. NIH NOT-OD-23-149
Title: "The Use of Generative Artificial Intelligence Technologies is Prohibited for the NIH Peer Review Process". Release date: June 23, 2023. Scope: NIH grant applications and R&D contract proposals (study-section review), NOT journal peer review. Verbatim:

> "NIH prohibits NIH scientific peer reviewers from using natural language processors, large language models, or other generative Artificial Intelligence (AI) technologies for analyzing and formulating peer review critiques for grant applications and R&D contract proposals."

> "AI tools have no guarantee of where data are being sent, saved, viewed, or used in the future"

> "uploading or sharing content or original concepts from an NIH grant application, contract proposal, or critique to online generative AI tools violates the NIH peer review confidentiality and integrity requirements."

Accessibility technologies may get an exception after telling the Designated Federal Officer. The live NIH site gave me a Cloudflare challenge, so the text is from archive.org (snapshot 2026-11-09).

### 3. Liang et al.
Europe PMC copy of the NEJM AI abstract and arXiv v1 abstract agree.
- Sample: 3,096 papers in 15 Nature family journals; 1,709 ICLR papers. The NEJM AI version adds 425 health sciences papers (Nature portfolio) and 666 eLife submissions ("similar patterns").
- Overlap of points, GPT-4 vs human reviewers: 30.85% (Nature), 39.23% (ICLR). Between two human reviewers: 28.58% (Nature), 35.25% (ICLR).
- arXiv v1 adds: overlap was larger for weaker papers.
- User study: 308 researchers from 110 institutions (AI and computational biology). 57.4% found the feedback "helpful/very helpful"; 82.4% found it "more beneficial than feedback from at least some human reviewers".
- Quote (arXiv): "comparable to the overlap between two human reviewers"
- Caveats: overlap measures shared points, not correctness. Users were AI/computational biology researchers rating feedback on their own papers, not clinicians. I did not read the limitations section; the abstract says only "several limitations".

### 4. Hosseini and Horbach
Crossref confirms: Res Integr Peer Rev 2023;8:4, published 18 May 2023, DOI 10.1186/s41073-023-00133-5. A correction exists (2023;8:7). From the PMC page (my fetch tool summarised it; quotes are as it returned them, so recheck):
- Confidentiality: LLMs "may store inputted text"; material "should not be fed into LLMs unless security and data protection measures are put in place".
- Bias: "some biases such as those related to geography, race or class might be reinforced".
- Accountability: "Reviewers should disclose the use of LLMs and accept full responsibility" for their reports; human agents should verify accuracy.
- Also: repeating a prompt can give different output; training for researchers on benefits and risks.

### 5. Sharma et al.
arXiv 2310.13548 (v4, May 2025). The ICLR 2024 venue comes from the brief; the arXiv page I read does not state it. One line: five state-of-the-art AI assistants consistently showed sycophancy, and humans and preference models sometimes preferred convincing sycophantic answers over correct ones. Quote: "sycophancy is a general behavior of state-of-the-art AI assistants". The paper does not test peer review; any link to review is our inference.

### 6. Publisher policies (accessed 2026-11-23)
**Elsevier** (page says "Policy updated: July 2026"):
> "Reviewers should not upload the material/manuscript or any part thereof into a generative AI tool"
> "Generative AI or AI-assisted technologies should not be used by reviewers to assist in the review of the material/manuscript"
> "The reviewer is responsible and accountable for the content of the review." (this sentence came from the fetch tool; my curl line was cut off after "The reviewer is resp")

It also says reviewers should not upload their communications "even if it is just for the purpose of improving language and readability".

**Springer Nature** (nature.com/nature/editorial-policies/ai, current wording; no date shown):
> "Reviewers should disclose any AI use in their report to support transparency and maintain trust in the peer review process."
> "Reviewers must not use AI to generate or substitute their critical evaluation, recommendation or decision-making."

Also: manuscript content "must not be uploaded to unsecured or public AI systems". The group guidance page says reviewers may use "secure or institutionally-approved AI tools". Older wording (2023-24, "peer reviewers do not upload manuscripts into generative AI tools") appeared only in search snippets; I did not open it. Do not use it.

**Wiley** (peer review policy page, no date shown):
> "not uploading manuscripts (or any parts of manuscripts including figures and tables) into Generative Artificial Intelligence (GenAI) tools"
> "If such tools are used to improve a peer review report, then they must be transparently declared in the report."

**JAMA, BMJ, Sage, IOP:** not opened. The Sage page returned 403. Search snippets say Sage and IOP allow AI for language polishing only; unverified, do not cite.

Pattern: Elsevier is strictest (no AI to assist the review); Springer Nature and Wiley allow limited, declared use but bar uploading to public tools. Tell the audience to read the target journal's current policy.

### 7. COPE
Opened via Wayback (live site 403). "Authorship and AI tools", 13 February 2023. Verbatim:
> "AI tools cannot meet the requirements for authorship as they cannot take responsibility for the submitted work."

It also requires authors to disclose AI use in Materials and Methods. It says nothing about reviewers. COPE's site lists a forum session called "Artificial intelligence and peer review" ("the state of artificial intelligence (AI) in peer review is discussed"), but I did not open it, so I have no COPE rule on reviewers to quote. Do not attribute a reviewer-AI rule to COPE.

### 8. Hallucination in AI reviews
Best citable study: Du J et al. LLMs Assist NLP Researchers: Critique Paper (Meta-)Reviewing. EMNLP 2024 main; arXiv 2406.16253. Full-text discussion, verbatim:
> "LLMs are more prone to generating contradictory claims in their reviews and making claims that the authors never stated in the submission, indicating a tendency towards hallucination."

Their category "Unstated statement": "Statements made in the review are not supported by content in the paper." Limits: NLP papers, expert-annotated review segments, no medical manuscripts, no rate of fabricated references.

Newer: Lin T-L et al. HalluPeer, arXiv 2609.03580 (EMNLP Findings 2026). I opened the abstract. It is a benchmark with hallucinations injected into reviews; it says "existing detectors struggle to separate hallucinations from legitimate critique". Preprint-level; no rate in the abstract.

Related, abstract opened: Ye et al., arXiv 2412.01708 "Are We There Yet?". Hidden text in manuscripts can manipulate LLM reviews; LLMs were "potentially assigning higher ratings to incomplete papers compared to full papers". This is manipulation and bias, not hallucination.

Fabricated references in review reports: I found no study that tested references inside AI-generated peer review reports. Studies on LLM-generated citations in general exist (for example a neurocritical care study, PMC13506236) but I saw only search snippets, did not open them, and they are not about reviews. Not usable.

## What this means for a slide

Safe (opened and checked):
- ICMJE V.B: follow the journal's AI policy or ask permission; confidentiality may bar uploading; disclose; check output because it "can be incorrect, incomplete, or biased". Cite as ICMJE Recommendations, updated January 2026.
- NIH bans generative AI in its grant peer review (NOT-OD-23-149, 23 June 2023). Label it as grant review, not journals.
- Elsevier: no uploading and no AI to assist the review. Springer Nature and Wiley: no uploading to public tools; disclose. Write "accessed Nov 2026".
- Liang et al. numbers (30.85% vs 28.58%; 57.4%; 82.4%), with the caveats above.
- Du et al.: LLM reviews contained contradictory and unstated claims (NLP papers).
- COPE: AI cannot be an author (2023).

Not safe or needs care:
- Do not say COPE forbids AI in peer review. I found no such COPE text.
- Do not give a "fabricated reference rate in AI reviews". No review-specific figure found.
- Do not say "AI review is as good as human review". GPT-4/human overlap is similar to human/human overlap, and both are only about 30% to 39%.
- Do not use Springer Nature's old "do not upload" wording as current.
- Sharma et al. is about sycophancy in chat tasks, not review. Present the link as our inference.
- Hosseini and Horbach: recheck quotes on the PMC page before using quotation marks.
- Policies change often. The only dates I saw: Elsevier July 2026, ICMJE January 2026.
