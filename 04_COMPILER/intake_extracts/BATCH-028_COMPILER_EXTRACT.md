# BATCH-028 — Compiler Extract

## Compiler-Relevant Findings
- Draft/random trigger IDs are treated as a flaw when canonical trigger blocks already exist.
- NeoBlocks should reference canonical MOLT IDs already present in project files.
- Compiler/tooling compatibility depends on reliable block resolution and normalization.
- Runtime flow is described as explicit staged logic, not freeform drafting.

## Candidate Compiler Tasks
1. validate neostack specs against canonical MOLT ID inventory before compile
2. replace draft/random trigger numbering with canonical block references
3. add normalization checks for identifier format drift such as `NST.` vs `NSTK.`
4. preserve route trace structure:
   - Trigger
   - Neostack
   - Directive
   - Instruction
   - Execution
   - Verify
   - Report
5. require stack-entry model binding metadata where applicable

## Confidence
- **Medium**
- Strong as architectural/refinement evidence.
- Limited because the batch does not perform the concrete substitutions itself.

## Hold Notes
- Do not treat this extract as proof of the final canonical ID scheme.
- Cross-check against the actual block inventory before any compiler-spec promotion.
