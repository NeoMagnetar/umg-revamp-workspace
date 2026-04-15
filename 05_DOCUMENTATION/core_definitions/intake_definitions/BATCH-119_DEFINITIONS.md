# BATCH-119_DEFINITIONS

## v0 Definition Extract
- **UMG:** framework for constructing, composing, and resolving cognitive processes as modular, non-executing specification artifacts independent of execution.
- **CSL:** pre-runtime, non-executing jurisdiction where cognitive intent, structure, constraints, and priorities are specified, resolved, versioned, and inspected prior to execution.
- **MOLT:** formal language used to specify cognitive structure, reasoning posture, constraints, and priorities as composable specification elements independent of execution.
- **Cognitive Block:** atomic declarative unit of cognitive specification.
- **Block Stack:** ordered composition of cognitive blocks forming a resolved cognitive dimension with defined precedence.
- **NeoBlock:** synthesized cognitive block produced through the combination of multiple cognitive blocks or block stacks into a higher-order cognitive specification artifact.
- **NeoStack:** ordered composition of NeoBlocks representing a multi-dimensional cognitive specification structure.
- **Governance Layer:** pre-runtime, non-executing authority layer able to veto, disable, prefer, limit, or reprioritize cognitive elements during compilation.
- **RuntimeSpec:** executor-facing bounded artifact produced after compilation.
- **Trace:** audit artifact containing events, warnings, links, and decisions from compilation.
- **CompileResult:** final contract returning runtime when valid, trace always, and hasErrors boolean.

## v0 MOLT Types
- trigger
- directive
- instruction
- subject
- primary
- philosophy
- blueprint

## Block Schema Elements Extracted
- id
- moltType
- optional role
- optional priorityOrder
- content
- optional tags

## BlockRole Values Extracted
- primary_shell
- merge_contributor
- blueprint_guide
- off

## Trigger Elements Extracted
- Trigger = named switch, not code
- TriggerKind:
  - manual
  - input_pattern
  - external_signal
- Trigger schema fields:
  - id
  - name
  - description
  - kind
  - optional pattern
  - optional signalKey
- TriggerState:
  - activeTriggerIds

## Governance Elements Extracted
- effects:
  - forbid
  - require
  - prefer
  - limit
  - override_priority
- severity:
  - hard
  - soft

## Output Artifact Fields Extracted
- **RuntimeSpec locked v0 fields:**
  - sleeveId
  - sleeveName optional
  - primary
  - triggers
  - triggersBlocks
  - directives
  - instructions
  - subjects
  - philosophy
  - blueprints
  - primaries
  - bundles
  - merges
  - governanceRules
  - appliedGovernance
  - meta optional
- **Trace locked v0 structure:**
  - TraceEvent with id, type, severity, optional code, message
  - contextual links to blocks, bundles, merges, governance rules, triggers
  - Trace with sleeveId and events
