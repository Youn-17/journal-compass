# Computers & Education — Submission Requirements (Evidence Pack)

**Journal:** *Computers & Education* (Elsevier)
**ISSN:** 0360-1315
**Review model:** Double anonymized (double-blind)
**Reference style:** APA 7th edition
**Word limit:** ≤ 8,000 words (excluding references and appendices)
**Researched:** 2026-06-02

This file is structured so each section can be turned by a tool into a fill-in template (title-page checklist, cover-letter skeleton, declarations block, etc.). Every item carries a source URL and a confidence tag.

**Confidence tags:** `HIGH` = stated verbatim in the official C&E Guide for Authors or an official Elsevier policy page; `MEDIUM` = official Elsevier general/support page (applies across Elsevier journals, not C&E-specific); `LOW` = inferred / not explicitly confirmed for C&E.

### Primary sources
- C&E Guide for Authors: https://www.sciencedirect.com/journal/computers-and-education/publish/guide-for-authors
- Elsevier double-anonymized peer review requirements: https://www.elsevier.support/publishing/answer/what-are-the-requirements-for-doubleanonymized-peer-review
- Elsevier generative-AI-in-writing policy: https://www.elsevier.com/about/policies-and-standards/the-use-of-generative-ai-and-ai-assisted-technologies-in-writing-for-elsevier
- Elsevier Highlights guidelines: https://www.elsevier.com/researcher/author/tools-and-resources/highlights
- Elsevier cover-letter guidance: https://www.elsevier.support/publishing/answer/what-should-be-included-in-a-cover-letter
- Elsevier suggest/oppose reviewers: https://www.elsevier.support/publishing/answer/how-can-i-suggest-or-oppose-reviewers-for-my-submission

---

## 0. Files to upload (submission kit manifest)

Because C&E is double-anonymized, a complete submission is split across **separate files**. A generator should produce each of these as a distinct artifact.

| # | File | Required? | Contains | Confidence |
|---|------|-----------|----------|------------|
| 1 | **Title page** (separate file) | Required | All identifying info (authors, affiliations, corresponding author, acknowledgements, competing-interest declaration if no separate file) | `HIGH` |
| 2 | **Anonymized manuscript** (.doc/.docx or .tex) | Required | Main body + references + tables, NO identifying info | `HIGH` |
| 3 | **Highlights** (separate editable file, "highlights" in filename) | Required | 3–5 bullets, ≤85 chars each | `HIGH` |
| 4 | **Figures** (one file per figure, e.g. `Figure_1`) | Required if any | Editable source, anonymized | `HIGH` |
| 5 | **Declaration of Competing Interest** (.doc/.docx from declarations tool) | Required | Output of the online declarations tool | `HIGH` |
| 6 | **Graphical abstract** (separate file) | Encouraged (optional) | 531 × 1328 px (h × w) min | `HIGH` |
| 7 | **Cover letter** | Recommended (not mandatory) | See §2 | `MEDIUM` |
| 8 | **Supplementary material** | Optional | Cited in text | `HIGH` |
| 9 | **Suggested/opposed reviewers** | Entered in system if enabled, NOT in cover letter | Names + reasons | `MEDIUM` |

> File format rule: editable source files required for the whole submission. `.doc/.docx` for Word, `.tex` for LaTeX. **A PDF is not an acceptable source file.** Word files must be **single-column**; double-column is only allowed for LaTeX. `HIGH`
> Source: https://www.sciencedirect.com/journal/computers-and-education/publish/guide-for-authors

---

## 1. Title page vs. anonymized manuscript

### 1a. SEPARATE TITLE PAGE — required elements (checklist)

The title page is a **separate file**; it stays separate through peer review and is **not** sent to reviewers. `HIGH`

