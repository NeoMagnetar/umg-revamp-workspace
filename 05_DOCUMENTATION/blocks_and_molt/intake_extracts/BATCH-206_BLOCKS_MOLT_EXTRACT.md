# BATCH-206 — Blocks / Runtime Objects Extract

## Scope
This extract captures runtime-object composition and role-bearing block language.

## Canonical Runtime Objects
- Block
- Stack
- Sleeve

## Block Schema Pressure
Fields described include:
- block_id
- type
- content
- priority
- tags
- mutable
- dependencies
- conflicts
- author
- created_at
- checksum

## Example Block IDs
- NB.PHILOSOPHY.ART_OF_WAR.v1
- NB.INSTRUCTION.STRUCTURED_OUTPUT.v2
- NB.POLICY.NO_NETWORK_WRITE.v1

## Block Categories Mentioned
- philosophy
- instruction
- policy
- tool
- constraint
- style
- memory
- validation
- budget
- epistemic

## Stability Notes
This batch is less about classical MOLT type locking and more about runtime object formalization. It is strongest where blocks are treated as persistent, versioned, provenance-aware runtime units.

## Project Relevance
Useful for:
- runtime object schema docs
- provenance requirements
- policy/tool/budget block treatment
- storage and validation planning
