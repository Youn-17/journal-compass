---
name: journal-decoder
description: |
  Distill a journal into a reusable skill — the way a person-distiller captures a thinker, this captures a journal.
  蒸馏一本期刊：像蒸馏一个人那样，把一本期刊蒸馏成一个可复用的 skill。
  From the journal's own papers + public info, it learns that journal's TOPIC TASTE (选题口味) and WRITING STYLE (写作风格),
  and packages them into a standalone "<journal>-fit" skill.
  从该刊的论文与公开信息里，学出这本刊的【选题口味】和【写作风格】，打包成一个独立的「<期刊>-fit」子技能。
  Once distilled, that skill can judge whether a topic/abstract fits and rewrite a draft into the journal's style.
  蒸馏之后，这个子技能可用来判断选题适不适合投、把稿子改写成该刊风格。
  Two ways in: (1) a named journal → distill it directly; (2) a vague need ("where should I submit this?") → recommend candidates first.
  Triggers / 触发词: "distill journal X", "decode journal X", "学这本刊的选题/写作风格", "蒸馏 X 期刊", "做个 X 期刊的 skill",
  "is this a fit for X?", "这篇适合投 X 吗", "按 X 期刊风格改", "我这个研究投哪本刊好", "更新 X 期刊的 skill".
---

# Journal Decoder · 期刊解码器

> Submitting isn't mailing a paper out — it's making a journal recognize itself in your work.
> 投稿不是把论文寄出去，是让一本期刊在你的稿子里认出它自己。

## What this skill IS · 它的定位

**This is a journal-distillation skill.** Its one job is to **distill a journal** — to learn, from that journal's own papers and public information, the two things that define it:

**这是一个「蒸馏期刊」的 skill。** 它只做一件事：**蒸馏一本期刊**——从这本刊自己的论文和公开信息里，学出定义这本刊的两样东西：

1. **Topic taste / 选题口味** — what this journal chooses to publish and what it turns away. 这本刊愿意登什么、把什么挡在门外。
2. **Writing style / 写作风格** — how its accepted papers are actually written (abstract, title, structure, framing, voice). 它录用的论文实际怎么写。

The distilled result is packaged as a standalone, reusable child skill named `<journal-slug>-fit`. **Once a journal is distilled, that skill can be used** to (a) judge whether a topic/abstract/idea fits the journal, and (b) rewrite a draft into the journal's style. These are *uses* of the distilled journal — the skill's identity is the distillation itself.

蒸馏结果打包成一个独立、可复用的子技能 `<journal-slug>-fit`。**蒸馏完成后，这个子技能可用来**：(a) 判断某选题/摘要/idea 适不适合这本刊；(b) 把草稿改写成该刊风格。这些是"蒸馏出来之后的用途"——本 skill 的身份是**蒸馏本身**。

It is **tool-agnostic** — distillation runs on plain web access + PDF reading, so anyone can use it. Optional accelerators (see Step 2) speed it up but are never required. This matters because the skill is meant to be shared on GitHub.

本技能**不绑定任何特定工具**——蒸馏靠普通联网 + 读 PDF 即可跑通，任何人都能用。可选加速器只是锦上添花、绝非必需（因为这是要发到 GitHub 给大家用的）。

---

## How it works · 工作原理（两个核心想法）

Before building, internalize these two ideas — they're what makes a distillation useful instead of generic.
动手前先吃透这两个想法——它们决定了蒸馏出来的是真有用的东西，还是一堆放之四海皆准的废话。

### Idea 1 — Read three things about the journal · 读懂一本期刊的三样东西

A journal tells you about itself in three ways, and they often disagree. Read all three and compare them:
一本期刊会从三个方面透露自己，而这三者常常对不上。三样都读，并互相对照：

