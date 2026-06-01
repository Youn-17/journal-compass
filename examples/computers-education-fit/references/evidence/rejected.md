# Computers & Education (Elsevier, ISSN 0360-1315) — BLOCK Evidence Stream

**What gets a submission KILLED at C&E, and why.**

Confidence tags: **[HIGH]** = direct from official Guide for Authors / Elsevier; **[MED]** = consistent secondary aggregators or well-reasoned third-party guides citing official policy; **[LOW]** = estimate / unverified / single-source inference. Acceptance-rate numbers are flagged explicitly — **no fabricated figures**.

Last researched: 2026-06-01.

---

## 1. Desk-Reject Triggers (returned without review)

The journal explicitly states it will return non-conforming papers without review:

> "Authors should take care to refer to and abide by the author guidelines. **Papers that do not address the criteria outlined in the author guidelines will be returned without review.**"
— Official Guide for Authors **[HIGH]**
Source: https://www.sciencedirect.com/journal/computers-and-education/publish/guide-for-authors

### 1a. Out-of-scope: technology without an educational/learning angle
Core scope statement (verbatim from Aims and Scope):

> "_Computers & Education_ aims to increase knowledge and understanding of ways in which digital technology can **enhance education**, through the publication of high-quality research, which **extends theory and practice**. The Editors welcome research papers on the **pedagogical uses of digital technology**, where the **focus is broad enough to be of interest to a wider education community**."
**[HIGH]** — Official Guide for Authors (URL above)

Red flag: pure technology / CS / AI with no demonstrated impact on learning or teaching. Confirmed by the explicit clause below.

### 1b. "Computers as a delivery platform only is insufficient"
Verbatim from Guide for Authors:

> "Papers that include discussions of the implementation of software and/or hardware should focus on the context of use, the user/system interface, usability issues and evaluations of the user experience and **impacts ... particularly on the implications for learning and teaching. Computers as a delivery platform only is insufficient. Detailed information on implementation architecture should NOT be included in the paper, but may be provided via URLs.**"
**[HIGH]** — Official Guide for Authors (URL above)

Implication: papers that lead with implementation architecture / system internals and bury (or omit) the learning-and-teaching contribution are out of scope. Architecture detail belongs in URLs/appendices, not the paper body.

### 1c. Small-scale / single-context evaluations with no broader relevance
Verbatim:

> "We **do not publish small-scale evaluations of specific software/systems in specialist domains or particular courses in individual institutions** (unless the findings have **broader relevance that is explicitly drawn out** in the paper)."
**[HIGH]** — Official Guide for Authors (URL above)

Red flag: single-institution / single-course deployment study with no external-generalizability discussion and no theoretical contribution. The "unless..." escape hatch requires the authors to *explicitly* draw out broader relevance — implicit relevance is not enough.

### 1d. AI/CS papers where the novelty is the model, not the educational consequence → routed to C&E: AI
The Guide for Authors directs AI/technology-led work to the sister journals:

> "Authors are also welcome to submit to the journal's open access companion titles, **Computers & Education Open** or **Computers & Education: Artificial Intelligence**."
**[HIGH]** — Official Guide for Authors (URL above)

C&E: AI (ISSN 2666-920X) is the explicit home for AI-application/AI-education work:
> CAEAI "aims to provide a platform for researchers, developers, and educators to present research studies ... and demonstrate **novel systems and pedagogical innovations on applications of artificial intelligence in education and AI education.**"
**[HIGH]** — CAEAI Guide for Authors: https://www.sciencedirect.com/journal/computers-and-education-artificial-intelligence/publish/guide-for-authors

Practical rule (third-party guide synthesizing the above policy): when a paper introduces an AI or analytics **model/architecture/prompt-scheme as its named novelty** but does not connect it to learning theory, feedback design, assessment, or pedagogy — or when the methods section describes implementation architecture in more detail than the learner experience — the better-fit venue is **C&E: AI**, and a submission to the flagship C&E risks a scope desk-reject. **[MED]**
Source: https://manusights.com/blog/computers-and-education-submission-guide

### 1e. Tool/satisfaction reports with no learning-outcome evidence
Third-party guide (synthesizing official scope) lists the recurring desk-screen rejection patterns at C&E **[MED]**:
1. **Tool evaluation without learning outcomes** — studies measuring only satisfaction scales or intention-to-use (e.g., TAM constructs) without validated learning measures.
2. **AI novelty without educational framing** — papers emphasizing model architecture rather than educational consequences (see 1d).
3. **Single-context studies lacking generalizability** — deployment research with no external applicability discussion or theoretical contribution (see 1c).
Source: https://manusights.com/blog/computers-and-education-submission-guide

### 1f. Systematic reviews / meta-analyses without proper structure
The Guide explicitly conditions acceptance of reviews:

> "We welcome systematic review papers and meta-analyses that include **clear research questions, a framework of analysis, and conclusions that reflect the aims of the paper. See PRISMA guidelines** for further advice."
**[HIGH]** — Official Guide for Authors (URL above)

Implication: a review lacking explicit RQs, an analysis framework, or PRISMA-style rigor is a rejection risk.

> Note on "no theoretical framework" / "weak samples": these are NOT spelled out as standalone verbatim desk-reject bullets in the public Guide for Authors. The Guide's leverage is via "extends theory and practice" (1a) and "small-scale evaluations" (1c). Treat "missing theoretical framework" and "small/weak sample" as **strongly implied** desk/early-review risks rather than quoted policy lines. **[MED]**

---

## 2. Reviewer / Editorial Assessment Criteria

C&E uses **double-anonymized** review. Editor screen first, then ≥2 reviewers:

