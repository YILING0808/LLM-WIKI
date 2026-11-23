# AGENTS.md — Mammography AI Wiki

## 1. Project mission and operating principles

Build and maintain a **persistent, evidence-traceable Mammography AI Wiki** for educational use. The wiki covers fundamentals of mammography through clinical applications of AI in breast cancer detection. Its primary audience is radiologic technologists and related healthcare professionals, but the first teaching presentation must also be understandable to learners with **no prior knowledge of mammography or AI**.

This repository follows the Karpathy-style LLM Wiki pattern:
1. Immutable **raw sources** are the primary evidence.
2. A structured, interlinked **wiki** accumulates and synthesizes knowledge across sources.
3. This **AGENTS.md** governs ingestion, querying, maintenance, review, and presentation generation.

**Non-negotiable:** Discuss first, propose changes, obtain explicit approval for the specific change batch, and only then change wiki files. A previous approval is not blanket authorization. Never fabricate clinical findings, citations, numerical results, or evidence.

This is an **educational literature wiki**, not a patient-specific diagnostic or clinical decision system. Make applicable population, modality, setting, limitations, and guideline jurisdiction clear.

## 2. Repository layout and file permissions

```text
mammography-ai-wiki/
├── AGENTS.md
├── raw/
│   ├── guidelines/           # Authoritative guidelines, original unmodified copies
│   ├── papers/               # Research papers, original unmodified copies
│   └── assets/               # Licensed/attributed source images
├── wiki/
│   ├── index.md              # Topic-oriented navigation, updated with approved changes
│   ├── log.md                # Append-only chronological activity history
│   ├── fundamentals/         # Mammography principles, CC/MLO, breast density, image quality
│   ├── imaging-findings/     # Mass, calcifications, architectural distortion, BI-RADS
│   ├── ai-methods/           # AI, DL, CNN, datasets, performance metrics
│   ├── clinical-applications/# CADe, CADx, AI-assisted reading, DBT, workflow
│   ├── evidence-and-limitations/ # Clinical evidence, bias, generalizability, safety
│   └── sources/              # One evidence summary per original source
├── output/
│   ├── slides/               # HTML slide decks and supporting assets
│   └── reports/              # Ingest, lint, and presentation audit reports
└── tools/                    # Optional validation utilities; only when needed
```

Do not create folders or placeholder pages simply to satisfy the example tree; create only what the current authorized operation requires.

### Permissions
- `raw/**`: read-only; never silently alter, overwrite, or delete originals. If new sources need to be added, propose placement and retain provenance.
- `wiki/**`: modifications require a **specific approved change plan**. This includes new pages, edits, index changes, and lint fixes.
- `wiki/log.md`: append-only. An approved wiki change includes its corresponding log entry; never rewrite past entries.
- `output/reports/**`: analysis and proposed plans may be saved as reports when the user asks. Logging here must never bypass the wiki review gate.
- `output/slides/**`: generate final HTML only after the user approves the presentation outline and generation. Never overwrite an existing final artifact without authorization.
- `AGENTS.md`: changes require explicit discussion and approval.

## 3. Source policy and evidence traceability

Use a mix of **authoritative clinical guidance** and **peer-reviewed medical/AI research**. Source prioritization is contextual, not a claim that one source type always supersedes another:
1. Relevant official clinical and professional guidance for recommended practice; record edition, date, country/organization and scope.
2. Systematic reviews/meta-analyses for cross-study evidence (with attention to quality and heterogeneity).
3. Peer-reviewed original studies for concrete methods, data and results.
4. Authoritative technical documents for technology definitions.
5. General webpages only as supplemental explanatory material, never as sole support for consequential clinical claims.

Target at least **five distinct original source documents** for the first assignment milestone. Never count multiple summaries of one document as multiple ingested sources.

Assign each approved original source a stable ID: `SRC-001`, `SRC-002`, etc. Every study-dependent assertion, measurement and important clinical conclusion must trace to a source ID plus a location (page, section, figure, table, or an exact identifiable passage when available). Preserve citation metadata (title, authors, year, publisher/journal, DOI or stable URL, source type, version/date, access date for online mutable content).

For a study extract, when applicable: objective, study design, population/eligibility, sample size/unit of analysis, imaging modality (e.g. FFDM vs DBT), AI task and role, comparator/reference standard, dataset provenance/splits, primary outcomes, point estimates and confidence intervals, key findings, limitations and applicability. If unreported or inaccessible, write **Not reported** / **Not verified**, not a guess.

**Important distinctions:** screening vs diagnostic mammography; CADe vs CADx vs risk prediction; standalone AI vs reader-assist vs triage; FFDM vs DBT; per-image vs per-exam vs per-patient results; sensitivity vs specificity vs AUC; retrospective validation vs prospective clinical impact. Do not generalize results across these distinctions without evidence.

Never claim to have read full text if only an abstract or citation is available. Distinguish source claims from cross-source inference. Do not reproduce copyrighted figures without appropriate permission/licensing and attribution.

## 4. Wiki schemas and conventions

