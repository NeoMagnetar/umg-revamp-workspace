# BATCH-132 — Contradiction Flags

## Scope Note
These are not canon decisions.
They are tensions or possible conflicts surfaced by the source.

## Flag 1
**Topic:** Compile-only versus live generation dependency  
**Tension:** The batch argues UMG can and should be useful publicly even without live generation, while the current working generator already depends on live model output for much of its visible magic.  
**Why it matters:** Product framing should not promise one mode while implementation still assumes another.

## Flag 2
**Topic:** Serializer concept without locked contract  
**Tension:** A deterministic serializer is central to the framing, but no exact contract is specified here.  
**Why it matters:** The project needs to avoid rhetorical certainty outrunning implementation clarity.

## Flag 3
**Topic:** Business model ambiguity  
**Tension:** BYOK, quota, credits, and hybrid access were all presented as viable.  
**Why it matters:** Release planning needs one concrete initial model even if the long-term path stays open.

## Flag 4
**Topic:** Governance demo without locked exemplar  
**Tension:** Governance-conflict demonstration is proposed as a signature showcase, but no final scenario or rule set is defined here.  
**Why it matters:** Public demo value depends on a concrete, repeatable example rather than an abstract promise.

## Flag 5
**Topic:** Cache and replay behavior  
**Tension:** RuntimeSpec-hash caching and replay were proposed, but cache invalidation, visibility, and allowed variance were not defined.  
**Why it matters:** Runtime convenience features can introduce confusion if not bounded carefully.

## Flag 6
**Topic:** Shareable sleeve/compiled artifact packaging  
**Tension:** Sharing compiled results was suggested, but no portable schema or privacy boundary was locked in this chat.  
**Why it matters:** Public-sharing features need explicit artifact and exposure rules.
