---
name: imprimatur
description: |
  Distill a journal into a reusable skill — the way a person-distiller captures a thinker, this captures a journal.
  蒸馏一本期刊：像蒸馏一个人那样，把一本期刊蒸馏成一个可复用的 skill。
  It learns the journal's topic taste, direction, writing style, author guidelines, and aims & scope — reading open-access full texts when it can —
  and packages them into a standalone "<journal>-fit" skill that guides you through the whole submission: TOPIC → WRITE → POLISH → SUBMIT.
  它学这本刊的选题口味、方向、写作风格、作者指南、aims & scope（能找到开放获取全文时连全文一起读），
  打包成一个独立的「<期刊>-fit」子技能，带你走完整投稿流程：选题 → 写作 → 润色 → 投稿（含 cover letter、title page）。
  Two ways in: (1) a named journal → distill it directly; (2) a vague need ("where should I submit this?") → recommend candidates first.
  Triggers / 触发词: "distill / decode journal X", "蒸馏 X 期刊", "学这本刊的选题/写作风格", "做个 X 期刊的 skill",
  "is this a fit for X?", "这篇适合投 X 吗", "按 X 风格改", "帮我写投 X 的 cover letter / title page", "我这个研究投哪本刊好", "更新 X 期刊的 skill".
---

# Imprimatur · 付梓

> *Imprimatur* — Latin, "let it be printed": the seal that says a work is fit to publish. This skill helps a manuscript earn it.
> 「付梓」即交付刊印。投稿不是把论文寄出去，而是让一本期刊在你的稿子里认出它自己。

## What this skill IS · 它的定位

**This is a journal-distillation skill.** It studies one journal deeply and packages what it learns into a standalone child skill, `<journal-slug>-fit`, that becomes your **submission companion** for that journal.

**这是一个「蒸馏期刊」的 skill。** 它把一本期刊吃透，打包成一个独立子技能 `<journal-slug>-fit`，成为你投这本刊的**投稿伴侣**。

### What it learns about the journal · 它学这本刊的什么（期刊档案 5 块）

1. **Aims & scope / 定位与范围** — the official positioning, and what it really means.
2. **Topic taste & direction / 选题口味与方向** — what topics it publishes, what's surging, what's saturated, what gaps it wants filled.
3. **Author guidelines & submission kit / 作者指南与投稿要素** — word/abstract limits, structured-or-not, highlights, **cover letter** expectations, **title page** elements, mandatory declarations (COI, CRediT, data, ethics, AI-use), reference style, submission system.
4. **Writing style & framework / 写作风格与框架** — from its published papers, and **from open-access full texts when available**: the section-by-section move structure, abstract recipe, title patterns, voice.
5. **The editorial decision model / 编辑决策模型** — the three stages a paper must clear (editor screen → peer review → acceptance shape) and the desk-reject red flags.

### What the generated skill does for you · 生成的子技能帮你做什么（四步流程）

The `<journal-slug>-fit` skill turns that profile into a four-step companion:

| Step / 步 | The child skill helps you… / 子技能帮你… |
|---|---|
| **1 · TOPIC / 选题** | Judge fit (**SUBMIT / RESHAPE / REDIRECT**) and shape your idea into an angle this journal actually wants. 判断适配，并把 idea 调成这本刊真正想要的角度。 |
| **2 · WRITE / 写作** | Draft each section on the journal's own framework — intro moves, methods layout, abstract recipe, title pattern. 按这本刊的框架起草各章节。 |
| **3 · POLISH / 润色** | Rewrite your draft toward the journal's house style; clear every desk-reject red flag. 把草稿改写成该刊风格，扫清 desk-reject 雷区。 |
| **4 · SUBMIT / 投稿** | Generate the submission kit: **cover letter, title page, highlights, declarations checklist** — all to this journal's guidelines. 生成投稿包：cover letter、title page、highlights、声明清单——全按该刊指南。 |

