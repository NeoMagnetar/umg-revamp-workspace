# BATCH-180 — Definitions Extract

## Terminology Scope Note
These definitions are extracted from a derived deployment-workflow summary.
They remain Stage 1 evidence until explicitly promoted elsewhere.

## Core Artifact Terms
**Grouped JSON Bundle**  
One downloadable JSON file containing many full block objects intended for later unpacking into individual block files.

**Row-Level Blockification**  
Generation rule in which each intended row or listed item becomes its own block object rather than being collapsed into a category summary.

**Artifact Contract**  
The fixed practical agreement about what shape a generated file must take in order to be accepted by downstream tooling.

**Unpack Flow**  
Terminal workflow in which the grouped JSON file is passed to `python scripts/unpack_blocks.py <filename>.json` for importer-side decomposition.

## Runtime Terms
**Importer-Compatible Block List**  
A JSON array of full block objects that the unpack script can validate and write to MOLT-based directories.

**Filename Discipline**  
Requirement that the downloadable file name exactly match the surfaced unpack command and remain stable enough for VS Code/terminal use.

## Definitional Candidates
One grouped JSON file should contain a list of full block objects, not strings or category summaries.  
Each intended row/item must become its own block when the agreed pattern is row-level blockification.  
No alternate packaging mode unless explicitly requested.
