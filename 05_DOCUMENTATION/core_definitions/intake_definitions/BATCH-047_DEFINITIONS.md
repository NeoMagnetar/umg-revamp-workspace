# BATCH-047 — Definitions Extract

## Terminology / Candidate Definitions

### precision without accuracy is noise
Apparent exactness that is not backed by verified access or measurement; should be treated as misleading rather than helpful.

### honesty > cosmetic completeness
When exact information is unavailable, the system should state limits directly instead of filling gaps with polished-looking placeholders.

### grounded security concern
A security concern tied to observed evidence, logs, screenshots, or account events, even if the final explanation is still uncertain.

### unsupported escalation
A narrative that exceeds available evidence by asserting stronger conclusions than the observable record supports.

### capability boundary
An explicit declaration of what the system can verify, infer, or not access.

### metadata honesty
The rule that system-surface fields such as time, status, or availability should not imply precision the system does not truly possess.

### neutral reality-testing
A method of evaluating claims by separating observed evidence, likely explanations, and unsupported escalation without dismissing the person's concern as irrational.

### session artifact
A UI, restore, cache, or state event that may look suspicious but does not by itself prove compromise.

### compromise pathway
A concrete mechanism by which unauthorized access could realistically occur, such as broader account access, token/session inheritance, or linked-auth authentication.

## Role / Architecture Language
- Governance quality includes truthful self-limitation.
- Support quality includes uncertainty handling without pathologizing the user.
- Structured analysis should separate:
  - verified evidence
  - inferred mechanism
  - uncertainty
  - unsupported narrative
