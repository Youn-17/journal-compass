---
name: journal-compass
description: |
  Distill a journal into a reusable submission companion.
  把一本期刊蒸馏成一个可复用的投稿伴侣技能。
  Learns the journal's topic taste, writing style, author guidelines, and aims & scope —
  reading open-access full texts where available — then guides four steps:
  TOPIC (fit verdict) → WRITE (section framework) → POLISH (house style) → SUBMIT (cover letter, title page, declarations).
  它读懂这本刊的选题方向、写作风格、作者指南与 aims & scope（有开放获取全文时连正文一起读），
  带你走完四步：选题适配判断 → 章节框架写作 → 按刊风格润色 → 生成投稿材料（cover letter、title page、声明清单）。
  Two ways in: (1) a journal name → distill directly; (2) a vague need → recommend candidates first.
  Triggers: "distill journal X", "蒸馏 X 期刊", "这篇适合投 X 吗", "按 X 风格写/改",
  "帮我写投 X 的 cover letter / title page", "我这个研究投哪本刊好", "更新 X 期刊的 skill".
---

# Journal Compass

A skill that studies one journal and builds a standalone `<journal-slug>-fit` companion for it.
The companion supports four steps: **TOPIC → WRITE → POLISH → SUBMIT**.

---

## Inputs

What the user can provide:

| Input | Effect |
|-------|--------|
| Journal name (+ publisher / ISSN) | Required — disambiguates look-alikes |
| PDFs of the journal's papers | Improves writing-framework extraction significantly |
| Author's own draft or abstract | Companion runs a fit check on it as a bonus deliverable |
| Rival journal name | Required for the rival-journal test; pick the closest competitor if the user has none |

---

## Core method

**Three evidence streams:**

| Stream | Where | What it tells you |
|--------|-------|------------------|
| **Claims** | Aims & Scope, editorials, author guidelines | The official position |
| **Published** | Recent papers + open-access full texts | What actually gets accepted |
| **Rejected** | Reviewer guidelines, desk-reject signals, author reports | The hidden filter |

**The claims-vs-reality gap** is the most useful finding. When a journal says it welcomes X but publishes under 5% X, that gap is a desk-reject risk for X-only submissions. Always compare the two streams.

**Three stages every submission must clear:**

```
Stage 1 — Editor's desk     (~30 seconds): scope, contribution type, obvious disqualifiers
Stage 2 — Peer review       (weeks):       rigor, framing, novelty standard
Stage 3 — Accepted paper shape:            abstract recipe, structure, title pattern, word limits
```

The companion maps your work to each stage so you know *which* stage fails, not just whether a paper fits.

**Rival-journal test (noise filter):**

A finding goes into the profile only if it would change which of two similar journals you'd submit to.
If both journals want it equally, it's a field-wide norm — discard it.
This is why you always compare against one rival journal.

---

## Build workflow

Seven steps. Stop at the two ⏸ checkpoints for explicit author confirmation before proceeding.

### Step 1 — Frame the build

Confirm before starting research:

- **Exact journal** — full name + publisher (e.g. *Computers & Education*, Elsevier). Disambiguate look-alikes (*Computers & Education* vs *Computers & Education: Artificial Intelligence*).
- **Rival journal** — one similar journal for the test. If the author has none, pick the closest competitor yourself and name it.
- **Material on hand** — any PDFs of the journal's papers? The author's own draft or abstract? First-hand papers beat anything scraped.
- **Depth** — quick (Stage 1 editor-screen only) or full (all four companion steps, default: full).
- **New or update** — scan `.claude/skills/*-fit/`. If one exists, switch to "Updating an existing skill" at the end of this file.

Create the self-contained evidence folder **before starting research** (so subagents have a place to write):

```
.claude/skills/<journal-slug>-fit/
├── SKILL.md                          # final product (built in Step 6)
└── references/
    ├── evidence/
    │   ├── claims.md                 # what the journal says it wants
    │   ├── published.md              # what it actually publishes (≥5 papers)
    │   ├── rejected.md               # what gets rejected and why
    │   ├── guidelines.md             # author guidelines → submission kit elements
    │   ├── writing-framework.md      # section-by-section moves (from OA full texts)
    │   └── rival-<slug>.md           # comparison against the rival journal
    └── corpus/                       # saved PDFs, guideline snapshots
```

### Step 2 — Gather evidence

Fill each `evidence/*.md`. If subagents are available, run these in parallel (one per stream). Without subagents, run sequentially — the process is identical.

**Every claim must have a source URL and a confidence tag: `[HIGH]` = verbatim from official source; `[MED]` = official Elsevier/Springer/etc. general policy; `[LOW]` = inferred.**