| What to read / 读什么 | Where / 在哪看 | What it tells you / 能看出什么 |
|---|---|---|
| **What it *claims* it wants / 它声称想要什么** | Aims & Scope, author guidelines, editorials | The official pitch. It's marketing — trust it least. 官方说辞，营销话术，最不可信。 |
| **What it *actually publishes* / 它实际登什么** | Papers from the last 2–3 years | The real answer. This is the ground truth. 真实答案，以此为准。 |
| **What it *rejects* / 它拒掉什么** | Reviewer/author guidelines, "reasons for rejection" editorials, retractions, author-forum reports | The hidden filter — what quietly gets a paper killed. 隐藏的过滤器：什么会让稿子悄悄被毙。 |

**The single most useful thing you can find is the gap between what a journal *claims* and what it *actually publishes*.** When a journal says "we welcome theoretical contributions" but every well-cited paper in three years is empirical, that gap is the insight — a theory-only paper is at high risk of being rejected without review. Always compare the claims against the real papers, and write down every gap you find.

**你能挖到的最有价值的东西，就是"它声称的"和"它实际登的"之间的落差。** 当期刊说"欢迎理论贡献"，但近三年被引高的全是实证研究，这个落差本身就是洞察——一篇纯理论稿很可能连送审都到不了就被退。永远拿真实论文去对照它的声称，把每一处落差都记下来。

### Idea 2 — A paper has to clear three stages · 一篇论文要闯三关

A paper doesn't get "accepted" in one move — it has to survive three stages in order, and "fit" means something different at each. Rebuild all three:
论文不是一步"被录用"，而是要按顺序闯过三关，每一关判"合不合适"的标准都不同。三关都要还原出来：

- **Stage 1 — The editor's first look / 第一关：编辑初筛**: the ~30-second decision an editor makes *before* sending it out for review. Most rejections happen right here. → Is the topic in scope? Is it the kind of contribution they publish? Any obvious dealbreaker?
- **Stage 2 — Peer review / 第二关：同行评审**: what reviewers in this community insist on. → The methods/rigor bar, how a contribution must be argued, the novelty standard.
- **Stage 3 — How accepted papers read / 第三关：录用论文怎么写**: what published papers actually look like once they're in. → Abstract recipe, title patterns, structure, length, citation habits.

The child skill maps "fit" onto these three stages, so the author learns **which stage** their paper would fail at — not just *whether* it fits.
子技能把"合不合适"对应到这三关，让作者知道稿子会**在哪一关**挂掉，而不只是"行不行"。

---

## The one rule that keeps it useful · 让它有用的唯一铁律：改投测试

Most "journal writing norms" are true of the whole field (use IMRaD, state your limitations, cite recent work). Writing those down is useless — they give the author no specific guidance. A finding earns a place in the profile **only if it passes this test**:

大多数"期刊写作规范"对整个领域都成立（用 IMRaD、写局限、引近作）。把这些写进去毫无用处——对作者没有任何具体指导。一条发现只有**通过下面这个测试**才配写进档案：

> **The rival-journal test / 改投测试**: Would knowing this change which of two similar journals you'd send the paper to? If two neighboring journals in the same field would both want it equally, it's a field-wide norm, not this journal's taste — drop it.
> 知道这件事，会改变你"在两本相似期刊之间该投哪本"的决定吗？如果同领域的两本邻刊都一样想要它，那它就是全领域通用规范、不是这本刊的口味——丢掉。

This is why **you must pick one rival journal to compare against** in Step 1. Without a rival to compare to, you can't tell this journal's house style from the whole field's norms, and the result degrades into generic writing advice.

所以 Step 1 **必须选一本对手刊来对照**。没有对照对象，你就分不清"这本刊的家风"和"全领域通用规范"，做出来的东西会沦为泛泛的写作建议。

---

## Build workflow · 构建流程

Seven steps. Pause for the author's OK at the two ⏸ checkpoints — catching a mistake there is far cheaper than after a full profile is written.
七步。在两个 ⏸ 处停下来让作者确认——在这里拦错，比写完整份档案再返工便宜得多。

### Step 1 — Frame the build · 圈定范围

