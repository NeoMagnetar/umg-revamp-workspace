# BATCH-193 - Compiler Extract

## Scope
Compiler- and runtime-facing implications extracted from the block-system source.

## High-Value Compiler Claims
1. Arbitrary imported information should be compilable into a new fully labeled block.
2. Candidate compile pathways in the source include:
   - drag text/JSON/image onto the canvas
   - parse content
   - suggest MOLT type and label
   - create full block
3. Other authoring inputs proposed:
   - clipboard-to-block
   - OCR/screenshot-to-block
   - AI-assisted natural-language block generation
4. The source suggests loading block JSON into a central state store and driving both library and canvas from that store.
5. Validation/runtime interactions proposed include:
   - snap ports
   - compatibility checking
   - connection validation
   - merge diff modal
   - history/timeline scrubber
   - live code probe

## Likely Compiler Audit Targets
- canonical builder block schema
- import-to-block pipeline rules
- allowed auto-inference scope
- state-store contract for block library/canvas
- merge behavior in the editor
- schema-lint and validation surfaces