---

#### `claims.md` — what the journal says it wants

Prompt for this stream:

```
Research <journal name> (<publisher>, ISSN <if known>).

Find and record:
1. The full Aims & Scope text — quote it verbatim.
2. The article types it accepts (research paper, review, short communication, etc.) and any explicit exclusions.
3. Any recent editorials or editor statements about scope, direction, or what they want more/less of.
4. The explicit "we do not publish X" statements, if any.

For each item, record: what it says, the source URL, and a confidence tag [HIGH/MED/LOW].
Distinguish between hard rules ("papers must be X") and soft guidance ("we prefer Y").

Write findings to: <skill-folder>/references/evidence/claims.md
```

---

#### `published.md` — what the journal actually publishes

Prompt for this stream:

```
Research what <journal name> has actually published in the last 2–3 years.

Use OpenAlex, Semantic Scholar, or the journal's own website to find recent papers.
If $ARIS_REPO/tools/openalex_fetch.py is available, use it to pull the corpus efficiently.
Analyze ≥5 papers (the more the better).

Record:
1. Topic clusters — what subjects appear most, with rough frequency estimates.
2. Contribution-type mix — approximately what % is: empirical / theory / methods / review / design.
3. Hot areas (rising fast), saturated areas (so many papers it's hard to stand out), and gaps (editors would likely welcome but few submit).
4. 4–6 concrete recent paper examples with titles + what made them publishable.
5. SAY vs DO: where does the journal's actual output differ from its stated aims?

Write findings to: <skill-folder>/references/evidence/published.md
```

---

#### `rejected.md` — what gets rejected

Prompt for this stream:

```
Research what <journal name> rejects and why.

Sources to check:
- The journal's reviewer guidelines and "Guide for Authors" (especially any "we will desk-reject if..." language)
- Editorials about submission quality or common reasons for rejection
- Author forum reports (Reddit r/AskAcademia, ResearchGate, academic blogs)
- Retraction notices (reveal what slips through vs what gets caught)

Record for each rejection reason:
- The specific failure mode (e.g. "no measured learning outcome", "out of scope", "method bar not met")
- Whether it's a desk-reject (Stage 1) or peer-review failure (Stage 2)
- The source and confidence tag

Also record: acceptance rate if officially published (mark estimates as [LOW]), typical review timeline if available.

Write findings to: <skill-folder>/references/evidence/rejected.md
```

---

#### `guidelines.md` — author guidelines → submission kit

Prompt for this stream:

```
Research the submission requirements of <journal name>.

Find the official Guide for Authors (usually on the journal's homepage under "Submit" or "Authors").
Record each requirement in a form that can be turned into a fill-in template:

1. Title page requirements — what goes on a separate title page vs the anonymized manuscript (for double-blind review); what must be stripped for anonymity.
2. Cover letter — expected or optional? What should it contain? What must NOT go in it?
3. Abstract — structured or unstructured, word cap, required elements.
4. Highlights — count, character limit.
5. Mandatory declarations — list each: competing interest, CRediT author statement, data availability, ethics/consent, funding, generative-AI-use. For each, note whether mandatory or conditional.
6. Format gates — word limit, reference style, section numbering, accepted file types.

For every item: source URL + confidence tag.
Flag any field that, if omitted, would trigger a desk reject.

Write findings to: <skill-folder>/references/evidence/guidelines.md
```

---

#### `writing-framework.md` — section-by-section moves from full texts

Prompt for this stream:

```
Extract the writing framework of <journal name> by reading open-access full texts.

Step 1: Find 2–3 open-access papers from this journal (try OpenAlex is_oa filter, Unpaywall, Europe PMC, or author-deposited preprints). Prefer recent empirical papers. Record titles + URLs.

Step 2: For each paper, extract the MOVE STRUCTURE of each section — the sequence of rhetorical actions, not the content:
- Introduction: what does it open on? how does it narrow? where does the gap sentence appear? where do RQs land?
- Theory/framework section (if present): separate section or folded into intro? structure?
- Methods: what subsections? level of detail expected (e.g. one block per scale with reliability stats)?
- Results: organized by RQ or by hypothesis? how are statistics reported inline?
- Discussion: fixed moves (restate → interpret vs theory → implications → limitations+future)?
- Conclusion: merged into discussion or separate?

Step 3: Note where two or more papers follow different patterns ("fork") — both are valid for this journal.

If no OA full text is available, note this and infer style from abstracts only — mark as [INFERRED].

Write findings to: <skill-folder>/references/evidence/writing-framework.md
Make it a fill-in skeleton, not a description.
```

