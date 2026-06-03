# Child-skill template · 子技能模板

Step 6 fills this in to produce `<journal-slug>-fit/SKILL.md` — a four-step submission companion. Placeholders are `[...]`. Keep it bilingual. **Anchor every claim to a real example** (a real title, a real abstract excerpt, a real guideline line) — generic advice is the failure mode this template exists to prevent.

Step 6 用它生成 `<journal-slug>-fit/SKILL.md`——一个四步投稿伴侣。占位符 `[...]`。**每条都要锚定真实范例**（真实标题、真实摘要片段、真实指南条款）。

---

```markdown
---
name: [journal-slug]-fit
description: |
  Submission companion for [Journal full name], distilled from [N] papers + official guidance (researched [date]); rival: [rival].
  Four steps: TOPIC (SUBMIT/RESHAPE/REDIRECT fit) → WRITE (the journal's section framework) → POLISH (house style) → SUBMIT (cover letter, title page, declarations).
  [期刊全名] 的投稿伴侣，蒸馏自 [N] 篇论文 + 官方指南。四步：选题 fit → 写作框架 → 风格润色 → 投稿包（cover letter / title page / 声明）。
  Use when the user asks "is this a fit for [Journal]", "投 [Journal] 行不行", "按 [Journal] 风格写/改", "帮我写投 [Journal] 的 cover letter / title page", "[Journal] desk reject risk", or pastes an abstract/draft aimed at [Journal].
---

# [Journal full name] — Submission Companion · 投稿伴侣

> [One line capturing this journal's editorial identity, from an editorial or its most-cited work.]
> First activation only: "Built from published papers + public guidance up to [date]. Reflects published taste, not the editor's private bar. Fit raises the odds — it never guarantees acceptance. Always check the live Guide for Authors before submitting."

## How this journal decides · 它怎么做决定（三关）
- **Stage 1 — editor's first look / 第一关 编辑初筛**: scope = [...]; contribution types it accepts = [...]; desk-reject red flags (each an auto-block) = [≥3, from `rejected.md` or a claims-vs-reality gap].
- **Stage 2 — peer review / 第二关 同行评审**: method/rigor bar = [...]; how a contribution must be framed = [...]; novelty standard = [...].
- **Stage 3 — how accepted papers read / 第三关 录用论文的写法**: see the WRITE framework below.

---

## STEP 1 · TOPIC — is it a fit, and what angle? · 选题
**Verdict protocol**: walk the three stages, score each PASS/WEAK/FAIL with one line of evidence; any Stage-1 red flag → auto-block. Return:
- **SUBMIT** — clears all three stages.
- **RESHAPE** — right journal, wrong framing → name the failing stage(s) + the exact fix.
- **REDIRECT** — won't fit even reshaped → name the better venue (often [rival]).
**Angle finder**: given a rough idea, propose 2–3 framings that match this journal's topic taste + fill a gap it wants. This journal's gaps right now: [...]. Its saturated zones (avoid): [...].

## STEP 2 · WRITE — draft on the journal's framework · 写作
The section-by-section move structure of accepted papers here (from `writing-framework.md`):
- **Title** — pattern: [...]. Real example: > [real title].
- **Abstract** — [structured? word cap]; sentence sequence: 1)[fn] 2)[fn] 3)[fn] 4)[fn] 5)[fn]. Real example: > [real abstract excerpt].
- **Highlights / 要点**: [count, char limit].
- **Introduction** — moves: [e.g. importance → narrow to tech → gap → "therefore we…" → contribution]. Where the RQs land: [...].
- **[Framework / Lit review]** — [own section? one subsection per construct?].
- **Methods** — subsections: [participants/context → design → measures → analysis], expected detail: [...].
- **Results** — organized by [RQ/hypothesis]; reporting style: [...]; tables/figures: [...].
- **Discussion** — fixed moves: [restate → interpret vs theory → implications → limitations+future].
- **Length / structure / references**: [word range; section numbering; reference style].

## STEP 3 · POLISH — toward the house style · 润色
For a draft or paragraph, do a **before → after** on the author's own text:
- Flag any sentence that doesn't match the framework/voice above and rewrite it.
- Enforce the limits ([word cap], [abstract cap]); fix the abstract to the recipe; retitle to a pattern.
- Run the desk-reject red-flag checklist and fix any hit.

## STEP 4 · SUBMIT — generate the submission kit · 投稿包
From `guidelines.md`. Generate, ready to verify against the live guide:
- **Cover letter / 投稿信** — skeleton this journal expects: [e.g. aim + main finding (significance) → fit to scope → novelty/broad implication → originality & no concurrent submission → close]. Exclude: [what must NOT go in it, e.g. declarations/reviewers if entered in-system].
- **Title page / 题名页** — exactly the required elements: [title; authors; affiliations+country; corresponding author contact; ORCID; funding; acknowledgements; CRediT]. For anonymized review, also list **what to strip from the manuscript**: [author names, acknowledgements, funding, self-citations → third person].
- **Highlights / structured abstract / graphical abstract** — to spec: [...].
- **Declarations checklist / 声明清单** — [Competing Interest; CRediT; Data Availability; Ethics/consent; Funding; Generative-AI-use]. Flag any that are mandatory so an omission can't trigger a desk reject.

---

## vs [rival journal] · 与对手刊的区别
Submit here rather than [rival] when: [distinguishing preference]. If the work leans toward [X], [rival] is the better home.

## Limits · 边界
- Reflects *published* taste up to [date]; can't see the editor's latest unindexed turn.
- Fit ≠ acceptance. The submission kit is a draft to verify against the live Guide for Authors.
- Built from public papers + guidance, not internal standards. Sample: [N] papers; rival: [rival].

## Evidence · 证据来源
`references/evidence/` — `claims.md` (says) · `published.md` (publishes) · `rejected.md` (rejects) · `guidelines.md` (submission kit) · `writing-framework.md` (section moves) · `rival-[slug].md` (contrast).

---

> Generated by Imprimatur · researched [date] · sample [N] papers · [your-repo-url]
```
