# INTAKE RANGE WORKFLOW STATUS — BATCHES 001–025

## Overall Workflow Status
**Workflow status: ADJUSTED**

The Stage 1 workflow remained stable in purpose, but several operational adjustments were made inside the range.

## Confirmed Stage 1 Pattern Used
The batch workflow executed as:

1. receive one source batch
2. treat source as evidence, not canon
3. assign next sequential batch number
4. create one zip handoff package
5. include the default four files:
   - REVIEW
   - EVIDENCE_ENTRY
   - PROJECT_IMPACT
   - DEFINITIONS
6. add optional extracts only when justified
7. include one PowerShell sorter block
8. map files to approved workspace destinations

## Default File Types Used
The default file types across the range were:

- `.md` for all batch artifacts
- `.zip` for each handoff package

No alternate artifact type was used for the Stage 1 packs themselves.

## Routing Assumptions Used
The range consistently used these routing assumptions:

### Default destinations
- `*_REVIEW.md` -> `01_INTAKE\reviewed_batches`
- `*_EVIDENCE_ENTRY.md` -> `01_INTAKE\pending_evidence_entries`
- `*_PROJECT_IMPACT.md` -> `01_INTAKE\pending_impact_maps`
- `*_DEFINITIONS.md` -> `05_DOCUMENTATION\core_definitions\intake_definitions`

### Optional destinations
- `*_COMPILER_EXTRACT.md` -> `04_COMPILER\intake_extracts`
- `*_SLEEVE_EXTRACT.md` -> `05_DOCUMENTATION\sleeves\intake_extracts`
- `*_BLOCKS_MOLT_EXTRACT.md` -> `05_DOCUMENTATION\blocks_and_molt\intake_extracts`
- `*_NEOSTRUCTURE_EXTRACT.md` -> `05_DOCUMENTATION\neoblocks_and_neostacks\intake_extracts`
- `*_CONTRADICTION_FLAGS.md` -> `02_SYNTHESIS\contradictions_and_conflicts`
- `*_CANON_CANDIDATES.md` -> `03_CORE_ALIGNMENT\candidate_fragments`

## Optional File Usage Pattern
Optional files were added when strongly justified by source content.

### Strongest recurring optionals
Most frequently justified:
- `COMPILER_EXTRACT`
- `SLEEVE_EXTRACT`
- `BLOCKS_MOLT_EXTRACT`
- `NEOSTRUCTURE_EXTRACT`

### Less frequent but justified when needed
- `CONTRADICTION_FLAGS`
- `CANON_CANDIDATES`

### Minimal batches
A few batches were intentionally minimal when source content was thin or inaccessible.
Most notable:
- `BATCH-024` was correctly handled as a minimal placeholder/hold because the source explicitly said the actual transcript body was inaccessible.

## Problems and Deviations Observed
The main operational issues in this range were:

### 1) Formatting drift in some responses
A few responses became too dense or visually compressed for easy reuse.
This later required:
- reissue requests
- cleaner spacing
- clearer file listing layout

### 2) Session/tool resets
At least one batch required regeneration/reissue after a session/code reset.
This did not change content scope, but it did create recovery work.

### 3) Inaccessible or partial source content
Some source batches were incomplete or explicitly blocked at transcript access.
The correct handling pattern that emerged was:
- do **not** speculate
- create minimal Stage 1 evidence pack
- mark hold/partial status
- preserve numbering continuity

### 4) Reissue handling
When a batch was reissued, the correct practice was:
- keep the same batch number
- keep content scope unchanged
- regenerate files/zip cleanly
- resend the exact PowerShell sorter block

## Lessons Learned
The strongest workflow lessons across the range were:

1. Stage 1 works best when it remains narrow.
2. It is better to export a compact, structured evidence pack than to over-summarize or drift toward synthesis.
3. Inaccessible transcript material should be held, not invented.
4. Formatting matters operationally because these outputs are being downloaded, unzipped, and sorted into a real workspace.
5. Optional files should stay evidence-driven, not template-driven.
6. Reissues should preserve numbering and scope.
7. Cross-batch duplication is high enough that later range-level tracking is necessary.

## Recommended Continuation Rule
The next intake GPT should continue using the same workflow, not invent a new one.