If a journal is named, confirm it; if the need is vague, recommend candidates first (see "Two entry points"). Then lock down:
若已给期刊名，确认；若需求模糊，先推荐候选（见"两个入口"）。然后锁定：

- **Exact journal / 确认是哪本刊** — full name + publisher + field (disambiguate look-alikes, e.g. *Computers & Education* vs *Computers & Education: Artificial Intelligence*).
- **Rival journal / 对手刊** — one similar journal to compare against, for the rival-journal test. Ask the author; if they have none in mind, pick the closest competitor yourself and say which.
- **Material on hand / 手头语料** — "Do you have PDFs of this journal's papers, especially recent or 'typical' ones? And/or your own draft/idea I should test against it?" First-hand papers beat anything scraped.
- **Depth / 深度** — quick (Stage 1 editor-screen only) or full (all three stages). Default: full.
- **New or update / 新建或更新** — scan `.claude/skills/*-fit/`; if one exists, switch to "Updating an existing decoder".

Create the self-contained folder now (before research), so the skill is portable — sharing it is just copying the folder:
现在就建好自包含目录（调研之前），保证可移植——分享时复制整个文件夹即可：

```
.claude/skills/<journal-slug>-fit/
├── SKILL.md                      # the child skill (final product)
└── references/
    ├── evidence/                 # raw research, one file per question
    │   ├── claims.md             # what it claims it wants (aims & scope, guidelines)
    │   ├── published.md          # what it actually publishes (≥5 real papers)
    │   └── rejected.md           # what it rejects (reviewer criteria, desk-reject signals)
    └── corpus/                   # first-hand material (PDFs, TOC exports, guideline snapshots)
```

### Step 2 — Gather the evidence · 采集证据

Fill the three `evidence/*.md` files — one per question from Idea 1. If you have subagents, research the three in parallel; if not, do them in sequence — same process. **Every claim gets a source URL and a confidence tag (first-hand > second-hand > inferred).**

把三个 `evidence/*.md` 填上——对应 Idea 1 的三个问题。有 subagent 就并行，没有就顺序做——流程一样。**每条都标来源 URL 和可信度（一手 > 二手 > 推断）。**

- **`claims.md`** → official Aims & Scope, author guidelines, recent editorials. Save snapshots to `corpus/`.
- **`published.md`** → analyze **≥5 real recent papers** (full text, not just titles): which topics recur, the contribution-type mix (empirical / theory / method / review / design), and how they're written. This is the heart — don't skimp.
- **`rejected.md`** → reviewer/author guidelines, "reasons for rejection" editorials, retraction notices, author-forum reports. What gets a submission killed here?

Then do a **rival comparison**: for 2–3 recurring topics, ask "how would *this* journal handle it vs the rival?" Tag anything identical across both as `field-wide`, to filter out later.

再做一遍**对手刊对照**：挑 2–3 个高频主题，问"本刊会怎么处理 vs 对手刊会怎么处理？"两边一样的标 `field-wide`，后面过滤掉。

**Optional accelerators / 可选加速器**（never required / 绝非必需）: if `$ARIS_REPO/tools/openalex_fetch.py` or `semantic_scholar_fetch.py` exist, use them to pull recent + high-cited papers and the citation network fast; if a `pdf`/`phd-deepread` skill is installed, use it to read supplied PDFs. Otherwise plain web search + reading works fine.

> ⏸ **Checkpoint 1 — Evidence review.** Show the author a one-screen summary: source counts per file, the top recurring topics, the sharpest claims-vs-reality gaps, and the rival comparison. Bad evidence → bad decoder, so confirm quality here before synthesizing. 把证据摘要给作者过目再继续。

### Step 3 — Name the claims-vs-reality gaps · 点出"声称 vs 实际"的落差

List every place the journal's claims diverge from what it actually publishes. Each gap becomes either a desk-reject risk (Stage 1) or a hidden preference the author can exploit. Keep this list — the most useful parts of the final verdict come from it.
列出所有"声称 vs 实际"的分歧。每个落差要么是编辑初筛会拒的风险（第一关），要么是作者可利用的隐藏偏好。留好这张清单，裁决里最有用的部分都来自它。