- [ ] **Article title** — concise, informative; avoid abbreviations/formulae unless established (e.g. DNA)
- [ ] **Author names** — given name(s) + family name(s) of each author; order must match the submission system; spelling checked. Optional: own-script name in parentheses after the English transliteration
- [ ] **Affiliations** — full postal address of each affiliation incl. country; tie to authors with lower-case superscript letters; include each author's email if available
- [ ] **Corresponding author** — clearly indicated; handles correspondence at all stages incl. post-publication
- [ ] **Corresponding author full postal address** — explicitly required on the title page for double-anonymized submissions
- [ ] **Corresponding author email address** — explicitly required on the title page
- [ ] **Present/permanent address** — footnote (superscript Arabic numeral) if an author moved since the work; main affiliation = where work was done
- [ ] **Acknowledgements** — go ONLY on the title page (help with language/writing/proofreading, etc.); never as a footnote to the title or elsewhere in the article
- [ ] **Declaration of competing interests** — put here ONLY IF a separate declaration-of-interest file is not submitted

Sources (all `HIGH`):
- Title page elements: https://www.sciencedirect.com/journal/computers-and-education/publish/guide-for-authors (section "Title page")
- Double-anonymized additions (acknowledgements, corresponding address+email, competing-interest fallback): https://www.sciencedirect.com/journal/computers-and-education/publish/guide-for-authors (section "Double anonymized peer review")

> NOTE on ORCID: The C&E Guide for Authors title-page list does **not** explicitly require ORCID on the title page; ORCID is collected by the Editorial Manager submission profile / and validated at the publishing-agreement stage. Treat ORCID as "supply in the submission system," not "on the title page." Confidence on placement: `MEDIUM` (not stated for C&E title page).
> NOTE on CRediT, funding, word count: These are NOT listed as title-page items. CRediT and funding belong in the manuscript declarations / system (see §4); a word count is not a required title-page field for C&E. `HIGH` (absence in title-page list) / `LOW` (where word count goes).

### 1b. ANONYMIZED MAIN MANUSCRIPT — what it contains / what must be REMOVED

Contains: the main body of the paper, **including references and tables**. `HIGH`

Must NOT contain any identifying information. Removal checklist (a tool can run this as an anonymity linter):

- [ ] **Remove author names and affiliations** everywhere in the body
- [ ] **Remove acknowledgements** entirely from the manuscript (they live on the title page only)
- [ ] **Remove references to funding sources** from the anonymized manuscript
- [ ] **Self-citation in third person** — replace "as we have shown before" with "… has been shown before [Anonymous, 2007]"
- [ ] **In-text self-citations** rendered as `[Anonymous, 2007]`
- [ ] **Reference-list self-citations** rendered as `[Anonymous 2007] Details omitted for double-anonymized reviewing.`
- [ ] Do NOT remove essential self-references entirely — keep only those relevant to reviewers, just anonymize them
- [ ] **Figures** must not contain any affiliation-related identifier
- [ ] **File names** must not contain author names
- [ ] **Document properties / metadata** must be anonymized (clear author field in file properties)

Sources (all `HIGH`):
- https://www.sciencedirect.com/journal/computers-and-education/publish/guide-for-authors (section "Double anonymized peer review")
- https://www.elsevier.support/publishing/answer/what-are-the-requirements-for-doubleanonymized-peer-review

---

## 2. Cover letter

**Status:** Not listed as mandatory in the C&E Guide for Authors. Elsevier *recommends* a cover letter as good practice and provides explicit guidance on its contents; Editorial Manager has a dedicated cover-letter field. Treat as **recommended / expected-but-not-enforced**. `MEDIUM`

### Cover-letter skeleton (fill-in template)

```
Dear Editor [name if known],

[1 SIGNIFICANCE + FINDINGS]  Aim of the study and main findings, no unnecessary detail.
[2 FIT TO SCOPE]             How the work fits Computers & Education's aim and scope
                             (pedagogical uses of digital technology; broad enough for the
                             wider education community).
[3 NOVELTY + IMPLICATIONS]   Why it is novel and its broader implications for learning/teaching.
[4 ORIGINALITY/EXCLUSIVITY]  Statement that the work is original, not published before
                             (preprint excepted), and not under consideration elsewhere.
[5 INVITATION]               Mention if you were invited to submit (e.g. special issue).
[6 OPTIONAL]                 Special considerations; brief background/data-collection note;
                             prior/concurrent submission details; topicality.

Sincerely,
[Corresponding author name, affiliation, contact]
```

