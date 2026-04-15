# BATCH-116 — Compiler / Process Extract

## Process Contribution
This batch contributes process logic rather than a narrow compiler rule. Its strongest signal is a deterministic fallback path for producing usable inventory artifacts when a connector cannot enumerate content.

## Candidate pipeline
1. Acquire source inventory
   - copy/paste list view
   - scripted export
   - screenshot transcription
2. Normalize
   - remove noise
   - dedupe filenames
   - preserve source notes
3. Validate
   - confirm folder/source name
   - check for truncation or missing rows
4. Persist
   - produce canonical inventory artifact
   - record acquisition method

## Candidate task concept
- **Inventory Artifact Generator**
  - Input: pasted list, screenshot transcription, or script output
  - Output: cleaned canonical file inventory
  - Purpose: deterministic artifact production when direct connector enumeration is unavailable

## Documentation pressure
- Define enabled vs authorized vs attached vs enumerable.
- Separate governance restrictions from connector capability limitations.
- Preserve evidence path for user-mediated inventory generation.

## Risk signal
- Misclassifying tool-surface limits as governance rules can create false canon and mislead later workflow design.
