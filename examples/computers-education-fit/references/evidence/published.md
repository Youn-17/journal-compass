# Computers & Education (C&E) — The "DO" Evidence Stream

**What the journal ACTUALLY publishes (ground truth from real papers), vs. its official claims.**

- Journal: *Computers & Education* (Elsevier), ISSN 0360-1315
- OpenAlex source: `S4210172634` (works_count ≈ 6,148; cited_by ≈ 528,983)
- Evidence base: 250 most-recent C&E `type:article` papers (publication_date ≥ 2023-01-01; in practice 2024–2026, dominated by 2025 n=175 and 2026 n=66) + 60 most-cited 2023–2026 articles, pulled live from OpenAlex API on 2026-06-01.
- Method note: topic tags use OpenAlex `primary_topic` + title/concept keyword matching; contribution-type mix is a heuristic classifier on reconstructed abstracts. ~57% of the *very newest* records had no abstract yet in OpenAlex (in-press 2026), so contribution-type percentages are computed on the abstract-bearing subset (n=89 recent + n=27 top-cited).
- **Convention:** [OBSERVED] = directly counted from the corpus; [INFERRED] = my interpretation. Confidence: High / Med / Low.

Source URLs:
- OpenAlex source record: https://api.openalex.org/sources/issn:0360-1315
- OpenAlex works query (recent): https://api.openalex.org/works?filter=primary_location.source.id:S4210172634,from_publication_date:2023-01-01,type:article&sort=publication_date:desc
- OpenAlex works query (top-cited): https://api.openalex.org/works?filter=primary_location.source.id:S4210172634,from_publication_date:2023-01-01,type:article&sort=cited_by_count:desc
- Official journal home: https://www.sciencedirect.com/journal/computers-and-education
- Elsevier journal page: https://www.journals.elsevier.com/computers-and-education

---

## 1. Recurring topics (ranked by prominence)

[OBSERVED] Frequency in the recent corpus (n=250). Keyword/concept hits; categories overlap, so percentages sum to >100%. **Confidence: High** (counts) / **Med** (category boundaries).

