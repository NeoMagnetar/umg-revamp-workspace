# BATCH-093 Sleeve Extract

## Scope
Sleeve identity, project-context switching, and resleeving implications.

## Extracted Signals
- Project folders are treated as separate “instances” or modular cognition contexts.
- Different vault sets can be loaded per project.
- Identity persistence is handled through instruction embeds plus vault state.
- Resleeving is implicitly performed by changing the loaded vault set/context package.

## Practical Meaning
This batch pressures sleeve documentation toward a deployment-aware model:
- sleeve/context may not just be presentation;
- it may include loaded identity, constraints, and project-specific cognition state.

## Risks
- The source does not formalize whether “project folder = sleeve” is literal UMG architecture or just a ChatGPT Projects implementation analogy.
- Identity persistence boundaries remain partly user-managed, not system-managed.
- Resleeving language may be more metaphorical than formally specified.

## Recommended Next Decision
Determine whether sleeve/resleeving should include:
- project-context loading semantics,
- identity persistence conventions,
- vault-set switching,
or whether those remain implementation examples rather than sleeve canon.
