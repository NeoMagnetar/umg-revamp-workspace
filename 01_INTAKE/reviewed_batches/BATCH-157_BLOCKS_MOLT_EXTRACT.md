# BATCH-157 — Blocks / MOLT Extract

## Role Mapping Signal
The source uses MOLT-adjacent role language to explain how UMG can wrap HRM without changing UMG’s identity.

## Candidate Role Mapping
- **Directive / Blueprint** → planning / route selection
- **Primary / Subject** → execution surface
- **Verifier** → post-execution checking, majority-vote, self-consistency, and bounded retry decision

## Candidate Call Flow
1. Directive / Blueprint chooses the route
2. Primary / Subject executes the selected wrapped solver
3. Verifier evaluates confidence, votes, and audit signal

## Block-Level Composition Signal
- proposed wrapped unit name: `hrm.solver`
- candidate wrapper artifacts:
  - `hrm_cli.py`
  - `hrm.config.json`
  - `adapter.ts`
- candidate metadata:
  - `name = hrm.solver`
  - `molt_type = PRIMARY`
  - `tags = solver / arc / puzzle`
  - `entrypoint = hrm_cli.py`

## Normalization Notes
- The source uses block, nCube, and solver module around the same concept.
- Canonical normalization is still required before downstream documentation or implementation hardening.
