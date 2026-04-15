# BATCH-143 — Contradiction Flags

## Scope Note
These are not canon decisions.
They are tensions or possible conflicts surfaced by the source.

## Flag 1
**Topic:** Exploratory operator/block naming  
**Tension:** Names such as `SourceBlock`, `LogicBlock`, and `UMG.TradeFlow` are useful but were not canonized in the chat.  
**Why it matters:** Documentation should preserve them as candidate vocabulary until ratified.

## Flag 2
**Topic:** Converter concept without defined mechanics  
**Tension:** The flow-to-code converter is directionally strong, but no concrete input format, schema, or translation strategy was finalized.  
**Why it matters:** Tooling direction should not be mistaken for completed compiler design.

## Flag 3
**Topic:** ETL base versus trading extension  
**Tension:** The same modular architecture is used for both ETL and trading, but the boundary between general-purpose workflow blocks and domain-specific blocks remains open.  
**Why it matters:** Later synthesis should keep base stack and extension layers distinguishable.

## Flag 4
**Topic:** Execution boundedness  
**Tension:** Trading execution is marked optional and cautioned with SafeMode/dry-run ideas, but no broader governance/control model is defined here.  
**Why it matters:** Higher-risk action layers need stronger boundedness than this chat alone provides.

## Flag 5
**Topic:** Stylized language versus extractable structure  
**Tension:** Some phrasing in the original discussion was highly stylized.  
**Why it matters:** Only the structural and logical content should be treated as durable evidence.