**Keep it under one page and focused.** `MEDIUM`

### Do NOT put in the cover letter (put in the system instead):
- Funding information
- Author declarations (competing interest, etc.)
- Suggested or opposed reviewers
> "If these details are needed, they will be requested separately." `MEDIUM`

Sources:
- https://www.elsevier.support/publishing/answer/what-should-be-included-in-a-cover-letter (`MEDIUM`)
- Scope wording for the "fit" paragraph: https://www.sciencedirect.com/journal/computers-and-education/publish/guide-for-authors (`HIGH`)

---

## 3. Abstract, Keywords, Highlights, Graphical Abstract

### 3a. Abstract `HIGH`
- **Format: UNSTRUCTURED** (no mandated subheadings) — "a concise and factual abstract."
- **Word cap: ≤ 250 words.**
- Must state purpose, principal results, major conclusions.
- Must stand alone (often presented separately from the article).
- Avoid references; if essential, cite author(s) + year(s). References cited in the abstract must be given in full.
- Avoid non-standard/uncommon abbreviations; define at first mention if essential.
- Source: https://www.sciencedirect.com/journal/computers-and-education/publish/guide-for-authors

### 3b. Keywords `HIGH`
- **1 to 7 keywords**, in English, for indexing.
- Avoid multi-word keywords using "and"/"of".
- Abbreviations only if firmly established in the field.
- Source: https://www.sciencedirect.com/journal/computers-and-education/publish/guide-for-authors

### 3c. Highlights — REQUIRED at submission `HIGH`
- **3 to 5 bullet points.**
- **Each bullet ≤ 85 characters, INCLUDING spaces.**
- Capture novel results + any new methods.
- Submit as a **separate editable file** (Word) with the word **"highlights" in the file name** / select "Highlights" from the file-type drop-down.
- Sources: https://www.sciencedirect.com/journal/computers-and-education/publish/guide-for-authors and https://www.elsevier.com/researcher/author/tools-and-resources/highlights

Fill-in template:
```
Highlights (3–5 lines, ≤85 chars each incl. spaces)
- ...
- ...
- ...
```

### 3d. Graphical abstract — ENCOURAGED (optional) `HIGH`
- **Optional** ("You are encouraged to provide…"), not mandatory.
- Single concise pictorial summary; submit as a **separate file**.
- **Size: 531 × 1328 pixels (h × w)** minimum, or proportionally larger; must be readable at **5 × 13 cm**.
- **Preferred file types: TIFF, EPS, PDF, or MS Office files.**
- Obtain permission for any third-party material.
- **Generative AI / AI-assisted tools are NOT permitted** to produce graphical abstracts (per Elsevier GenAI policy).
- Source: https://www.sciencedirect.com/journal/computers-and-education/publish/guide-for-authors

---

## 4. Declarations / mandatory statements

A generator should emit a **declarations block** placed appropriately (most at end of manuscript before references; competing-interest via the declarations tool; acknowledgements/funding handled per anonymization rules).

### 4a. Declaration of Competing Interest — REQUIRED `HIGH`
- All authors must disclose financial/personal relationships that could bias the work.
- Example categories: employment, consultancies, stock ownership, honoraria, paid expert testimony, patent applications/registrations, grants/other funding, **affiliation with the journal as an Editor or Advisory Board Member**.
- **The declarations tool must always be completed.** If nothing to declare, select **"I have nothing to declare."**
- Output a **.doc/.docx** file from the tool and upload at the "attach/upload files" step. Author signatures not required.
- Journal-affiliated authors must add specified text under "Other Activities" and notify the journal before submitting:
  > "Given their role as [journal role title], [name] had no involvement in the peer-review of this article and has no access to information regarding its peer-review. Full responsibility for the editorial process for this article was delegated to another journal editor."
