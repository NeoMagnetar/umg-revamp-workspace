# BATCH-174 — Update block library — Review

## Source Snapshot
Source type: pasted chat summary  
Scope: Bolt-based builder rebuild focused on a starter website block library organized by MOLT type  
Evidence status: Stage 1 intake only; not canon

## Faithful Source Summary
This batch focused on rebuilding a broken Bolt-based UMG website/block-builder scaffold. The concrete target was a block library organized first by MOLT type and then by selectable blocks within each type. The implementation direction moved from a minimal Vite/React/TypeScript template toward a drag/drop canvas prototype using a block palette and a drop area. The work repeatedly ran into Bolt terminal/file-write limitations, especially around shell redirection and heredoc-style paste flows.

## UMG-Relevant Extraction
### Stable signal
- MOLT types are used here as first-class organizational shelves for a builder library.
- The builder is split into:
  - definition layer (`blockLibrary.ts`)
  - palette UI (`BlockPalette.tsx`)
  - placement/runtime surface (`Canvas.tsx`)
  - app wiring (`App.tsx`)
- A concrete starter data model appears:
  - `MOLTType`
  - `BlockMeta`
  - `Record<MOLTType, BlockMeta[]>`
- The MVP target is intentionally small and practical:
  - website-oriented starter blocks
  - at least 10 blocks per MOLT category
  - drag from palette, drop onto canvas, render placeholders

### Source-justified category signal
- Primary, Subject, Instruction, Philosophy, and Directive are the operative categories for this builder pass.
- The block inventory is implementation-starter content for web building, not full UMG canon.
- The runtime behavior in this batch is shallow by design:
  - local placed state
  - placeholder rendering
  - no nesting
  - no inspector
  - no serialization/export engine
  - no full semantic renderers yet

## Independent Review
This batch is useful evidence for translating UMG into a practical authoring interface. Its strongest contribution is not theoretical semantics but UI structure: category-first block browsing, clean separation between definitions and UI/runtime layers, and a low-complexity path to a functioning builder prototype.

The taxonomy here should remain scoped to the website-builder MVP. The five categories are treated as operational for this implementation pass, but the source does not prove that this is the complete or final category set for broader UMG use. The starter blocks are workable inventory examples rather than canon-level ontology.

The environment constraint is important evidence. Bolt terminal behavior materially affects how code updates can be delivered. That means future builder workflow should preserve editor-safe or terminal-safe update paths rather than assuming full shell capabilities.

## Roadmap Mapping
### Phase 1 — Core Alignment
- Moderate relevance:
  - category names are being used operationally
  - not enough evidence here to finalize broader taxonomy

### Phase 2 — Compiler Impact
- Moderate relevance:
  - runtime path from palette to canvas is explicitly modeled
  - future renderer mapping by block id is implied

### Phase 3 — Documentation Impact
- Strong relevance:
  - builder taxonomy
  - minimum library scope
  - separation of definition layer from UI/runtime layer

### Phase 4 — Skill Alignment
- Moderate relevance:
  - builder update workflows need platform-aware delivery methods
  - terminal-safe/editor-safe workflows matter

### Phase 5 — PRD and Staging
- Strong relevance:
  - MVP scope is concrete
  - 10 starter blocks per category is a usable staging requirement

## Disposition
ACCEPT_AS_EVIDENCE

## Optional Extract Rationale
Included:
- Blocks/MOLT extract
- NeoStructure extract
- Compiler extract
- Canon candidates

Not included:
- Sleeve extract
- Contradiction flags

Reason:
This source materially defines builder taxonomy, layered builder structure, runtime interaction basics, and reusable requirement language. It does not materially develop sleeve behavior or direct cross-source contradictions.
