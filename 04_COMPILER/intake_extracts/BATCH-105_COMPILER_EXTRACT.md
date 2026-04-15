# BATCH-105_COMPILER_EXTRACT

## Scope
Compiler/runtime-relevant signals extracted from BATCH-105.

## High-Signal Candidates

### 1. Pre-runtime validation as required gate
The batch strongly implies that invalid blocks must be detected before runtime use.

Compiler/runtime consequences:
- add repository validation before build/run
- surface both parse failures and schema failures
- fail fast on structurally invalid blocks
- separate audit reporting from mutation/remediation

### 2. Strict validator plus loose checker workflow
The source introduces both Ajv-based strict validation and a looser checker.

Implementation pressure:
- support strict schema conformance reports
- support heuristic drift scans for legacy repositories
- distinguish canonical failures from compatibility warnings
- make reports legible enough for batch remediation

### 3. Migration versus schema-relaxation decision
Two remediation paths are discussed:
- update schema
- migrate blocks

Compiler consequences:
- decide whether canonical import normalizes legacy fields
- define migration transforms for known mismatches
- support version-aware upgrades if schema_version is present
- document what counts as tolerated legacy structure versus blocked structure

### 4. Canonical field normalization
The packet highlights recurring field issues:
- `content` type mismatch
- unexpected fields such as `color`
- possible disallowed or misplaced `merge_logic`

Implementation pressure:
- normalize content shape where policy allows
- explicitly whitelist or reject extension fields
- preserve ledger/provenance during migration
- avoid silently mutating semantics while repairing structure

### 5. Non-mutating scanner behavior
The scanner is explicitly observational.

Runtime/staging consequences:
- preserve human-in-the-loop review before mutation
- separate scan, migrate, and revalidate as distinct stages
- support report generation for assistant analysis or commit gates
- avoid conflating utility-memory cards with executable scripts

## Suggested Audit Angles
- formalize scan → validate → migrate → revalidate pipeline
- define strict versus compatibility validation modes
- settle canonical field list and allowed extension policy
- document schema_version handling and upgrade pathways
- preserve a clean boundary between executable utilities and CyentCore memory representation

## Confidence
High for workflow relevance, medium for final policy implications.
The batch is concrete about failure modes and tooling needs, but does not settle the canonical schema strategy.