> "This journal follows a **double anonymized review process**. Your submission will **initially be assessed by our editors** to determine suitability for publication in this journal. If your submission is deemed suitable, it will typically be sent to a **minimum of two reviewers** for an independent expert assessment of the scientific quality. The decision ... will be taken by our editors."
**[HIGH]** — Official Guide for Authors (URL above)

So there is an explicit **two-stage gate**: (1) editor suitability/scope screen (the desk-reject stage), then (2) ≥2 expert reviewers on scientific quality.

What editors/reviewers weigh (synthesized from scope + third-party guide) **[MED]**:
- **Educational-technology substance** — a substantive edtech contribution, not a demo.
- **Learning-outcomes connection** — technology tied to learning/teaching outcomes empirically or theoretically; the criterion is that technology must change *learning, teaching, feedback, self-regulation, assessment, or educational decision-making* — not that it is novel in CS terms.
- **Methodological rigor** — empirical, design-based, or qualitative methods of top-tier quality.
- **Relevance beyond a single software/institution/domain** (generalizability / theory).
Source: https://manusights.com/blog/computers-and-education-submission-guide

No separate public "reviewer guidelines" document distinct from the Guide for Authors and Elsevier's general peer-review pages was located. **[MED — absence noted, not confirmed nonexistent]**

Appeals: one formal appeal per submission allowed under Elsevier's Appeal Policy; appeal decision is final. **[HIGH]** (Guide for Authors)

---

## 3. Acceptance Rate & Review Timeline

### Acceptance rate
- **No reliable, officially-published acceptance rate was found.** Major aggregators (Resurchify, Researcher.Life/Editage) display an "Acceptance Rate" heading but state the figure is not provided and recommend contacting the editor. **[HIGH that it is unpublished]**
  Sources: https://www.resurchify.com/impact/details/17645 , https://www.editage.com/research-solutions/journal/computers-education/2640
- C&E is widely regarded as highly selective (top-tier Q1 edtech journal), but **any specific percentage (e.g., ~8–12%) circulating online is an UNVERIFIED ESTIMATE.** Do not cite a number as fact. **[LOW]**

### Timeline (from ScienceDirect "Journal Insights" metrics, surfaced via third-party guide)
These are journal-level medians/averages, "**not a promise for one manuscript**":
- **Submission to first decision: ~7 days** **[MED]**
- **Review time (decision after review): ~48 days** **[MED]**
- **Submission to acceptance: ~190 days** **[MED]**
- **Acceptance to online publication: ~2 days** **[MED]**
Source: https://manusights.com/blog/computers-and-education-submission-guide
(These mirror the format of Elsevier ScienceDirect "Journal Insights" panels; verify on the live journal page before quoting, as they update.)

### Author-reported timing (SciRev)
- **Immediate-rejection decision time: ~31 days** (i.e., desk rejections reported by authors came back in about a month — note this is *longer* than the 7-day "first decision" insight metric, reflecting small/older sample). Most other SciRev fields are "n/a" for this journal. **[MED — small sample, author self-report]**
Source: https://scirev.org/journal/computers-and-education/

### Journal standing (context, not a gate)
- Impact Factor (2024): **10.5** (per ScienceDirect journal header) **[HIGH]**; a separate aggregator lists IF 13.85 **[MED — conflicting]**.
- CiteScore: **23.7** (ScienceDirect header) **[HIGH]**.
- h-index: **253** (Resurchify) **[MED]**.
Sources: https://www.sciencedirect.com/journal/computers-and-education/publish/guide-for-authors , https://www.resurchify.com/impact/details/17645

---

## 4. Editorial "why we reject" statements

- The strongest *official* "we reject" signal is the Guide for Authors itself: the verbatim clauses in Section 1 (returned-without-review, "delivery platform only is insufficient", "we do not publish small-scale evaluations", review-paper structure requirements). **[HIGH]**
- A frequently-referenced **Neil Selwyn** editorial line ("Looking beyond learning: notes towards the critical study of educational technology", *J. Computer Assisted Learning*, 2010; and "Telling tales on technology") critiques edtech research that is celebratory/promotional and disconnected from real educational consequence. This is **adjacent/influential thinking**, NOT a C&E desk-reject policy document — Selwyn published it elsewhere. Use as context for the journal's "education-first" ethos, not as a citable C&E rejection rule. **[MED — relevance HIGH, but not a C&E editorial]**
  Source: https://onlinelibrary.wiley.com/doi/abs/10.1111/j.1365-2729.2009.00338.x
- A specific, widely-cited C&E *editors' editorial* enumerating numbered rejection reasons was **searched for but not located** in the public record during this research. Do not invent one. **[LOW — not found]**

---

## TL;DR — Top desk-reject red flags (most important first)

1. **No learning/teaching impact** — technology described but no demonstrated educational consequence ("computers as a delivery platform only is insufficient"). **[HIGH, verbatim]**
2. **AI/CS novelty leads, education trails** — named contribution is a model/architecture/prompt scheme, not a pedagogical effect → belongs in **C&E: AI**, not flagship C&E. **[HIGH route policy / MED specifics]**
3. **Small-scale, single-course/single-institution evaluation** with no explicitly-drawn broader relevance. **[HIGH, verbatim]**
4. **Tool/satisfaction report** measuring only acceptance/intention-to-use, no validated learning outcomes. **[MED]**
5. **Implementation-architecture-heavy** paper (internals in body instead of URLs). **[HIGH, verbatim]**
6. **Review/meta-analysis without clear RQs, analysis framework, PRISMA.** **[HIGH, verbatim]**
7. **No theoretical extension / weak sample** — implied via "extends theory and practice" + "small-scale evaluations"; strong early-review risk though not a quoted standalone bullet. **[MED, inferred]**
