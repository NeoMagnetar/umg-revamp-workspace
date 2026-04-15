# BATCH-116 — Contradiction Flags

## Overall Status
- **Contradiction Watch:** MEDIUM
- **Reason:** The batch turns on several similar-looking but materially different states that could be collapsed incorrectly in later canon or workflow docs.

## Flag 1 — Enabled vs Enumerable
- **Tension:** The user’s UI showed Drive enabled, but direct folder enumeration still did not happen in the session.
- **Why it matters:** Users may assume UI enablement equals enumeration capability.
- **Required caution:** Keep enabled, authorized, attached, and enumerable as separate states.

## Flag 2 — Governance vs Capability
- **Tension:** The user tested whether governance had blocked the connector; the source found no evidence of explicit exclusion.
- **Why it matters:** Tool-surface limits could be misread as governance behavior.
- **Required caution:** Treat connector limitations as external/tool-surface constraints unless an explicit governance artifact exists.

## Flag 3 — Heuristic Audit Only
- **Tension:** The governance audit was heuristic and based on absence of evidence in the source.
- **Why it matters:** Later summaries may overstate the certainty of the result.
- **Required caution:** Preserve the result as “no evidence found here,” not as a universal rule.

## Flag 4 — Fallback Protocol Not Yet Standardized
- **Tension:** Manual paste, scripted export, and screenshot transcription were proposed as fallbacks, but no project-wide fallback protocol was locked.
- **Why it matters:** Similar cases may be handled inconsistently later.
- **Required caution:** Treat current fallback methods as provisional until standardized.
