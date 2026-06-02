# Computers & Education — Section-by-Section Writing Framework

A reverse-engineered, reusable **move-structure skeleton** for empirical articles in
*Computers & Education* (Elsevier, ISSN 0360-1315). This captures the *rhetorical moves*
(the sequence of argumentative steps) shared across C&E empirical papers — not the content.
Fill in each `▢` prompt with your own study.

> **Method note.** This skeleton was induced from the **full text** of three genuinely
> open-access C&E empirical articles (read via Europe PMC full-text JATS XML, which serves
> the complete article body, not just the abstract). Three structurally *different* designs
> were deliberately chosen — a survey/SEM study, a controlled experiment, and a multi-group
> path-analysis survey — so that the convergent moves are design-independent and the
> divergent options are visible. Where the three papers disagree on a structural choice
> (e.g. separate vs. merged Conclusion), both options are recorded.

---

## Source articles read (full text) + confidence

| # | Article | Year | Design | URL (open access) | Confidence |
|---|---------|------|--------|-------------------|------------|
| **A** | Vidergor, H. E. — *The effect of teachers' self-innovativeness on accountability, distance learning self-efficacy, and teaching practices* | 2023 | Survey + path/SEM model (N=200 teachers) | DOI: https://doi.org/10.1016/j.compedu.2023.104777 · Full text: https://pmc.ncbi.nlm.nih.gov/articles/PMC9998282/ | **High** (full text read) |
| **B** | Tsai, C.-W., Lin, M.-Y., Cheng, Y.-P., et al. — *The effects of online peer-facilitated learning and distributed pair programming on students' learning* | 2023 | 2×2 factorial quasi-experiment, pretest/post-test (N=128) | DOI: https://doi.org/10.1016/j.compedu.2023.104849 · Full text: https://pmc.ncbi.nlm.nih.gov/articles/PMC10232937/ | **High** (full text read) |
| **C** | Gherghel, C., Yasuda, S., & Kita, Y. — *Interaction during online classes fosters engagement with learning and self-directed study both in the first and second years of the COVID-19 pandemic* | 2023 | Survey + multi-group path analysis (N=1167) | DOI: https://doi.org/10.1016/j.compedu.2023.104795 · Full text: https://pmc.ncbi.nlm.nih.gov/articles/PMC10088368/ | **High** (full text read) |

*All three are 2023 empirical articles, genuinely OA (green OA via PMC).
A 2023–2026 spread was attempted, but most 2024–2026 C&E articles are hybrid-OA whose
"PDF" link resolves back to the paywalled ScienceDirect page; the three above are the
recent articles whose **complete body text** was reliably retrievable. The induced
move-structure is stable across all three and matches C&E's long-standing house style.*

---

## At-a-glance: the shared skeleton

```
Title  (Construct/intervention + outcome + context — descriptive, often "The effect(s) of X on Y")
Abstract  (unstructured single paragraph: problem → study aim → method one-liner → key findings → implication) + Keywords
1. Introduction        ← problem importance → narrow to technology → gap → aim
2. Literature review / framework  ← one subsection per construct, each ending in a hypothesis
   (in some papers this is folded INTO the Introduction as themed subsections)
   └─ "Focus of study" / "The current research"  ← RQs/hypotheses + Fig. 1 (model diagram)
3. Method / "The empirical study"
   ├─ Participants & context
   ├─ Design / procedure (interventions described in detail if experimental)
   ├─ Instruments / Measures (one labelled sub-block per scale; α reported)
   └─ Data analysis (named software + technique)
4. Results            ← organized by RQ / hypothesis / effect; exact inline statistics; tables + figures
5. Discussion         ← restate aim → interpret each finding vs. theory & prior work → implications for teaching/learning → "broad contribution"
   └─ Limitations & future directions  (often a final subsection)
6. Conclusion         ← EITHER its own section OR merged into Discussion
CRediT author statement · Data availability · References
```