### Concept page (primary knowledge unit)
Use a stable descriptive lowercase kebab-case filename and an H1 title. Include relevant sections only; do not fill unsupported content for the sake of a template.

```markdown
# Breast Density

## Beginner Explanation
## Definition and Key Concepts
## Why It Matters / Clinical Relevance
## Connection to Mammography and AI
## Evidence and Applicability
## Limitations and Open Questions
## Related Topics
## References
## Last Reviewed
```

- `Beginner Explanation` explains the concept in plain **Traditional Chinese** with English professional terms, when this page may support introductory teaching.
- Link to related local wiki pages by working relative Markdown links; no unsupported cross-references.
- Distinguish **well-established definition/guideline**, **study finding**, and **interpretation/inference**.
- Important claims cite relevant `SRC-xxx` pages and, where possible, source locations.
- Retain nuance when updating: do not silently delete valid older evidence because a newer publication disagrees.

### Source page (one per original document)

```markdown
# SRC-001 — [Exact source title]

## Bibliographic Information
## Verification and Source Access
## Research Question / Scope
## Design, Population and Methods
## Imaging Modality and AI Task
## Key Findings (with source locations)
## Limitations and Generalizability
## Related Concept Pages
## Original Source
```

Use `Not applicable` for non-study guidelines where relevant, and `Not reported` for missing study details. Keep direct source facts separate from agent commentary. Never invent citations or study statistics.

### Index and log
- `wiki/index.md`: catalog pages by topic; for each page include a working relative link and one-line description. Use it first during Query.
- `wiki/log.md`: append entries in consistent form `## [YYYY-MM-DD] action | description`, listing approved source IDs, added/changed pages, approval basis, lint outcome, and unresolved issues. Record proposals or rejected actions as *not applied* if logged, without implying they were committed.

## 5. Human approval gate (mandatory for persistent changes)

For any wiki change, first prepare **one consolidated change proposal** containing:
1. Source identification and verified access status.
2. Concise summary of new evidence and its clinical relevance.
3. Exact files to create, edit, or append (including `index.md` and `log.md`).
4. Per-file proposed changes and supporting source IDs/locations.
5. Conflicts, evidence gaps, uncertainties and potential clinical implications.
6. Risks and the validation plan.

Then **stop and request explicit approval of this batch**. Approval must correspond to that proposal; modified scope requires renewed approval. If rejected, revise or abandon without touching wiki content. If partially approved, implement only the approved subset and adjust the change plan accordingly. A user approving an outline is not automatically approving ingestion, and vice versa.

The agent may perform read-only inspection, analysis, querying, and lint reports without this gate. No tool invocation or automation may silently bypass it.

## 6. Ingest workflow (source → accumulated knowledge)

**Trigger:** User submits a document, DOI/URL, or asks to ingest a source.

1. **Register and verify** source identity, type, version, accessibility and duplicates. Report if full text cannot be inspected.
2. **Read and extract** faithfully. Build a structured source summary; locate exact evidence supporting important facts.
3. **Map against the existing wiki**: read `index.md`, relevant concept pages and related `wiki/sources` pages.
4. **Compare and reconcile cautiously**: identify evidence that supports, extends, qualifies or challenges existing statements. Distinguish true contradictions from differences in populations, metrics, workflows and modalities.
5. **Draft the source page and concept edits as a proposal**; specify every affected file. Do not write to `wiki/` yet.
6. **Human Review:** show the batch proposal and wait for explicit approval.
7. **Apply only approved changes**: source page, concept pages, cross-links, `index.md`, and append to `log.md`.
8. **Post-update Lint**: verify references, links, schema and clinical/terminological consistency. If fixes require wiki edits beyond approved scope, propose them rather than silently fixing.
9. **Report** actual changes, evidence gaps, lint result and pending follow-ups.

**Loop:** Steps 3–5 repeat if evidence conflicts or the proposed summary lacks provenance. After the commit, failed lint loops back to a proposed repair and approval, not autonomous edits.

## 7. Query workflow (wiki-first answers)

**Trigger:** User asks a knowledge question.

1. Read `wiki/index.md` to locate relevant topics.
2. Read concept pages and underlying source summaries as necessary.
3. Cross-check relevant statements and qualifiers against original sources when possible.
4. Compose an answer in **Traditional Chinese**, retaining English medical/AI technical terms, with source IDs and citations for consequential claims.
5. If evidence is absent, uncertain, inconsistent or outdated, say so. Do not silently supplement the wiki with unapproved external findings. Offer a source-ingest proposal if needed.
6. If the answer reveals a useful novel synthesis, **propose** creating/updating a wiki page; never auto-commit it.

**Loop:** Search additional related wiki pages if the evidence is insufficient; terminate with a clearly stated gap rather than invented certainty.

## 8. Lint workflow (read-only until approved)

**Trigger:** After an approved ingest, at user request, or before building a presentation.

Check:
- **Structure**: naming, page headings, IDs, source metadata, index completeness.
- **Links**: relative links, referenced source IDs, orphan pages, duplicate entries.
- **Evidence**: unsupported claims, missing citations, numerical discrepancies, uncertain provenance.
- **Clinical consistency**: BI-RADS and relevant terminology, FFDM/DBT distinctions, AI role, applicability, study design, outdated guidance and apparent contradictions.
- **Language**: Traditional Chinese prose, English professional terms, consistency with approved terminology.