It is **tool-agnostic** — it runs on plain web access + PDF reading, so anyone can use it. Optional accelerators (Step 2) just speed it up. This matters because the skill is meant to be shared on GitHub.

本技能**不绑定任何工具**——靠普通联网 + 读 PDF 即可，任何人都能用。可选加速器只是提速。（因为这是要发到 GitHub 给大家用的。）

---

## How it works · 工作原理（两个核心想法）

### Idea 1 — Read three things, and compare them · 读三样东西并互相对照

A journal reveals itself three ways, and they often disagree. The gap between them is the gold.
一本期刊从三方面透露自己，三者常常对不上；落差就是金矿。

| Read / 读 | From / 来源 | Tells you / 看出 |
|---|---|---|
| **What it claims it wants** / 它声称想要什么 | Aims & Scope, **author guidelines** | the official pitch + the hard submission rules |
| **What it actually publishes** / 它实际登什么 | recent papers (+ **open-access full texts**) | the real topic taste *and* the writing framework |
| **What it rejects** / 它拒掉什么 | reviewer criteria, desk-reject signals, retractions | the hidden filter |

**The most useful find is the gap between what a journal claims and what it actually publishes** (e.g. it *says* it welcomes theory but publishes <2% → a theory-only paper risks rejection without review). Always compare claims against the real papers.
**最有价值的，是"声称"与"实际"的落差**（说欢迎理论，实际<2% → 纯理论稿大概率连送审都到不了）。永远拿真实论文对照声称。

### Idea 2 — A paper has to clear three stages · 一篇论文要闯三关

It's never accepted in one move: **Stage 1 the editor's first look → Stage 2 peer review → Stage 3 the writing style of accepted papers.** The four-step companion above maps onto these: TOPIC clears Stage 1, WRITE+POLISH clear Stages 2–3, SUBMIT packages what Stage 1 needs to even start.
论文不是一步录用：**第一关 编辑初筛 → 第二关 同行评审 → 第三关 录用论文的写法。** 上面的四步正对应：选题过第一关，写作+润色过第二三关，投稿备齐第一关启动所需的材料。

### The one rule that keeps it useful · 唯一铁律：改投测试

> **The rival-journal test / 改投测试**: keep a finding **only if it would change which of two similar journals you'd submit to.** Anything two neighboring journals want equally is a field-wide norm, not this journal's taste — drop it.
> 一条发现只有"会改变你在两本相似期刊之间该投哪本"时才保留。两本邻刊都一样想要的，是全领域规范、不是这本刊的口味——丢掉。

That's why you **pick one rival journal** to compare against (Step 1). Without it, the result degrades into generic writing advice.
所以 Step 1 **必须选一本对手刊**对照，否则结果会沦为泛泛的写作建议。

---

## Build workflow · 构建流程

Seven steps. Pause for the author's OK at the two ⏸ checkpoints.
七步。在两个 ⏸ 处停下让作者确认。

### Step 1 — Frame the build · 圈定范围
- **Exact journal / 确认是哪本刊** — full name + publisher + field (disambiguate look-alikes).
- **Rival journal / 对手刊** — one similar journal for the rival-journal test. If the author has none, pick the closest and say which.
- **Material on hand / 手头语料** — ask for PDFs of the journal's papers and/or the author's own draft/idea.
- **Depth / 深度** — quick (Stage 1 only) or full (all five profile parts + 4-step companion). Default: full.
- **New or update / 新建或更新** — scan `.claude/skills/*-fit/`.

Create the self-contained folder now (before research):
现在就建好自包含目录（调研之前）：