- For the double-anonymized split: if no separate declaration file is submitted, the competing-interest statement goes on the **title page** (not in the anonymized manuscript).
- Source: https://www.sciencedirect.com/journal/computers-and-education/publish/guide-for-authors

Template:
```
Declaration of competing interest
The authors declare that they have no known competing financial interests or personal
relationships that could have appeared to influence the work reported in this paper.
[OR: list each interest by author.]
```

### 4b. CRediT author statement / Author contributions — REQUIRED `HIGH`
- Corresponding authors **must** acknowledge co-author contributions using **CRediT** (Contributor Roles Taxonomy).
- The 14 roles: Conceptualization; Data curation; Formal analysis; Funding acquisition; Investigation; Methodology; Project administration; Resources; Software; Supervision; Validation; Visualization; Writing – original draft; Writing – review & editing.
- Not all roles apply to every paper; authors may hold multiple roles.
- Source: https://www.sciencedirect.com/journal/computers-and-education/publish/guide-for-authors

Template:
```
CRediT authorship contribution statement
[Author A]: Conceptualization, Methodology, Writing – original draft.
[Author B]: Formal analysis, Visualization.
[Author C]: Supervision, Writing – review & editing.
```
> Anonymity note: a CRediT statement naming authors is identifying — keep it OFF the anonymized manuscript and provide it on the title page / system, or insert at acceptance. (`LOW` on exact placement; C&E does not specify, but it is identifying info.)

### 4c. Data Availability / Data statement — REQUIRED `HIGH`
- C&E uses research-data **Option C**: authors are **required** to deposit research data in a relevant repository, **cite and link** the dataset in the article, OR — if not possible — provide a statement explaining why data cannot be shared.
- A **data (availability) statement is required at submission**; appears with the published article on ScienceDirect.
- Source: https://www.sciencedirect.com/journal/computers-and-education/publish/guide-for-authors

Template:
```
Data availability
[The data that support the findings of this study are openly available in [repository] at [DOI/URL].]
[OR: The data are not publicly available because [reason, e.g. they contain information that could
compromise participant privacy].]
```

### 4d. Funding statement — REQUIRED (state even if none) `HIGH`
- Disclose all funding sources; declare the role of sponsors in study design, data collection/analysis/interpretation, report writing, and the decision to submit. If sponsors had no such involvement, state it.
- Standard format:
  > "Funding: This work was supported by the [Funder] [grant numbers xxxx, yyyy]; …"
- If no funding:
  > "This research did not receive any specific grant from funding agencies in the public, commercial, or not-for-profit sectors."
- Anonymity note: funding references must be **removed** from the anonymized manuscript and restored on title page / at acceptance.
- Source: https://www.sciencedirect.com/journal/computers-and-education/publish/guide-for-authors

### 4e. Ethics approval / informed consent `HIGH (policy exists) / MEDIUM (exact statement wording)`
- Authors must follow Elsevier's **Publishing Ethics Policy** (general ethics requirement).
- **Submission declaration** (implied on submission): work not previously published (preprint/abstract/thesis/registered report excepted); not under consideration elsewhere; approved by all authors and by responsible authorities where the work was carried out; if accepted, won't be published elsewhere in the same form.
- **Sex- and gender-based analysis (SGBA):** when research involves humans/animals/eukaryotic cells, integrate SGBA into design; address sex/gender dimensions or declare as a limitation; explicitly define sex and/or gender used (SAGER guidelines + SAGER checklist).
- Note: The C&E Guide for Authors does not print a single fixed "ethics approval / informed consent" boilerplate sentence; education-research human-subjects approval is governed by the general Publishing Ethics Policy + responsible-authorities approval in the submission declaration. Provide IRB/ethics approval + informed-consent statements in the manuscript per institutional norms. (`MEDIUM` on exact wording.)
- Sources: https://www.sciencedirect.com/journal/computers-and-education/publish/guide-for-authors ; Elsevier Publishing Ethics Policy (linked therein)