| Rank | Topic cluster | Share of recent papers |
|---|---|---|
| 1 | **AI / ML in education** (intelligent tutoring, adaptive learning, AI literacy, "AI assistance") — the umbrella theme | ~50% |
| 2 | **Online / blended / distance / flipped learning** (incl. MOOCs, remote) | ~30% |
| 3 | **Self-regulated learning, motivation, engagement, self-efficacy** (outcome/process constructs) | ~20% |
| 4 | **Generative AI / ChatGPT / LLMs** (subset of #1, but the fastest-rising) | ~16% by keyword; ~17% by title in 2025–26 |
| 5 | **Computational thinking / programming / CS education** | ~16% |
| 6 | **Teachers: TPACK, digital competence, professional development, pre-service** | ~16% |
| 7 | **Feedback & assessment** (incl. automated/AI feedback, peer feedback) | ~14% |
| 8 | **Collaborative learning / CSCL / peer learning** | ~13% |
| 9 | **Game-based learning & gamification** | ~11% |
| 10 | **VR / AR / immersive / metaverse** | ~11% |
| 11 | **Digital / AI / information literacy & competence** | ~9% |
| 12 | **Learning analytics / EDM** (log/clickstream/dashboards) | ~7% |
| 13 | **Chatbots / conversational & pedagogical agents** | ~5% |
| 14 | **Mobile learning** | ~3% |

[OBSERVED] OpenAlex `primary_topic` top labels (recent set) corroborate: "Innovative Teaching and Learning Methods" (28), "Online Learning and Analytics" (20), "Virtual Reality Applications and Impacts" (12), "Educational Games and Gamification" (10), "Teaching and Learning Programming" (9), "Digital literacy in education" (9), "Online and Blended Learning" (9), "Intelligent Tutoring Systems and Adaptive Learning" (8), "Ethics and Social Impacts of AI" (7), "Gender and Technology in Education" (7). **Confidence: High.**

[INFERRED] The recurring substrate is **technology-as-intervention measured against a learning outcome or learning process** — almost every topic is framed around "does this digital tool/condition change learning, engagement, or competence?" rather than the technology itself. **Confidence: High.**

---

## 2. Hot zone vs. saturated zone vs. gaps

**HOT / SURGING** [OBSERVED + INFERRED, Med-High]
- **Generative AI in education** is the dominant surge. GenAI appears in ~17% of 2025–2026 *titles* (vs ~11% in the small 2024 slice), and 4 of the top-6 most-cited 2023–26 papers are GenAI/chatbot studies. Recent 2026 titles show the frontier moving from "does ChatGPT help?" to **mechanism and second-order effects**: cognitive load of AI explanation styles, AI's effect on critical thinking / reliance / over-reliance behaviors, metacognitive reasoning in LLMs, GenAI as a "double-edged sword" for creativity, equity ("Bridge or widen gaps"), and teacher/parent *intention to use*. [OBSERVED titles]
- **AI feedback & AI literacy / competence** (incl. teacher digital competence, AI literacy interventions) are rising alongside GenAI.
- **Equity, ethics, agency, and over-reliance** framings around AI ("Ethics and Social Impacts of AI" is a top-7 primary topic; #1 cited paper is "Impact of AI assistance on student agency").

**SATURATED / CROWDED** [INFERRED, Med]
- Generic **"ChatGPT improves X" experimental studies** and **technology-acceptance / intention-to-use (TAM/UTAUT)** survey papers — extremely common; bar for novelty/contribution is now high.
- **Gamification and VR/AR "increases engagement/learning" comparison studies** remain steady but are a mature, crowded space (still publishable when tied to mechanism or strong design).
- **Online/blended learning** generally — large, mature volume; needs a sharp angle.

**GAPS / EDITOR-WANTED-BUT-RARE** [OBSERVED + INFERRED, Med]
- **Theory / conceptual** and **pure methods** contributions are nearly absent in the corpus (<2% combined) — the journal's official scope says it "extends theory and practice," but in practice almost everything is empirical. A well-grounded conceptual framework with broad relevance is rare and therefore distinctive.
- **Large-scale / longitudinal** designs are under-represented relative to single-shot experiments (longitudinal engagement-achievement work does appear among top-cited, signaling editor appetite).
- **Rigorous systematic reviews / meta-analyses** are explicitly welcomed by the editors but make up only ~7–10% of output — a relatively open lane *if* methodologically strong (PRISMA, clear RQs, analysis framework).
- **Negative / "double-edged" / equity-gap findings** about AI are emerging but still scarce vs. the flood of positive-effect studies.

---

## 3. Contribution-type mix

[OBSERVED] On abstract-bearing recent papers (n=89) and top-cited 2023–26 (n=27). **Confidence: High for "overwhelmingly empirical"; Med for fine sub-splits** (heuristic classifier).

| Contribution type | Recent (n=89) | Top-cited (n=27) |
|---|---|---|
| Empirical — quantitative | ~69% | ~67% |
| Empirical — mixed-methods | ~14% | ~22% |
| Empirical — qualitative | ~8% | ~4% |
| **Empirical (all)** | **~90%** | **~93%** |
| Review / meta-analysis / systematic review | ~10% | ~7% |
| Design / system (without empirical eval) | ~1% | 0% |
| Pure theory / conceptual | ~1% | 0% |
| Methods / instrument-only | ~0% | 0% |

**Verdict on the "empirical evidence of educational impact" reputation: CONFIRMED and strong.** [OBSERVED + INFERRED, High]
- ~90% of papers are empirical, and the dominant mode is quantitative or mixed-methods with controlled/quasi-experimental designs, surveys with SEM/regression, pre/post-tests, and effect sizes. Purely descriptive system papers, position pieces, and methods-only papers are essentially not published.
- The official scope corroborates the DO data: the journal **does NOT publish** "small-scale evaluations of specific software/systems ... in individual institutions unless the findings have broader relevance that is explicitly drawn out," and demands focus on **"implications for learning and teaching."** It **welcomes systematic reviews / meta-analyses** "with clear research questions, a framework of analysis, and conclusions that reflect the aims of the paper." (Source: Elsevier aims & scope via https://www.sciencedirect.com/journal/computers-and-education) [OBSERVED claim]
- [INFERRED, High] The operative gate is **generalizable educational impact evidence**: a tool/condition is only a vehicle; the publishable unit is rigorous evidence of an effect on learning/teaching processes or outcomes, with theory grounding and broad relevance.

---

## 4. Concrete recent paper examples (real titles)

All from the OpenAlex C&E corpus; citation counts as of 2026-06-01.

1. **"Impact of AI assistance on student agency"** (2023, ~363 cites). DOI: 10.1016/j.compedu.2023.104967.
   *Why publishable:* hot topic (AI assistance) + counter-intuitive construct (agency, not just performance) + empirical study with broad theoretical relevance. The single most-cited recent C&E paper — exemplifies "AI tool → measured effect on a learning-relevant construct."

2. **"ChatGPT improves creative problem-solving performance in university students: An experimental study"** (2024, ~275 cites). DOI: 10.1016/j.compedu.2024.105031.
   *Why publishable:* GenAI surge topic + **experimental design** (the journal's preferred evidence type) + a measured outcome (creative problem-solving). Textbook C&E template.

3. **"Beyond ChatGPT: A conceptual framework and systematic review of speech-recognition chatbots for language learning"** (2023, ~202 cites). DOI: 10.1016/j.compedu.2023.104898.
   *Why publishable:* fills the welcomed-but-rare **systematic review** lane, adds a **conceptual framework** (the scarce theory contribution), in a hot subdomain (chatbots + language learning).

4. **"A self-determination theory approach to teacher digital competence development"** (2024, ~106 cites). DOI: 10.1016/j.compedu.2024.105017.
   *Why publishable:* teacher digital competence (top-6 recurring topic) anchored to an established **theory (SDT)** — shows the journal rewards explicit theory grounding, not just tool evaluation.

5. **"Approaches and game elements used to tailor digital gamification for learning: A systematic literature review"** (2024, ~78 cites). DOI: 10.1016/j.compedu.2024.105000.
   *Why publishable:* PRISMA-style **systematic review** (43 articles) with clear RQs and an analysis framework — exactly what the editors say they welcome, in a mature topic (gamification).

6. **"Collaborative generative learning activities in immersive virtual reality increase learning"** (2023, ~74 cites). DOI in corpus.
   *Why publishable:* immersive VR (top-10 topic) + CSCL + a **measured learning gain** (causal-flavored claim) — tech-as-intervention with an outcome.

7. **"Effects of chatbot-assisted in-class debates on students' argumentation skills and task motivation"** (2023, ~156 cites).
   *Why publishable:* conversational agent intervention + **dual outcomes** (cognitive skill + motivation), quasi-experimental — high-impact mix-methods style.

8. **(Frontier 2026 examples showing the moving hot zone)** — "Innovating diagnostic learning: How generative AI explanation styles influence cognitive load and comprehension"; "Generative AI: A double-edged sword for creative thinking learning — Evidence from facial expression…"; "Do school-based ChatGPT policies bridge or widen gaps in students' computer and information literacy."
   *Why publishable:* GenAI has shifted from "does it work" to **mechanism, cognitive-process measurement, and equity** — the current cutting edge editors are buying.

---

## TL;DR for fit-checking a submission
- Must be **empirical with generalizable evidence of educational impact** (quant or mixed-methods preferred; controlled/quasi-experimental, SEM/regression, pre/post, effect sizes). [High]
- A bare system/tool description, a position/theory-only paper, or a single-course pilot without broad relevance = near-automatic misfit. [High]
- Strongest current bets: **generative AI in education with a mechanism/process or equity angle**, AI feedback, teacher AI/digital competence, and **methodologically rigorous systematic reviews/meta-analyses** (an under-filled, editor-welcomed lane). [Med-High]
- Always frame the technology as a vehicle; the contribution is the **learning/teaching evidence + theory link**, not the artifact. [High/INFERRED]
