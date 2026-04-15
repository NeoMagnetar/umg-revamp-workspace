# BATCH-116 — Definitions Extract

## Governance terms
- **Governance restricts participation only**  
  Governance acts by permitting or excluding participation; it should not be inferred from ordinary connector/tool failure.
- **OFF is absolute**  
  OFF remains the explicit exclusion mechanism relevant to participation blocking.
- **No implicit blocking without explicit exclusion**  
  The source supports an evidence standard: connector failure alone does not prove governance exclusion.

## Connector/tool-surface terms
- **Enabled**  
  Visible or switched on in the UI; does not guarantee in-session enumeration capability.
- **Authorized**  
  Permission scope exists for the connector or source.
- **Attached / Selected**  
  A specific source or file has been actively brought into the current chat context.
- **Enumerable**  
  Folder or source contents can be listed directly by the active tool surface.

## Workflow terms
- **Inventory artifact**  
  A normalized file-list artifact derived from pasted content, scripted export, or screenshot transcription when direct enumeration is unavailable.
- **Artifact fallback protocol**  
  A standard user-mediated path for producing inventory data when connectors cannot enumerate directly.

## Source-faithful implications
- Governance and connector capability are distinct categories.
- Connector enabled does not imply enumeration permitted.
- User-provided listings are valid fallback artifacts when direct enumeration fails.
