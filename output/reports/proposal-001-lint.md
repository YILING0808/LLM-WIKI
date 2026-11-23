# Proposal 001 — Lint Report

- Run date: 2026-11-23
- Scope: approved initial copy, source SRC-001, four concept pages, index/log
- **Overall status: WARNING** (structural checks pass; provenance/clinical checks carry warnings)

## Mechanical checks

| Check | Result | Evidence |
|---|---|---|
| Relative Markdown links | PASS | 46 local links inspected; 0 broken |
| Concept page sections | PASS | 4 pages; 0 missing-template violations |
| Referenced source IDs | PASS | SRC-001; 0 unknown IDs |
| index links | PASS | All listed Markdown targets present |
| raw source copy fidelity | WARNING | `raw/guidelines/...md` is **metadata registration**, not an original-byte capture |

## Clinical / provenance warnings (expert review needed)

1. **WARNING — `raw/guidelines/ucla-positioning-and-technique.md`:** The URL content is educational material, not a formal guideline. Approved folder name retained for Proposal 001 compatibility; metadata explicitly flags category. **Remediation proposed, not applied:** future approved plan may reclassify file location under an education-source category.
2. **WARNING — `wiki/sources/SRC-001.md`:** No publisher publication/last-update date or immutable source file verified. **Remediation:** acquire permitted archival capture or record a verifiable official version/date.
3. **WARNING — `wiki/fundamentals/cc-view.md`:** The 1 cm PNL rule is attributed to the source but not independently validated as a currently applicable official guideline. **Remediation:** ingest authoritative QC guidance.
4. **WARNING — `wiki/sources/SRC-001.md`:** Implant view regulation claims on the source page have not been checked against current MQSA / local jurisdiction. Not promoted to general instructions. **Remediation:** verify from official regulations before any clinical recommendation.
5. **WARNING — image use:** UCLA figures are cited by section/Figure number only; no copying without permissions.
6. **WARNING — presentation readiness:** 1 of 5 minimum distinct sources ingested. AI, BI-RADS, Breast Density, findings and study metrics have no verified approved content. Do not generate final teaching deck yet.

## Failures / proposed repair

- Missing relative links: `[]`
- Missing page sections: `{}`
- Unknown source IDs: `[]`
- No Wiki edits were made in response to Lint; any extra repairs require a new approval batch.