---

#### `rival-<slug>.md` — comparison against the rival journal

Prompt for this stream:

```
Compare <journal name> and <rival journal name>.

For 2–3 recurring topic areas that both journals cover, ask:
- How would THIS journal handle it vs the rival?
- What's the key difference in what they accept?

Focus on: contribution types (empirical vs theory vs design), evidence bar, framing requirements, style differences.
For each difference, ask: "Would this change which journal I'd submit to?" — if yes, it's specific to this journal; if no, it's field-wide noise.

Tag every finding as either:
- `[SPECIFIC]` — genuine difference between the two journals
- `[FIELD-WIDE]` — both journals want this equally; will be filtered out

Write findings to: <skill-folder>/references/evidence/rival-<slug>.md
```

---

After all streams are filled, also do a **sibling comparison check** on `published.md`: tag any recurring topic/style feature that appears identically in the rival journal as `[FIELD-WIDE]`.

> ⏸ **Checkpoint 1 — Evidence review.**
> Show a one-page summary covering:
> - Source count and confidence distribution per file
> - Top 3–5 topic clusters from `published.md`
> - The sharpest 2–3 SAY vs DO gaps
> - Whether OA full text was found for `writing-framework.md`
> - Key submission-kit items (separate title page? mandatory declarations?)
> - The main `[SPECIFIC]` findings from the rival comparison
>
> **Do not proceed to Step 3 until the author confirms the evidence is adequate.**
> Thin evidence → thin profile. Better to flag gaps here than produce a misleading companion.

---

### Step 3 — Name the gaps

From `published.md` and `claims.md`, list every place the journal's official position diverges from what it actually publishes.

For each gap, classify it:

| Type | Pattern | What it means |
|------|---------|---------------|
| **Aspirational** | Claims to want X, publishes almost none | X-only submissions are high-risk; frame X as support, not the main contribution |
| **Narrower than stated** | Claims broad scope, clusters in a sub-area | Position inside the cluster |
| **Drifting** | Recent issues diverge from older self-description | Weight last 1–2 years; flag the trend |
| **Hidden bar** | "Welcomes all methods" but accepted papers share an unstated rigor floor | Name the floor from the corpus |

These gaps feed directly into the Stage-1 red-flag list in the companion.

### Step 4 — Build the journal profile

Read `references/signal-mining.md` for how to separate genuine journal-specific signals from field-wide noise. Then write the profile organized by three stages:

**Stage 1 profile** (from `claims.md` + `rejected.md` + gaps):
- Scope boundaries (what's in, what's out)
- Accepted contribution types and their mix
- Desk-reject red-flag list (3–7 items, each with a source)

