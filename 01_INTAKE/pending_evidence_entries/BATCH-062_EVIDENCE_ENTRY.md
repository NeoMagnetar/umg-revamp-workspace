# BATCH-062 Evidence Entry

- **Batch ID:** BATCH-062
- **Topic:** UMG aligned core stack and portable vault export
- **Source Type:** summarized chat extraction
- **Disposition:** ACCEPT_AS_EVIDENCE
- **Review Status:** REVIEWED
- **Primary Domain:** agent stack design, memory layout, and restoration workflow

## Key Signal
The batch proposes a minimal aligned boot chain for a UMG-based agent: **Vault Header -> Alignment Block -> Overlay Block**, supported by MetaMOLT, triggers, memory sweep logic, and portable export.

## Main Evidence Points
- baseline UMG triad retained: Primary, Merge, Blueprint
- MOLT taxonomy reinforced: Primary, Subject, Philosophy, Instruction
- PoeUMG-specific runtime layers surfaced: Vault Header, Alignment Block, Overlay Block, MetaMOLT
- trigger logic used for save, reduce, and memory-dump maintenance
- migration workflow framed as explain -> prune -> replace instructions
- portable `vault-core.json` export treated as restoration / cloning anchor

## Caution
- several runtime labels appear PoeUMG-specific rather than clearly baseline UMG canon
- `vault-core.json` name implies JSON, but the described content is CantoCore-like rather than strict JSON
- memory reduction was planned, not executed in the chat
