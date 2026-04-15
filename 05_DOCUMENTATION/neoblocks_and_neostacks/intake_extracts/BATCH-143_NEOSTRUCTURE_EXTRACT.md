# BATCH-143 — NeoStructure Extract

## Scope
Block and stack architecture material extracted from the ETL translation source.

## Candidate Block Families
- `SourceBlock`
- `TransformBlock`
- `LogicBlock`
- `DataFlowBlock`
- `ExportBlock`

## Expanded Operator Equivalence Examples
- Add Constants → `logic.addDefaults()`
- Alter Columns → `transform.modifyColumns()`
- Set Column Value → `logic.deriveColumn()`
- Value Mapper → `logic.mapValues()`
- Select Columns → `transform.pick()`
- Add Formula → `logic.compute()`
- Filter Rows → `logic.filter()`
- Remove Duplicates → `logic.deduplicate()`
- Join Data → `logic.join()`
- Group By → `logic.groupBy()`
- Pivot → `transform.pivot()`
- Unpivot → `transform.unpivot()`
- Rank & Window → `logic.rankWindow()`

## Layer Taxonomy
- Ingest Layer
- Sanitize Layer
- Logic/Value Layer
- Structure Layer
- Join & Merge Layer
- Export Layer
- Optional Feedback Loop & Automation Layer

## Domain Extension Stack Signal
Trading extension added candidate blocks:
- `MarketDataBlock`
- `SignalDetectionBlock`
- `StrategyBlock`
- `AlertBlock`
- `PortfolioSimulatorBlock`
- `ExecutionBlock`

## Structure Notes
The source is especially valuable for showing how a generic layered workflow architecture can accept domain-specific stack extensions without losing modularity.