**Stage 2 profile** (from `published.md` + `rejected.md`):
- Method/rigor bar (what accepted papers share that the journal doesn't state explicitly)
- How a contribution must be framed to satisfy this community
- Novelty standard (incremental OK? replication valued? big-claim expected?)

**Stage 3 profile** (from `writing-framework.md` + `published.md`):
- Abstract recipe: structured or not, word cap, sentence-by-sentence function sequence, with one real example
- Title patterns: 2–3 patterns with real examples
- Section structure: the standard sequence; where the framework/theory section lives; where limitations go
- Length range, citation density, reference style, voice

**Quality check before proceeding:**
- At least 3 Stage-1 findings that pass the rival-journal test (would change submission decision)
- At least 1 claims-vs-reality gap named and classified
- Stage 3 includes at least one concrete abstract example and one real title

> ⏸ **Checkpoint 2 — Profile review.**
> Show:
> - Stage-1 findings with sources
> - The "this journal vs rival" one-liner
> - The named gaps
> - The abstract recipe + one real example
> - The submission-kit summary (from `guidelines.md`)
>
> **Do not write the child skill until the author confirms the profile direction.**

### Step 5 — Calibrate

Test that the profile discriminates correctly. Use a subagent where possible (to avoid grading your own work):

**Hit test**: take 2 papers the journal actually published (held out from Step 2, not used to build the profile). Run them through the draft Stage-1 logic. Both must score **SUBMIT**. If either fails, the Stage-1 findings are wrong — revise and retest.

**Redirect test**: take 1 paper from the rival journal, or a clearly off-topic paper. Run it through Stage-1. It must score **REDIRECT** with a specific, correct reason. If it scores SUBMIT, the findings are too broad — they lack discriminating power.

**Both must pass before writing the child skill.**

### Step 6 — Write the child skill

Read `references/fit-skill-template.md` and fill it with the profile. The child skill must:

1. **TOPIC step**: run the three-stage logic and return SUBMIT / RESHAPE / REDIRECT with per-stage reasoning; propose 2–3 topic angles that fit the journal's current gaps
2. **WRITE step**: give the section-by-section skeleton, abstract recipe, and title patterns — each anchored to a real published paper
3. **POLISH step**: for any draft pasted in, produce before → after edits targeting this journal's style; enforce word/abstract limits; clear every desk-reject flag
4. **SUBMIT step**: generate a cover letter draft, a title-page checklist (with an anonymization strip-list if the journal is double-blind), highlights, and a declarations checklist

State limits honestly at the bottom: sample size, research date, "fit improves odds, not a guarantee", "verify against the live Guide for Authors before submitting".

Write the skill to `<journal-slug>-fit/SKILL.md`.

### Step 7 (optional) — Trigger check

Verify that the description field triggers naturally on how users actually ask:
- "Is this a fit for [journal]?"
- "投 [journal] 行不行"
- "按 [journal] 风格帮我写引言"
- "帮我写投 [journal] 的 cover letter / title page"

If any common phrasing isn't covered, update the description.

---

## Entry points

**Named journal** → Step 1.

**Vague need** ("Where should I submit a study on GenAI and learning analytics?") → recommend 2–3 contrasting candidates first, then distill the one the author picks:

```
### Candidate: [Full journal name]  ⚡ already distilled / 🆕 needs distilling
Position: [one line — what it publishes and for whom]
Why it fits: [match to topic, method, manuscript stage]
Risk: [acceptance bar, typical sticking points]
vs the others: [the key trade-off]
```

Check `.claude/skills/*-fit/` first — an already-distilled journal is ready to use without any new research.

---

## Calibration quality gates

A profile is only valid if:
- At least 3 Stage-1 signals pass the rival-journal test
- At least 1 SAY-vs-DO gap is named and classified
- The hit test and redirect test both pass
- Stage 3 is grounded in real published examples, not generic advice

If a gate fails, fix the profile before shipping the child skill. It is better to say "this journal has sparse public data, the profile is limited" than to ship a companion that confidently gives wrong guidance.

---

## Special cases

**Broad/megajournal** (*Nature Communications*, *PNAS*, *Science Advances*): Stage-1 topic signals are weak because scope is wide. Shift weight to Stage 2 (contribution magnitude, novelty framing, "broad significance") and Stage 3 (writing quality, claim precision). The fit verdict becomes "is it impactful enough?" not "is it on-topic?".

**Conference** (*CHI*, *NeurIPS*, *AERA*): add deadline cadence, page limit, and rebuttal culture to the profile. Some venues use explicit scoring rubrics (e.g. soundness/excitement) — include them. In the SUBMIT step, note that cover letters are usually not required but submission checklists are.

**Non-English journal** (*Chinese Social Sciences*, CNKI-indexed journals): use appropriate indexes; note that national core-journal style requirements are often stricter and more prescriptive than international journals.

**Thin evidence** (fewer than 5 readable full papers, or no official reviewer guidelines): cap Stage-1 signals at 2–3, label each "[LIMITED SAMPLE]", say so in the companion's honesty section, and lean on any author-supplied PDFs.

**No open-access full text**: build the writing framework from abstracts only; mark every inference "[INFERRED FROM ABSTRACTS]" — the framework is useful but less reliable than one grounded in full texts.

**Author-supplied draft**: after building the companion, run the full four-step check on the draft as a bonus deliverable. Give the SUBMIT step output (cover letter + title page + declarations) specific to that draft's actual authors and content.

---

## Updating an existing skill

When the author says a journal has changed (new editor, scope update, or "redo the distillation"):

1. Read the existing SKILL.md; find the research date in the honesty section; note how stale it is.
2. Re-collect only what changes: `published.md` (latest year of papers), `claims.md` (any guideline updates, scope announcements), `rival-<slug>.md` (editorial-board changes).
3. Reconcile: if a new trend reinforces an existing signal → add the new evidence. If it contradicts → mark the shift and update the signal. If a new hot area appears → add a new signal.
4. Update the "recent shifts" note and research date. Do not rewrite the whole companion — incremental update only.

---

## Honesty

- Never invent acceptance rates, review timelines, or editorial preferences not supported by the evidence
- Never label a field-wide norm as this journal's specific taste
- Always surface the gap between what the journal claims and what it actually publishes
- The submission kit is a draft — users must verify it against the live Guide for Authors before submitting
- Fit improves the odds. It is not a guarantee of acceptance

---

## Credits

Footer for child skills:
`> Generated by Journal Compass · researched [date] · [N] papers · https://github.com/Youn-17/journal-compass`
