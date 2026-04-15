# BATCH-144 — Definitions Extract

## Terminology Scope Note
These definitions are extracted from a derived builder-serialization summary.
They remain Stage 1 evidence until explicitly promoted elsewhere.

## Core Pipeline Terms
**Category → Block List → JSON → Zip**  
Repeatable serialization pipeline in which domain categories are expressed as block sets, instantiated into JSON files, and bundled into master zip artifacts.

**Category Layer**  
Functional domain grouping such as persona, tone, memory, safety, tools, UI, or control.

**Block**  
Atomic configuration unit defining behavior, interface, logic, or constraints inside a category.

**JSON Instantiation**  
Portable configuration form of a category block set.

**System Bundle**  
Zip-packaged collection of category JSON artifacts representing a deployable or shareable system state.

## Runtime Control Terms
**Instruction Injection**  
Runtime override or modification layer supporting temporary instructions, append/override behavior, and return-to-base triggers.

**Persona Switching**  
Runtime resleeving mechanism that changes identity configuration and may use shared or isolated memory policies.

**Token Governance**  
Usage-limit control layer that constrains cost, token budgets, or hard-stop behaviors.

## Definitional Candidates
Category → Block List → JSON → Zip.  
Blueprint → JSON → UI/deployment.  
Control, Safety & Expansion as final layer.  
Serialized NeoStack instance.