### Step 4 — Build the journal profile · 合成期刊档案

Read `references/signal-mining.md` for how to separate real findings from noise, then write the **journal profile**, organized by the three stages. Run the rival-journal test on every candidate finding; drop the `field-wide` ones.

读 `references/signal-mining.md` 学如何区分真发现与噪声，然后按三关写出**期刊档案**。对每条候选发现跑改投测试；`field-wide` 的丢掉。

- **Stage 1 profile** — scope boundaries, accepted contribution types + mix, and the desk-reject red-flag list (from `rejected.md` + the gaps).
- **Stage 2 profile** — the methods/rigor bar, how a contribution must be framed to satisfy this community, the novelty standard.
- **Stage 3 profile** — abstract recipe (length + sentence-by-sentence functions), title patterns (with ≥1 real example), section template, length range, citation density/recency/self-cite habits.

Keep 3–7 sharp Stage-1 findings, max. Three that pass the rival-journal test beat ten that don't.
第一关的核心信号控制在 3–7 条。三条过了改投测试的，胜过十条没过的。

> ⏸ **Checkpoint 2 — Profile review.** Show: the Stage-1 findings (with evidence), the one-line "this journal vs the rival" difference, the claims-vs-reality gaps, and the writing-style summary. Synthesis is the most judgment-heavy step; confirm direction before writing ~400 lines. 合成是主观判断最重的一步，确认方向再开写。

### Step 5 — Calibrate against held-out papers · 用留出论文校准

Validate with an independent check (spawn a subagent if available, to avoid grading your own work):
用独立检查做校准（有 subagent 就开一个，避免自评偏差）：

- **Hit test / 命中测试** — take 2 real papers *this* journal published (held out from the ones you read in Step 2) and run them through the draft fit logic. Expected: **SUBMIT**. If they don't pass, the Stage-1 findings are wrong → back to Step 4.
- **Redirect test / 改投测试** — take 1 paper from the rival journal (or a clearly off-topic one). Expected: **REDIRECT**, with a correct reason. If it scores SUBMIT, the findings are too broad — they have no discriminating power.

Both must pass before shipping. A decoder that says SUBMIT to everything is worse than none.
两个都过才能交付。对什么都说 SUBMIT 的解码器比没有还糟。

### Step 6 — Ship the `<journal-slug>-fit` skill · 生成子技能

Read `references/fit-skill-template.md` and fill it from the profile. The child skill **must** contain: the fit-verdict protocol (three stages → SUBMIT/RESHAPE/REDIRECT), the reframe playbook (per-stage concrete edits with real examples), the desk-reject red-flag list, the rival-journal note, and an honesty section with sample size + research date. Write it to `<journal-slug>-fit/SKILL.md`.

读 `references/fit-skill-template.md`，用档案填充。子技能**必须**包含：裁决协议（三关 → SUBMIT/RESHAPE/REDIRECT）、重构剧本（逐关的具体改法 + 真实范例）、编辑初筛红旗清单、对手刊备注、含样本量与调研日期的诚实声明。

### Step 7 (optional) — Polish & sanity-check triggers · 打磨与触发检查

If the author wants, do a quick pass: do the description triggers cover how people really ask ("is X a fit?", "投 X 行不行", "reframe for X")? Is the verdict protocol executable as written? Tighten anything vague.

---

## Two entry points · 两个入口

**Named journal / 已给期刊名** → straight into Step 1.

**Vague need / 模糊需求** ("I work on GenAI + learning analytics, where should I submit?") → recommend **2–3 contrasting candidates** before building. For each:
```
### Candidate: [Journal full name]   ⚡has a -fit skill / 🆕 needs decoding
Position / 定位: [one line — what it publishes, for whom]
Why it fits you / 为何适合: [matches your topic + method + manuscript stage]
Bar & risk / 门槛与风险: [acceptance difficulty, review speed, likely desk-reject traps]
vs the others / 与其他候选的差别: [the distinguishing trade-off]
```
Scan `.claude/skills/*-fit/` first — an already-distilled journal is plug-and-play. The author picks one → confirm details → Step 1.

