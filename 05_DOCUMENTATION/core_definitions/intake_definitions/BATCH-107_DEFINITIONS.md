# BATCH-107 — Definitions Extract

## Role / Taxonomy Definitions
- **Primary** — core or main objective block.
- **Subject** — subject matter or content-space context.
- **Instruction** — behavior, rule, or process guidance.
- **Directive** — emphasis, steering, or control logic.
- **Philosophy** — worldview, framework, ethics, or tone-governing logic.
- **Blueprint** — layout, rendering, format, or structure logic.
- **Merge** — content/logic intended to blend into another stack or prompt.
- **Trigger** — event or activation logic; semantically distinct from code payload.
- **CodeBlock** — block whose primary payload is executable or markup code.
- **Off** — disabled or catch role.
- **Deployment** — legacy/problematic pseudo-role; operationally normalized to Instruction in this chat but explicitly questioned by the user.

## Schema / Composition Terms
- **block** — modular unit carrying structured metadata plus usable content for builder assembly.
- **cantocore** — compact DSL/signature for self-identification and merge/snap hints, not the whole content model.
- **prompt_template** — one allowed content shape in the working strict schema.
- **body** — second allowed content shape in the working strict schema.
- **code_modules** — optional attached code payloads such as HTML/CSS/JS/shell, distinct from semantic role.
- **display** — builder-facing UI metadata cluster; `color` and `icon` treated as essential.
- **snap_config** — builder/runtime metadata for stacking and attachment behavior.
- **merge_behavior** — required merge object controlling blend/composition behavior.
- **editable_fields** — normalized as an array of strings in the working strict schema.

## Builder / Runtime Terms
- **Block Builder** — stack-based system expected to browse by category/subcategory/domain while snapping and merging by MOLT role.
- **schema-clean blocks** — blocks that pass validation and are safe for reorg and builder/runtime use.
- **preview-first safe reorg** — confirm-first workflow before destructive folder moves or git operations.
- **CI validation** — validation step intended to prevent future drift automatically.

## Candidate Schema Notes
- **Schema v1.0** — strict schema without `domain`.
- **Schema v2.0** — later proposal adding required `domain`.
- **additionalProperties: false** — strict language indicating legacy keys must be removed rather than tolerated.
- **oneOf(prompt_template | body)** — strong content-shape rule in the source.

## Migration / Cleanup Definitions
- **legacy fields to remove** — `ledger`, `canto_overlay`, `stack_priority`, `merge_logic`, `merge_origin`, `example_block_data`, `runtime_behavior_flags`, `integration_layer`, `agent_orchestration`, `future_extensions`.
- **normalization examples** —
  - `content` → `body`
  - `code_modules[].path` → `code`
  - `Deployment` → `Instruction` (provisional operational fix only)
