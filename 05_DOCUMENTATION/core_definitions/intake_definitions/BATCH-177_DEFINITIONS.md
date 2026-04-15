# BATCH-177 — Definitions Extract

## Terminology Scope Note
These definitions are extracted from a derived repo-agent and schema-design summary.
They remain Stage 1 evidence until explicitly promoted elsewhere.

## Core Terms
**Cantocore**  
Condensed language logic intended for visible human-to-agent structured communication.

**Cyentocore**  
Remembered as a more compressed internal system language for system-to-system use when no user-facing output is needed.

**NeoCore Modular Block Schema**  
Rich JSON block schema supporting recursive block composition, metadata, merge behavior, trigger behavior, snapping, stack grouping, provenance, and code modules.

**Minimal Everyday Block**  
Lightweight block format intended for fast daily use, carrying only essential identity and body fields rather than full production metadata.

## Runtime Terms
**Schema-Aware Poe Runtime**  
Agent behavior pattern in which Poe loads a repo schema file, validates rich blocks, interprets natural language, asks for missing parameters, and acts in the repo/codespace.

**Clarification Fallback**  
Interaction rule in which the agent prompts the user when required parameters are missing rather than acting blindly.

## Definitional Candidates
Not every block needs to be maximal.  
Rich canonical blocks and simple utility blocks may need distinct handling paths.  
Cantocore needs a master key.  
Repo-operable agents need both schema validation and natural-language clarification.
