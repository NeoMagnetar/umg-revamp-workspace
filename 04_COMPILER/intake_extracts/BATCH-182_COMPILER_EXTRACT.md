# BATCH-182 - Compiler Extract

## Scope
Compiler- and runtime-facing implications extracted from the Builder repair-plan source.

## High-Value Compiler Claims
1. The Builder runtime can remain file-based and database-free.
2. Global runtime rule maps include:
   - snapMatrix.json
   - mergeMatrix.json
3. Local runtime utilities include:
   - update_stack_logic.py
   - autopopulate_stack.py
   - validate_manifest_refs.py
4. Manifest files should live at `/apps/umg-builder-web/manifests/`.
5. Manifest structure is flat JSON keyed by MOLT type, with array order representing stack order.
6. Runtime behavior depends on both:
   - per-block metadata
   - matrix-level global rules
7. Plan validation, merge previews, rebuild stack, runtime event logging, snapshot restore, and deploy hooks are all preserved as implementation-facing runtime concerns.

## Likely Compiler Audit Targets
- Builder-specific manifest schema
- matrix-file maintenance policy
- stack-priority injection rules
- block reference validation policy
- Builder-specific runtime event handling
- clear separation between Builder runtime docs and framework canon docs
