# BATCH-143 — Definitions Extract

## Terminology Scope Note
These definitions are extracted from a derived workflow-translation summary.
They remain Stage 1 evidence until explicitly promoted elsewhere.

## Core Translation Terms
**Layered Blueprint**  
Ordered modular decomposition of a workflow into functional layers such as ingest, sanitize, logic/value, structure, join/merge, export, and optional automation.

**Modular Upgrade Pattern**  
Approach in which a fixed visual or recipe-like workflow is translated into reusable, upgradeable logic modules.

**Treat ETL as an App**  
Design shift that frames a data workflow as reusable, forkable, interactive, and versionable rather than as a single static pipeline.

**Flow-to-Code Converter**  
Proposed tool that transforms source workflow representations such as screenshots or configs into modular UMG JSON, JSX, or equivalent logic representations.

## Operator/Block Terms
**SourceBlock**  
Candidate block type for ingest/data-source steps.

**TransformBlock**  
Candidate block family for reshaping or column-level structural changes.

**LogicBlock**  
Candidate block family for filters, derivations, mappings, rankings, joins, and related transformations.

**ExportBlock**  
Candidate block type for final output targets.

## Definitional Candidates
Layered Blueprint.  
Modular upgrade pattern.  
Treat ETL as an app.  
Versioned UMG blocks.  
Forkable and interactive.