```
.claude/skills/<journal-slug>-fit/
├── SKILL.md                          # the child skill (the 4-step companion)
└── references/
    ├── evidence/
    │   ├── claims.md                 # aims & scope (what it says it wants)
    │   ├── published.md              # topic taste + direction (≥5 real papers)
    │   ├── rejected.md               # desk-reject signals + reviewer criteria
    │   ├── guidelines.md             # author guidelines → submission kit (cover letter, title page, declarations)
    │   ├── writing-framework.md      # section-by-section moves (from OA full texts when available)
    │   └── rival-<slug>.md           # how it differs from the rival
    └── corpus/                       # first-hand material (PDFs, guideline snapshots)
```

### Step 2 — Gather the evidence · 采集证据
Fill the `evidence/*.md` files. Parallelize with subagents if available; same process otherwise. **Every claim gets a source URL + a confidence tag (first-hand > second-hand > inferred).**

- **`claims.md`** → official Aims & Scope, editorials.
- **`published.md`** → analyze **≥5 real recent papers**: recurring topics, the contribution-type mix, hot vs saturated vs gap.
- **`rejected.md`** → reviewer/author guidelines, "reasons for rejection" editorials, retractions, author-forum reports.
- **`guidelines.md`** → the official **Guide for Authors**: word/abstract limits, structured-or-not abstract, highlights, graphical abstract, **what a cover letter should contain**, **what goes on the title page** (and, for anonymized review, what must be stripped from the manuscript), and every **mandatory declaration** (competing interest, CRediT, data availability, ethics, generative-AI-use). Organize it so each becomes a fill-in template.
- **`writing-framework.md`** → **find 2–3 open-access full texts** (try OpenAlex `is_oa`, Unpaywall, Europe PMC, repository copies) and reverse-engineer the **move structure** of each section (intro funnel, where RQs land, methods subsections, how results are reported, the discussion's fixed moves). If no OA full text exists, say so and infer style from abstracts only.

Then a **rival comparison**: for 2–3 topics, "how would *this* journal handle it vs the rival?" Tag anything identical as `field-wide`.

**Optional accelerators**（never required）: `$ARIS_REPO/tools/openalex_fetch.py`, `semantic_scholar_fetch.py`, a `pdf`/`phd-deepread` skill. Otherwise plain web + reading works.

> ⏸ **Checkpoint 1 — Evidence review.** One-screen summary: source counts per file, top topics, the sharpest claims-vs-reality gaps, the submission-kit highlights (cover letter? separate title page? key declarations), whether OA full text was found, and the rival contrast.

### Step 3 — Name the claims-vs-reality gaps · 点出"声称 vs 实际"的落差
List every place the journal's claims diverge from what it publishes. Each gap becomes a desk-reject risk or an exploitable hidden preference.

### Step 4 — Build the journal profile · 合成期刊档案
Read `references/signal-mining.md` (how to keep real findings, drop noise; how to turn full texts into a writing framework and guidelines into a submission kit). Then write the profile, organized so it can drive all four steps. Run the rival-journal test on every finding; drop `field-wide` ones. Keep 3–7 sharp Stage-1 findings.

> ⏸ **Checkpoint 2 — Profile review.** Show the Stage-1 findings (with evidence), the "this journal vs rival" one-liner, the gaps, the writing-framework skeleton, and the submission-kit checklist.

### Step 5 — Calibrate against held-out papers · 用留出论文校准
- **Hit test** — 2 real papers this journal published (held out) → must score **SUBMIT**.
- **Redirect test** — 1 rival-journal/off-topic paper → must score **REDIRECT** with a correct reason.
Both must pass before shipping. Use an independent checker (subagent) if available.

### Step 6 — Ship the `<journal-slug>-fit` skill · 生成子技能
Read `references/fit-skill-template.md` and fill it. The child skill **must** deliver all four steps (TOPIC fit verdict; WRITE framework; POLISH playbook; SUBMIT kit with cover-letter + title-page generators), the desk-reject red-flag list, the rival note, and an honesty section (sample size + research date).

### Step 7 (optional) — Polish & sanity-check triggers · 打磨与触发检查
Do the description triggers cover all four steps (fit, write, polish, cover letter)? Is each step executable as written?

---

## Two entry points · 两个入口

**Named journal** → Step 1.

**Vague need** ("I work on GenAI + learning analytics, where should I submit?") → recommend **2–3 contrasting candidates** first:
```
### Candidate: [Journal full name]   ⚡has a -fit skill / 🆕 needs distilling
Position / 定位: [what it publishes, for whom]
Why it fits you / 为何适合: [topic + method + manuscript stage]
Bar & risk / 门槛与风险: [acceptance difficulty, review speed, likely desk-reject traps]
vs the others / 与其他的差别: [the distinguishing trade-off]
```
Scan `.claude/skills/*-fit/` first — an already-distilled journal is plug-and-play.

---

## The child skill's contract · 子技能必须满足的契约

`<journal-slug>-fit/SKILL.md` must, on its own, support all four steps:
1. **TOPIC** — take an idea/abstract → **SUBMIT / RESHAPE / REDIRECT** with per-stage reasons, and propose journal-fitting angles.
2. **WRITE** — give the journal's section-by-section skeleton + abstract recipe + title patterns, each anchored to a *real* example.
3. **POLISH** — before→after edits on the author's own text toward the house style; clear every red flag; hit the word/format limits.
4. **SUBMIT** — generate a **cover letter** (to the journal's expected content), a **title page** (exactly the required elements, respecting anonymized-review rules), highlights/structured abstract, and a **declarations checklist** so nothing triggers a desk reject.
Plus: honest limits (published taste, not the editor's private bar; fit raises odds ≠ guarantees acceptance; sample size + date).

See `references/fit-skill-template.md` for the exact skeleton.

---

## Updating an existing decoder · 更新已有解码器
1. Read the existing `SKILL.md`; find the research date; note staleness.
2. Re-collect only the moving parts: latest papers, any guideline/scope changes, editorial-board changes.
3. Reconcile: reinforce, mark-and-update, or add a finding.
4. Update the "recent shifts" note + research date. Incremental, not a rewrite.

---

## Honesty rules · 诚实守则
- **Never fabricate** acceptance rates, review times, guideline details, or preferences the evidence doesn't show.
- **Never dress up field-wide norms** as this journal's special taste.
- **Always surface the claims-vs-reality gap** rather than parroting the Aims & Scope.
- **Prefer an honest 60-point decoder** with stated gaps over a polished 90-point one that invents taste.
- **Never promise acceptance.** Fit raises the probability; it isn't a verdict the journal is bound by.
- **The submission kit is a draft to verify**, not a substitute for reading the live Guide for Authors before you submit.

---

## Special cases · 特殊场景
- **Broad/megajournal vs niche** — for wide-scope venues, Stage-1 topic signals are weak; weight contribution magnitude + writing framework instead.
- **Conference vs journal** — add deadline cadence, page limits, rebuttal culture; SUBMIT step adapts (e.g. no cover letter, but a checklist).
- **Non-English journals** — use the right indexes (e.g. CNKI) and submission rules; note stricter national style requirements.
- **New / low-output journal** — if <5 readable papers, say so, cap findings at 2–3 "limited sample", lean on author-supplied PDFs.
- **No open-access full text** — build the writing framework from abstracts + any author preprints; mark it "style inferred, full text not sampled".
- **Test the author's own draft** — if supplied, run all four steps on it as a bonus deliverable.

---

## Credits · 署名
When shipping a child skill, footer it with:
`> Generated by Imprimatur · researched [date] · sample [N] papers · https://github.com/Youn-17/imprimatur`

---

> A good decoder doesn't tell you how to please a journal. It shows you, before you submit, where "what you want to say" and "what they want to publish" actually overlap — and hands you the cover letter to prove it.
> 一个好的解码器不教你讨好期刊。它在你投稿前让你看清「你想说的」和「它想登的」的真实交集——还顺手把 cover letter 给你写好。
