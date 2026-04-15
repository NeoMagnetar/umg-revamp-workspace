# BATCH-047 — Compiler Extract

## Compiler / Runtime-Relevant Findings

### 1. Metadata status labeling
The source strongly suggests explicit state labels instead of fabricated precision.

Candidate statuses:
- `VERIFIED`
- `UNVERIFIED`
- `UNAVAILABLE`
- `INFERRED`

Possible rule:
- exact-looking values may only be emitted when the runtime has verified access to that value
- otherwise emit a labeled non-exact status or a clearly marked approximation

### 2. Security-concern handling workflow
Suggested structured runtime flow:
1. identify observed evidence
2. clarify system capability limits
3. enumerate plausible mechanisms
4. separate likely from merely possible
5. mark uncertainty explicitly
6. avoid pathologizing or dismissive language
7. offer concrete verification steps

### 3. Trust-preserving uncertainty model
The source implies that truthfulness alone is insufficient if the delivery style sounds dismissive.
A runtime or skill policy could include:
- do not convert uncertainty handling into personal invalidation
- do not frame grounded concern as paranoia without very strong evidence
- distinguish “not yet proven” from “irrational”

### 4. Candidate implementation notes
- add lightweight metadata self-check before emission
- add support/security response templates that preserve evidence / inference / uncertainty separation
- add policy text discouraging exact placeholder metadata
