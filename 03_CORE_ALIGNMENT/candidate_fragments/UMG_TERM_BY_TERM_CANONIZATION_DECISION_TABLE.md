# UMG Term-by-Term Canonization Decision Table

## Purpose
This table translates the recent architecture and glossary review into a direct decision-oriented map for terminology cleanup.

It is not itself a final canon log.
It is a working table to support future promotion into canonical decisions.

## Legend
- **Keep** = preserve as a core term
- **Split** = preserve, but divide into separate terms or layers
- **Rename** = keep the concept, change the preferred term
- **Demote** = reduce from core canon status or stop using as a primary term
- **Canonize Now** = strong candidate for immediate stabilization
- **Clarify** = keep for now, but require narrower definition

| Term | Current Problem | Recommendation | Why | Suggested Next Action |
|---|---|---|---|---|
| CSL / Cognitive Specification Layer | Newer framing but not yet fully dominant across all legacy language | Canonize Now | Best current framing for UMG as a spec-first system rather than a vague cognitive OS | Promote into canonical decisions and top-level public framing |
| Compiler | Early translator framing and later deterministic-interpreter framing coexist | Canonize Now | Compiler is the enforcing spine and the strongest modern core of the system | Lock the current compiler contract into audit + canon records |
| RuntimeSpec | Strong later-era term but not yet visibly dominant everywhere | Canonize Now | Clean, modern, implementation-facing, and host/runtime compatible | Promote into compiler doctrine and glossary canon |
| Trace | Strong term, but can be misread as hidden chain-of-thought | Canonize Now | Excellent structural accountability concept if protected from misuse | Add trace taxonomy later and explicitly reject raw-hidden-thought interpretation |
| MOLT | Valuable core grammar but historical doctrine drift remains | Keep + Clarify | One of the strongest architectural bones in the project | Freeze exact type doctrine and publish the current canonical set |
| MOLT Block | Strong term with clear architectural use | Keep | Good typed semantic unit language | Preserve and anchor in final MOLT doctrine note |
| Merge | Historically treated as both type and operation | Demote from type-space; Keep as operation | Merge behaves more like a procedure than a native semantic kind | Record formal decision: Merge is an operation, not a MOLT type |
| Bundle | Useful but still at risk of becoming an all-purpose grouping word | Keep + Clarify | Good ordered grouping concept if kept narrow | Define Bundle against MOLT blocks, NeoBlocks, and execution chains |
| Sleeve | Overloaded across authoring, identity, runtime, and presentation | Split | Most overloaded core term in the corpus | Separate Authoring Sleeve from Active Sleeve / Runtime Shell |
| Resleeving | Powerful metaphor but too identity-heavy for strict compiler canon | Demote in core compiler doctrine; keep as optional user-facing metaphor | Useful emotionally, risky technically | Use operational runtime transition terms in canon-facing compiler docs |
| Active Sleeve | Not yet cleanly distinguished from authored sleeve | Clarify / possibly canonize after split | Needed if Sleeve remains in use | Define only after the authored/runtime split is formalized |
| Source Assets | Good current term | Keep | Clean separation from compiled and active state | Preserve in runtime/state doctrine |
| Compiled Assets | Good current term | Keep | Supports the spec/compile/runtime separation | Preserve in compiler/output doctrine |
| Active State | Good current term | Keep | Necessary runtime distinction | Preserve as part of runtime artifact model |
| Surface Persona | Good distinction when separated from architecture | Keep + Clarify | Strong protection against persona/architecture confusion | Explicitly define as presentation layer only |
| NeoBlock | Useful but not yet explicit enough in relation to MOLT blocks | Keep + Clarify | Good practical subfunction idea if staged correctly | Write one note on NeoBlock compression and downstream use |
| NeoStack | Useful but vulnerable to taxonomy sprawl | Keep + Clarify | Good middle-layer family concept if governed tightly | Define stack qualification rules |
| Stack (unqualified) | Too overloaded internally and externally | Demote | Creates confusion with software/AI stack meanings | Require qualified stack names only |
| Compiler Stack | Potentially useful qualified term | Keep if needed | Better than plain Stack | Only use when it names a real distinct layer |
| Organizational Stack | Potentially useful qualified term | Keep if needed | Helps separate family/grouping uses | Keep only with strict qualification |
| PrimaryShell | Functional but awkward and easily confused with Primary-as-type | Rename or Clarify | Concept seems useful; label is doing too much work | Revisit after role/type/output-anchor cleanup |
| Role | Frequently bleeds into type and precedence | Keep + Clarify | Essential axis, but currently too porous | Define role independently from type and precedence |
| Type | Good term but mixed historically with role/function | Keep + Clarify | Core grammar axis | Pair with a strict role/type distinction note |
| Authority / Precedence | Strong compiler-facing idea | Canonize Now | This is where the hierarchy becomes real and operational | Lock into compiler contract and hierarchy note |
| Directionality | Useful if kept in compiler or execution law, not vague philosophy | Keep + Clarify | Potentially important to ordering and legality | Define exactly where directionality participates |
| Trigger | Good operational term, especially with v0 actions-only scope | Keep | Practical runtime control concept | Preserve and constrain tightly |
| Snap | Useful but may need stronger public explanation | Keep + Clarify | Seems important to runtime choice / selection | Add one focused definition note for snap selection |
| Module | Practical human-facing container term | Keep | Better grounded than some other older metaphors | Preserve in authoring-layer docs |
| Domain | Potentially useful but can overlap with Module and Stack | Clarify | It may still be needed, but it risks taxonomy overlap | Define relationship to Module and Stack |
| Thought Unit | Potentially useful explanatory term | Keep if clearly subordinate to MOLT grammar | Can help explain atomic structure without replacing MOLT | Use as explanatory, not competing, terminology |
| Neo* vocabulary overall | Mixed value: strong internal identity, weaker public precision in places | Review case-by-case | Some terms may survive; others may not age well publicly | Run a dedicated Neo* vocabulary review later |

## Immediate canon queue
1. Canonize CSL framing.
2. Canonize compiler outputs: RuntimeSpec + Trace.
3. Freeze MOLT type doctrine.
4. Demote Merge from type-space.
5. Split Sleeve into authored vs active/runtime layers.
6. Require qualified use of Stack.

## Follow-up queue
7. Clarify NeoBlock compression.
8. Add NeoStack qualification rule.
9. Clean up PrimaryShell naming.
10. Separate role, type, precedence, and output anchor in one explicit note.

## Practical reading rule
Any future reviewer should assume that terms marked Split, Demote, or Clarify are not yet safe for loose use in canon-facing documents.
