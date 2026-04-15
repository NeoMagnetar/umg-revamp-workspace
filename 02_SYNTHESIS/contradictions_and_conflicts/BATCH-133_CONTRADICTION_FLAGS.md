# BATCH-133 — Contradiction Flags

## Scope Note
These are not canon decisions.
They are tensions or possible conflicts surfaced by the source.

## Flag 1
**Topic:** Code role vocabulary mismatch  
**Tension:** The visible code role list includes `annotation` and omits some preferred role names seen elsewhere.  
**Why it matters:** Documentation and canon alignment cannot assume code vocabulary is already normalized.

## Flag 2
**Topic:** Governance effect surface versus visible enforcement  
**Tension:** The type surface includes effects such as `override_priority` and `limit`, but visible excerpts do not fully demonstrate their full runtime behavior.  
**Why it matters:** Audit and documentation should distinguish typed capability from fully verified behavior.

## Flag 3
**Topic:** LangChain integration layer scope  
**Tension:** Prompt-layer integration, Runnable integration, and full governed-tools lab were all proposed as staged options.  
**Why it matters:** Product and implementation planning need one concrete initial integration boundary.

## Flag 4
**Topic:** Runtime extension proposals versus current schema  
**Tension:** Proposed tool-governance and routing extensions were suggestions, not confirmed compiler schema in the exposed files.  
**Why it matters:** Adapter-layer proposals should not be mistaken for present-core contracts.

## Flag 5
**Topic:** prefer.boost-derived priority behavior  
**Tension:** Contract checking derives numeric-style priority effects from `prefer.boost`, which may not cover the full intended governance semantics.  
**Why it matters:** Governance and priority documentation may need a narrower or more explicit statement.

## Flag 6
**Topic:** Philosophy handling  
**Tension:** Multiple philosophy blocks remain active with warning rather than undergoing winner selection.  
**Why it matters:** This behavior should be documented explicitly so readers do not assume all MOLT lanes behave like primary selection.