---

## The child skill's contract · 子技能必须满足的契约

When you write `<journal-slug>-fit/SKILL.md`, it must be able to, on its own:
1. Take a manuscript / abstract / idea and return **SUBMIT / RESHAPE / REDIRECT** with per-stage reasoning.
2. Tell the author **which stage** they'd fail at and **what specific change** clears it.
3. Provide a **fill-in abstract template + title patterns + structure**, each anchored to a *real* example from the journal (not generic advice).
4. State its limits honestly: it reflects *published* taste, not the editor's private bar; high fit raises the odds, never guarantees acceptance; it carries a sample size and a research date.

See `references/fit-skill-template.md` for the exact skeleton.

---

## Updating an existing decoder · 更新已有解码器

When the author says a journal changed (new editor, scope shift, "decode X again"):
1. Read the existing `SKILL.md`; find the research date in its honesty section; note how stale it is.
2. Re-collect only the moving parts: the latest year of published papers (new issues/special issues) + any new claims (editorials/guideline changes) + editorial-board changes.
3. Reconcile: a new trend reinforces a finding → add evidence; contradicts it → mark the shift and update; a brand-new hot area appears → add a finding.
4. Update the "recent shifts" note + research date. Incremental, not a rewrite.

---

## Honesty rules · 诚实守则

These protect both the author and the skill's credibility on GitHub:
保护作者，也保护这个开源项目的可信度：

- **Never fabricate** acceptance rates, review times, or preferences the evidence doesn't show. 绝不编造录用率/周期/偏好。
- **Never dress up field-wide norms** as this journal's special taste. 不把全领域规范包装成本刊独有口味。
- **Always surface the claims-vs-reality gap** rather than parroting the Aims & Scope. 永远点出"声称 vs 实际"的落差，而不是复读官网。
- **Prefer an honest 60-point decoder** with stated gaps over a polished 90-point one that invents the journal's taste. 宁要诚实标注局限的 60 分，也不要编造口味的"完美"90 分。
- **Never promise acceptance.** Fit raises the probability; it isn't a verdict the journal is bound by. 永不承诺录用。

---

## Special cases · 特殊场景

- **Broad/megajournal vs niche / 综合大刊 vs 专刊** — for wide-scope venues (*Nature Communications*, *PNAS*), Stage-1 scope signals are weak; shift weight to Stage 2 (contribution magnitude, novelty framing, "broad significance") and Stage 3. Fit becomes "is it big enough?" not "is it on-topic?".
- **Conference vs journal / 会议 vs 期刊** — add a deadline-cadence + page-limit + rebuttal-culture note; some venues use explicit scoring (e.g. soundness/excitement). Stage 3 rewards "one-sentence contribution" clarity.
- **Non-English / 非英文期刊** — use the appropriate indexes (e.g. CNKI for Chinese journals) and submission rules; exclude self-media commentary; note that some national core-journal style requirements are stricter than international ones.
- **New / low-output journal / 新刊或冷门刊** — if fewer than ~5 readable papers exist, say so up front, cap Stage-1 findings at 2–3 marked "limited sample", and lean on author-supplied PDFs.
- **Test the author's own draft / 顺带测稿** — if the author supplied a draft/idea, run the finished fit protocol on it as a bonus deliverable.

---

## Credits · 署名

When shipping a child skill, footer it with:
`> Generated by journal-decoder · researched [date] · sample [N] papers · https://github.com/Youn-17/journal-decoder`

---

> A good decoder doesn't tell you how to please a journal. It shows you, before you submit, where "what you want to say" and "what they want to publish" actually overlap.
> 一个好的解码器不教你讨好期刊。它在你投稿前让你看清：「你想说的」和「它想登的」，真实的交集在哪里。