**Length envelope observed:** Introduction ~400 words (when Lit Review is separate) up to
~1,900 words (when themed subsections live inside it). Discussion is the longest prose
section (~1,200–1,800 words incl. limitations). Methods is dense and itemized rather than
long-winded.

---

## 1. Introduction

**Function:** convince a general education-technology reader that a *learning/teaching*
problem matters, then funnel to the specific technology and the specific gap. C&E is an
*education* journal that happens to be about computers — the Introduction always opens on the
**educational/learning problem**, never on the technology for its own sake.

**Move structure (the funnel):**

1. **Move 1 — Establish the educational territory & its importance.** Open with a real-world
   educational pressure or stake (in all three papers: the COVID-19 shift to online/distance
   learning and the challenge it posed to teachers/students). State why it matters for
   learners or teachers. *(Paper A para 1; Paper B para 1; Paper C opening.)*
   - ▢ What educational problem/pressure does your study sit inside? Why does it matter for learning or teaching?
2. **Move 2 — Survey what is known & narrow to the technology/approach.** A compact "a review
   of the literature reveals…" sweep that shows the active research conversation, then narrows
   to the specific technology, tool, or pedagogy you study. *(Paper A para 2 explicitly lists
   what prior COVID-DL research has covered.)*
   - ▢ What has prior work established about this technology/approach? What is the active conversation?