Template:
```
Ethics approval and consent
This study was approved by the [name] Institutional Review Board / Ethics Committee
(approval no. [xxx]). Informed consent was obtained from all participants
[and/or their legal guardians].
```

### 4f. Declaration of Generative AI use in writing — REQUIRED IF AI USED `HIGH`
- Authors **must declare** use of generative AI in manuscript preparation at submission.
- Place a statement at the **end of the manuscript, in a new section BEFORE the references list**. It appears in the published work.
- **Section title:** "Declaration of generative AI and AI-assisted technologies in the manuscript preparation process."
- **Statement template:**
  > "During the preparation of this work the author(s) used [NAME OF TOOL / SERVICE] in order to [REASON]. After using this tool/service, the author(s) reviewed and edited the content as needed and take(s) full responsibility for the content of the published article."
- **Exemptions:** basic tools for grammar, spelling, and references do NOT require a declaration. If nothing to disclose, no statement is needed.
- AI **must not** be listed or cited as an author/co-author.
- Authors remain fully accountable; must verify AI output (incl. checking for fabricated references).
- **Figures/images:** GenAI may NOT be used to create/alter images (sole exception: AI as part of the research method/design, fully disclosed in Methods with model name, version, manufacturer). GenAI not permitted for graphical abstracts.
- **Reviewers/editors** of C&E may NOT use generative AI in peer review.
- Sources: https://www.sciencedirect.com/journal/computers-and-education/publish/guide-for-authors and https://www.elsevier.com/about/policies-and-standards/the-use-of-generative-ai-and-ai-assisted-technologies-in-writing-for-elsevier

---

## 5. Manuscript format

| Item | Requirement | Confidence | Source |
|------|-------------|-----------|--------|
| **Word limit** | **≤ 8,000 words**, excluding references and appendices | `HIGH` | C&E GfA "Journal specific information" |
| **Reference style** | **APA 7th edition** (Publication Manual of the APA, 7th ed., 2020, ISBN 978-1-4338-3215-4). Reference list alphabetical then chronological; same-author-same-year disambiguated a, b, c | `HIGH` | C&E GfA "References" |
| **Section structure** | Numbered sections: 1, then 1.1 / 1.1.1, 1.2 … Use numbers when cross-referencing (not "the text"). Abstract is not numbered. IMRAD-style implied but not rigidly mandated; systematic reviews/meta-analyses should follow PRISMA | `HIGH` | C&E GfA "Article structure" / "Aims and scope" |
| **Tables** | Editable text (NOT images); cited in text; numbered consecutively; captions provided; notes below body; avoid vertical rules and cell shading; use sparingly | `HIGH` | C&E GfA "Tables" |
| **Figures** | Separate files, one per figure (e.g. `Figure_1`); cited and numbered in order; every figure needs a caption (brief title + description). Vector: EPS/PDF. Halftone photos: TIFF/JPG/PNG ≥300 dpi. Bitmap line art: ≥1000 dpi. Combination: ≥500 dpi | `HIGH` | C&E GfA "Figures, images and artwork" |
| **File types** | `.doc/.docx` (Word, single-column) or `.tex` (LaTeX, Elsevier template, may be double-column). PDF NOT accepted as source. Editable source required for everything | `HIGH` | C&E GfA "File format" / "LaTeX" |
| **Language** | American OR British English, not a mix | `HIGH` | C&E GfA "Language and editing services" |
| **Footnotes/Appendices** | Footnotes used sparingly, numbered consecutively. Appendices labelled A, B…; appendix equations Eq. (A.1); appendix tables/figures Table A.1, Fig. A.1 | `HIGH` | C&E GfA "Article structure" |
| **DOIs in references** | Encouraged as reference links | `HIGH` | C&E GfA "References" |

Source (all rows): https://www.sciencedirect.com/journal/computers-and-education/publish/guide-for-authors

---

## 6. Submission system & process

