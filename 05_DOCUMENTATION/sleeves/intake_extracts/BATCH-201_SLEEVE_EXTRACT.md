# BATCH-201 — Sleeve Extract

## Scope
This extract captures the sleeve/stack separation emerging in the repo.

## Sleeve Split
- `/poe_core/sleeves/` = embedded or runtime-core sleeves
- `/sleeves/` = user-facing stack bundles and templates

## Example Files Mentioned
- `poe_core/sleeves/coder.sleeve.json`
- `poe_core/sleeves/stock_broker_sleeve.block.json`
- `sleeves/Poe/NeoPoeUMG.API.stack.json`
- `sleeves/Poe/NeoPoeUMG.StockBroker.stack.json`
- `sleeves/BusinessPlan.stack.json`
- `sleeves/Chatbot.stack.json`

## Sleeve Reading
The split is treated as meaningful rather than erroneous:
- runtime/core sleeves
- gallery/library/user-facing plan stacks

## Resleeving Pressure
Resleeving here is implicit in the movement of templates into a clearer `sleeves/` hierarchy and the sharper distinction between runtime embedded sleeves and user-facing stack libraries.

## Project Relevance
Useful for:
- sleeve docs
- builder library design
- runtime vs gallery separation
- Poe integration architecture