3. **Move 3 — State the gap / tension (the hinge sentence).** One sharp sentence naming what
   has *not* been addressed, immediately followed by "Therefore, our study aimed to…".
   In all three this is a *literature gap* ("X was not addressed"; "very few studies have
   explored its effects in online environments"; "very few studies use data from students'
   actions or thoughts").
   - ▢ State the gap in one sentence. Then state your aim in the next sentence.
4. **Move 4 — State the study scope & promise of contribution.** Name the population, setting,
   and the specific relationships/effects investigated; end on the payoff ("Understanding X
   could lead to better preparation/teaching…"). *(Paper A para 4.)*
   - ▢ Who/what/where is your study? What is the concrete payoff for educators/learners?

**Where the RQs land:** **NOT** inside the opening Introduction prose. They are deferred to a
dedicated closing subsection — labelled **"Focus of study"** (Paper A), **"The current research"**
(Paper C), or placed at the end of the Introduction's themed subsections (Paper B). See §2.

**Paragraph count:** 2–4 paragraphs when a separate Literature Review follows (Papers A, B);
expands to several themed subsections when the Introduction *absorbs* the literature (Paper C).

---

## 2. Theoretical / conceptual framework & literature review

**Is it its own section?** *Variable — and this is a genuine fork in the C&E house style:*

- **Option 1 — separate `Literature review` section** (Papers A & B). Contains **one
  subsection per construct/variable in the model** (e.g. "Distance learning", "Innovativeness",
  "DL self-efficacy", "Accountability", "DL teaching practice" in Paper A; "Peer-facilitated
  learning", "Distributed pair programming", "Students' programming skills", "Enjoyment of
  learning", "Intention to learn" in Paper B). Each subsection (~250–600 words) defines the
  construct, reviews evidence, and **builds toward the hypothesis that involves it.**
- **Option 2 — folded into the Introduction** as themed subsections (Paper C: "Challenges to
  maintain… engagement", "Role of interaction…", "Spillover effects…"). No standalone
  "Literature review" header.

**What it does (function), regardless of placement:**
1. Define each construct/variable precisely (so the later model is interpretable).
2. Review prior empirical evidence per construct.
3. **Motivate each hypothesized link** — the review is *instrumental*: every subsection exists
   to justify an arrow in the model, not to be comprehensive for its own sake.

**Explicit theory anchoring:** C&E expects the study to be **grounded in a named learning
theory**, stated near where the model is introduced. Paper C: *"Grounded in social
constructivist theories of learning (Palincsar, 1998)…"*; the theory is then invoked again in
the Discussion (*"Supporting socio-constructivist views of learning…"*). Theory is usually a
**lens woven through the framework**, not always a separate "Theoretical Framework" header.

**The RQ/hypothesis sub-block (the funnel's exit):** a short final subsection that:
- Restates the overarching question in one sentence ("our question was: How might…?").
- Lists numbered RQs (Paper B: three numbered RQs) **or** a numbered chain of hypotheses each
  with a one-clause theoretical rationale + citation (Paper C: "First, …(cites); Second, …(cites);
  Third, …; Finally, we explore…").
- **Points to Figure 1 = the hypothesized model / path diagram.** All three papers introduce a
  conceptual/path model figure here.

- ▢ List one subsection per construct. End each with the hypothesis it supports.
- ▢ Name the learning theory you are grounded in (and re-invoke it in the Discussion).
- ▢ State RQs/hypotheses as a numbered list; reference your Figure 1 model diagram.

---

## 3. Method (a.k.a. "Method", "The empirical study")

**Function:** give enough operational detail to judge validity and (in principle) replicate.
C&E methods are **dense and itemized** — many short labelled sub-blocks rather than long prose.

**Typical subsections (in order):**

1. **Participants / sample.** N, ages/grade/level, country, recruitment, sampling, relevant
   demographics. (Paper C: N=1167 first-year Japanese students across two cohorts; Paper A:
   200 Israeli elementary/secondary teachers; Paper B: 128 undergraduates, four class sections.)
   - ▢ N, who, where, how recruited, key demographics, cohort/group breakdown.
2. **Context / course setting** (especially for interventions). The course, platform, duration,
   delivery mode.
   - ▢ Course, platform, duration, mode.
3. **Design & procedure.** For experiments: name the design explicitly ("2 (PFL vs. non-PFL) ×
   2 (DPP vs. non-DPP) factorial pretest/post-test design"), define each group/condition, and
   **describe each intervention in its own labelled sub-block** with concrete week-by-week or
   step-by-step detail (Paper B devotes ~600 words to the PFL intervention alone). For surveys:
   describe administration, timing, and ethics/consent.
   - ▢ Name the design. Describe each condition/intervention step by step. State ethics/consent.
4. **Instruments / Measures.** **One labelled sub-block per scale/measure.** For each: source
   of the instrument, number of items, example item, response scale, and a **reliability
   coefficient (Cronbach's α)**. (Both survey papers give a sub-block per construct;
   Paper C reports α inline per measure.)
   - ▢ For each measure: source, #items, example item, scale, Cronbach's α.
5. **Data analysis.** A short sub-block naming the **software package** (Paper C: "the R package
   lavaan… 5000 bootstrap samples"; SEM/AMOS in Paper A) and the **technique** (path analysis,
   SEM, multi-group analysis, ANOVA/ANCOVA, mediation with bootstrapped indirect effects),
   plus model-fit indices to be reported and how qualitative data (if any) were coded.
   - ▢ Name software + analytic technique + fit indices + qualitative coding scheme.

**Level of detail expected:** high on *measurement* (every scale's α and provenance) and on
*intervention operationalization*; comparatively terse on generic procedure. Mixed-methods is
common — quantitative scales plus interview/feedback data (Paper B).

---

## 4. Results

**Function:** report findings cleanly, **organized by RQ / hypothesis / effect**, letting tables
and figures carry the numbers while prose states what each number means for the model.

**Organization:** mirror the RQ/hypothesis order. Subsection headers literally restate the
effect under test:
- Paper A: "Descriptive statistics" → "Research hypotheses examination" → "Testing the model and
  questionnaire validation" → "Differences according to background variables".
- Paper B: "Validity and reliability" → "The effect of peer-facilitated learning" → "The effect of
  distributed pair programming" → "The combined effect…" (one subsection per RQ).
- Paper C (no subsections, but ordered): descriptives/correlations → group differences →
  path-model estimates → indirect (mediated) effects.

**Standard opening move:** report **descriptive statistics + reliability/validity first**
("Descriptive statistics and correlations… are presented in Table 1"), then inferential tests.

**How statistics are reported — report the full inline test, not just "significant":**
- t-tests with df, statistic, exact p: `t(1159) = 23.74, p < .001`.
- Path/mediation effects with unstandardized estimate, SE, exact p, **and 95% CI**:
  `b = 0.181, SE = 0.02, p < .001, 95% CI [0.136, 0.228]`.
- Bootstrapped indirect effects are reported explicitly (number of bootstrap samples stated).
- Variance explained reported as `R²`/percentage ("6% in 2020 and 8% in 2021").
- SEM papers report model-fit indices and validity/CFA before interpreting paths.
- Exact p-values preferred; non-significant results reported plainly (`p = .388`), not hidden.

**Table/figure usage:** Tables carry descriptives, correlations, reliability, and full
parameter estimates (the three papers had 1, 4, and 6 tables). Figures are used sparingly and
purposefully: **Fig. 1 = hypothesized model; Fig. 2 = the fitted model with path coefficients
overlaid.** Prose points to each ("The results are shown in Fig. 2").

- ▢ Order subsections by RQ/hypothesis. Lead with descriptives + reliability.
- ▢ Report each test fully (statistic, df, exact p, effect size / CI). Put parameter tables + a fitted-model figure.

---

## 5. Discussion

**Function:** the interpretive heart. Translate statistical findings back into claims about
**learning and teaching**, position them against theory and prior work, and argue why they
matter beyond this one study. This is the most formulaic section — the move sequence below was
identical across all three papers.

**Move structure:**

1. **Move 1 — Restate the aim and hypotheses** (1 opening paragraph). "This study aimed to…
   We hypothesized that…". Re-orients the reader before interpretation. *(Paper C para 1.)*
   - ▢ One paragraph: restate aim + what you hypothesized.
2. **Move 2 — Interpret each key finding, one at a time, anchored to theory.** Walk the findings
   in model order. Each gets: what was found → why (mechanism) → **explicit tie to the named
   learning theory** ("Supporting socio-constructivist views of learning (Palincsar, 1998),
   our results showed…").
   - ▢ For each finding: state it, explain the mechanism, connect to your theory.
3. **Move 3 — Position against prior work.** Signal-phrase every finding as confirming, extending,
   or replicating ("In line with previous research…", "Replicating previous research
   (Sagayadevan & Jeyaraj, 2012)…", "this result replicates…"). Note where results *diverged*
   from expectation and offer an explanation (Paper B: distributed pair programming showed no
   effect — interpreted via interview feedback).
   - ▢ For each finding: cite the prior work it agrees/disagrees with; explain any surprise.
4. **Move 4 — Implications for learning & teaching (the obligatory move).** Every interpreted
   finding is converted into concrete advice for educators ("lecturers who want to keep students
   motivated could include interactive activities such as group work…"; "teachers may provide
   more opportunities for brainstorming…"). This is where C&E's *educational* identity is
   enforced — no finding is left as a bare statistical result.
   - ▢ For each finding: what should a teacher / instructional designer / institution do differently?
5. **Move 5 — Argue the broad contribution / relevance.** A paragraph naming "the most important
   contribution" and why it generalizes beyond the immediate setting (Paper C: online interaction
   has *spillover* effects on learning *outside* class → reframes the stakes; Paper B: "three
   different values and contributions to theory and practice").
   - ▢ State your single most important contribution and why it matters beyond this study/sample.
6. **Move 6 — Limitations & future directions** (usually a labelled final subsection). Limitations
   are **grouped by type** (self-report, correlational/causal inference, single-site sample,
   construct coverage) and **each limitation is paired with a concrete future-research direction**
   (e.g. "cross-sectional design → run longitudinal studies"; "quantitative only → verify with
   interviews/focus groups"; "one university → test generalizability elsewhere"). Often closes by
   warning against overgeneralization ("'the more the better' is not always the case").
   - ▢ List limitations by type; pair each with a future study that would address it.

---

## 6. Conclusion

**Present or merged? — a real fork:**
- **Merged into the Discussion** (Paper A folds a "Conclusions and recommendations" subsection
  *inside* Discussion; Paper C has no separate Conclusion at all — the Discussion's final
  paragraphs carry the takeaway).
- **Its own section** (Paper B: a standalone `Conclusions` section).

**When present as its own section, its move structure (Paper B):**
1. Re-state the educational problem and what the study did about it (1 paragraph).
2. **Answer each RQ in turn**, restating the verdict and giving practitioner recommendations
   ("Based on the first research question… the researchers recommend that PFL could be adopted…").
3. A "contributions" paragraph enumerating 2–3 specific contributions to theory and practice.
4. A closing call to educators/researchers (forward-looking, slightly hortatory:
   "the researchers encourage online educators… to apply innovative teaching strategies…").

- ▢ Decide: separate Conclusion or merged? If separate, answer each RQ + list contributions + close with a call to educators.

---

## Cross-cutting conventions (what makes it read as *Computers & Education*)

1. **Every analysis is tethered to a learning/teaching construct.** No result is reported as a
   bare statistical or technological fact. Variables are framed as learning constructs
   (engagement, self-efficacy, enjoyment of learning, intention to learn, self-directed study,
   programming *skill development*) and findings are always cashed out as implications for how
   people *learn* or how teachers *teach*. The technology is the independent variable or the
   environment — the **dependent variables are educational outcomes.**
2. **"Broad relevance" is argued explicitly, twice.** Once in the Introduction (Move 4 payoff)
   and again in the Discussion (Move 5 "most important contribution"). The argument is typically:
   *this generalizes beyond the immediate course/sample/pandemic because the underlying learning
   mechanism (interaction → engagement; innovativeness → efficacy; peer facilitation → skill) is
   general.* Spillover, transfer, and "post-pandemic this will persist" framings are used to
   stretch relevance.
3. **Theory bookends the paper.** A named learning theory is introduced with the model and
   re-invoked in the Discussion ("Supporting socio-constructivist views…"). The contribution is
   framed as refining/extending that theory *and* informing practice ("contributions to the
   theory and practice of online education").
4. **The model figure is the spine.** Fig. 1 (hypothesized model) → Fig. 2 (fitted model with
   coefficients). The whole paper can be read as: propose the arrows → test the arrows →
   interpret the arrows.
5. **Practitioner address is constant.** "Lecturers should…", "teachers may…", "online educators
   are encouraged to…". C&E papers speak to educators, not only to researchers.
6. **Measurement transparency.** Every construct has a named, sourced scale with a reliability
   coefficient; analysis names its software. This is a quiet but consistent quality signal.
7. **Citation density is highest in the Lit Review and Discussion** (clusters of 3–6 refs per
   claim) and the Discussion's signal phrases ("In line with…", "Replicating…") do the
   positioning work.

---

## Coverage / honesty notes

- All six major sections (Introduction, Framework/Lit Review, Method, Results, Discussion,
  Conclusion) were read in **full text** for all three papers — no section was inferred from an
  abstract or summary.
- The two genuine **structural forks** in C&E's house style (separate vs. embedded Literature
  Review; separate vs. merged Conclusion) are documented above with which paper does which,
  rather than presented as a single rigid template.
- This skeleton is induced from **three 2023 empirical articles**. A wider 2024–2026 sample was
  attempted but blocked by hybrid-OA paywalls (PDF links resolving to ScienceDirect). The
  induced moves match C&E's stable, long-standing IMRaD-plus-framework house style, so the
  skeleton should transfer to current submissions; if you need 2025–2026 confirmation, the
  arXiv-hosted C&E preprints (e.g. *Mapping student–AI interaction dynamics…*, 2025,
  https://arxiv.org/pdf/2506.02993) are openly readable.