- **System:** Elsevier online submission system. The Guide refers to "Editorial Manager" by name (the "Attach files" page is referenced for co-submissions), and the system converts uploaded files into a single PDF used for peer review. `HIGH` (online system + PDF conversion) / `MEDIUM` (explicit "Editorial Manager" branding for C&E)
- **Suggested / opposed reviewers:** Not stated as mandatory in the C&E Guide for Authors. If the journal has enabled the option, it appears under the **"Review Preferences"** step in Editorial Manager; authors locate their own suggestions; the editor decides whether to use them. **Do not put reviewer suggestions in the cover letter.** `MEDIUM`
  - Source: https://www.elsevier.support/publishing/answer/how-can-i-suggest-or-oppose-reviewers-for-my-submission
- **Correspondence:** all decisions/revision requests sent by email to the corresponding author. `HIGH`
- **Peer review:** double anonymized; editor triage first, then typically ≥2 reviewers; editor makes the decision. Papers not meeting the author guidelines are **returned without review.** `HIGH`
- **Proofs:** corrections requested within 2 days. `HIGH`

### Official Elsevier submission checklist (C&E) `HIGH`
Source: https://www.sciencedirect.com/journal/computers-and-education/publish/guide-for-authors ("Submission checklist")

- [ ] One author designated **corresponding author** with full contact details (email, full postal address, phone)
- [ ] All files uploaded — tables and figures (with titles, captions, footnotes), keywords, supplementary materials, videos
- [ ] Spelling and grammar checks done
- [ ] All in-text references in the reference list and vice versa
- [ ] Permission obtained for any copyrighted material (incl. from the Web)
- [ ] For open-access articles, authors understand they are responsible for the APC if accepted

### Derived "submission kit" checklist (combines the above + double-anonymized rules) — for the generator
- [ ] Title page file (with all identifying info, acknowledgements, corr. address + email)
- [ ] Anonymized manuscript (≤8,000 words; APA 7; numbered sections; no names/affiliations/acknowledgements/funding; self-cites anonymized; metadata scrubbed)
- [ ] Highlights file (3–5 bullets, ≤85 chars; "highlights" in filename)
- [ ] Figures as separate editable, anonymized files (correct dpi/format)
- [ ] Tables embedded as editable text
- [ ] Declaration of Competing Interest (.docx from declarations tool)
- [ ] Data availability statement (Option C — deposit + cite + link, or justify)
- [ ] Funding statement (or the "no specific grant" sentence)
- [ ] CRediT author contribution statement
- [ ] Generative-AI declaration (only if AI used; section before references)
- [ ] Ethics / informed-consent statement (as applicable)
- [ ] Abstract ≤250 words (unstructured); 1–7 keywords
- [ ] Graphical abstract (optional; 531×1328 px; TIFF/EPS/PDF/MS Office)
- [ ] Cover letter (recommended; significance + scope fit + novelty + originality/no concurrent submission; NO funding/declarations/reviewers)
- [ ] Suggested/opposed reviewers entered in system if the option is enabled

---

## 7. Quick-reference numbers (for assertions / validation)

| Parameter | Value | Confidence |
|-----------|-------|-----------|
| Manuscript word limit | 8,000 (excl. refs + appendices) | `HIGH` |
| Abstract word cap | 250 | `HIGH` |
| Abstract structure | Unstructured | `HIGH` |
| Highlights count | 3–5 | `HIGH` |
| Highlight char limit | 85 (incl. spaces) | `HIGH` |
| Keywords | 1–7 | `HIGH` |
| Reference style | APA 7th (2020) | `HIGH` |
| Review model | Double anonymized | `HIGH` |
| Min reviewers (typical) | 2 | `HIGH` |
| Graphical abstract size | 531 × 1328 px (h × w), readable at 5×13 cm | `HIGH` |
| Word layout | Single-column (LaTeX may be double) | `HIGH` |
| Proof turnaround | 2 days | `HIGH` |
| Cover letter | Recommended, not mandatory | `MEDIUM` |
| ORCID on title page | Not required by C&E title-page list | `MEDIUM` |
