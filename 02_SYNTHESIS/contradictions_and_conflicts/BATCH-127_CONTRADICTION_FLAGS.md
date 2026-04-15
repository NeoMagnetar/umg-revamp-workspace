# BATCH-127 — Contradiction Flags

## Scope Note
These are not canon decisions.
They are tensions or possible conflicts surfaced by the source.

## Flag 1
**Topic:** Packaging layer confusion  
**Tension:** The source notes repeated confusion among workspace root package, compiler package, README surface, and GitHub repo settings.  
**Why it matters:** Later release templates should not assume this layer separation is already normalized everywhere.

## Flag 2
**Topic:** Naming drift before stabilization  
**Tension:** Multiple names were considered before settling on UMG Compiler / `umg-compiler` / `umg`.  
**Why it matters:** Older notes or repos may still contain alternative names, creating duplicate pressure and documentation mismatch.

## Flag 3
**Topic:** Canonical implementation wording  
**Tension:** The source frames the compiler as the first canonical implementation, but Stage 1 should preserve this as evidence rather than finalized canon.  
**Why it matters:** This claim should later be verified against official repo state and canon language.

## Flag 4
**Topic:** Future umbrella CLI scope  
**Tension:** The chat keeps CLI scope intentionally minimal for v0.1.0 while also hinting at broader future command surfaces.  
**Why it matters:** Future expansion should not silently change the compiler’s bounded identity.

## Flag 5
**Topic:** Markdown portability as workflow constraint  
**Tension:** Documentation correctness alone was not enough; portability in the user’s actual workflow changed formatting decisions.  
**Why it matters:** Release/document templates may need delivery-format rules in addition to semantic rules.