Classify findings:
- `PASS`: passes defined checks; not a certification of clinical accuracy.
- `WARNING`: gaps, staleness, questionable applicability, missing optional links, apparent conflicts needing review.
- `FAIL`: broken required links, nonexistent citations, material contradictions or demonstrably unsupported key claims.

Output a report with severity, file/section, issue, evidence and proposed remediation. **Never silently edit wiki files** as a result of lint. Distinguish mechanically verified findings from items requiring expert judgment.

## 9. Presentation workflow — first fixed teaching deck

**Fixed topic:** **「乳房攝影與人工智慧：從基礎影像到 AI 輔助乳癌偵測」**.

**Audience:** Radiologic technologists and related healthcare professionals, explicitly accessible to learners unfamiliar with mammography and AI.

### Instructional design requirements
- **All narrative content, slide titles, explanations, interactions, navigation, and quizzes must be in Traditional Chinese (`zh-TW`)**. **Keep medical and AI professional terms in English** (e.g. Mammography, Breast Density, Mass, Calcification, Architectural Distortion, BI-RADS, FFDM, DBT, CC View, MLO View, Deep Learning, CNN, CADe, CADx, Sensitivity, Specificity, AUC). On first use, explain technical terms clearly in Traditional Chinese; preserve original English bibliographic titles.
- Avoid Simplified Chinese. Maintain a consistent English terminology glossary.
- **Beginner-first progression**: explain prerequisites before dependent ideas; one main idea per slide; use concrete clinical examples; translate abstract metrics into intuitive hypothetical examples before formulas.
- Mark hypothetical teaching examples clearly as **illustrative**, not real study findings.
- Use visuals/diagrams when educationally valuable, but verify provenance, image interpretation and usage rights. Do not invent clinical mammograms or represent synthetic diagrams as real cases.
- Every important study- or guideline-dependent slide must cite its approved wiki/source evidence; include an accessible references section.
- Avoid overstating AI performance, clinical applicability or replacing healthcare professionals.

### Proposed six-unit outline
1. Why mammography matters: screening purpose and basic X-ray image formation.
2. How to read the basics: CC/MLO, Breast Density, Mass, Calcification, Architectural Distortion, introductory BI-RADS.
3. What AI learns: AI, Deep Learning, CNN and basic training/validation concepts.
4. Clinical AI: CADe/CADx, assisted reading and workflows, with clear distinction from autonomous diagnosis.
5. Evidence and limitations: Sensitivity, Specificity, false positives, generalization, clinical study interpretation.
6. Knowledge checks and synthesis: 2–3 interactive quizzes, takeaway summary, references.

Target approximately **12–15 slides**, adjusted for clarity rather than mechanically enforced. The deck must be comprehensible without advanced AI knowledge.

### Generation steps
1. Define learning objectives and audience prerequisites.
2. Read approved `wiki/index.md`, relevant concept pages and source summaries.
3. Map each proposed slide to supporting wiki pages and source IDs.
4. Check **knowledge completeness**. If necessary foundations or evidence are missing, stop deck generation, state the gap, and propose a separate Ingest plan. Do not silently browse and slip new information into the deck.
5. Present a slide-by-slide **outline with citations** to the user for approval before generating the final file.
6. Generate self-contained or properly bundled **navigable HTML** (previous/next, keyboard navigation if feasible, page numbers, responsive layout, source references, working quizzes with feedback).
7. Validate educational ordering, first-use terminology explanations, citation mapping, HTML functionality, media accessibility/attribution, and `zh-TW` language consistency. Test in a browser where tooling permits; otherwise disclose untested behavior.
8. Save a presentation audit in `output/reports/` mapping slide numbers to wiki pages and original sources, and record unresolved gaps.

**Loops:** (a) missing prerequisite/evidence → propose Ingest → human approval → updated wiki → return to slide mapping; (b) slide validation failure → revise the deck → revalidate. Neither loop overrides the wiki approval gate.

## 10. Completion criteria and reporting

The initial assignment-ready demonstration should provide evidence for:
- At least **5 distinct source ingests** with reliable metadata and provenance.
- A concept-first, interlinked wiki with source summaries and updated `index.md`/`log.md`.
- At least one **visible before/after cross-document synthesis** showing changed concept pages.
- A real **human-approved change plan**, rather than automatic silent edits.
- Query answers with source traceability and honest uncertainty.
- A lint report that surfaces at least one meaningful check and makes unresolved issues visible.
- A usable **Traditional Chinese HTML teaching deck**, English specialist terms, beginner-level explanation, accessible references, and interactive learning checks.
- A concise execution trace explaining the **Ingest, Query, Lint and Presentation loops/graph**, approval gates, and any failures or reruns.

At the end of each operation, report: **what was inspected; what was proposed; what was approved; what actually changed; evidence/verification status; unresolved issues; next permissible action**. Never describe a proposed action as completed.
