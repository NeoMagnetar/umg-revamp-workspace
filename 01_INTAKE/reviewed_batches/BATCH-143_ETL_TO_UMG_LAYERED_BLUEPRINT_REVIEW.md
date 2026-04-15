# BATCH-143 — ETL to UMG Layered Blueprint Review

## Batch Overview
Batch ID: BATCH-143  
Source Type: derived summary / visual-ETL-to-UMG translation and domain-stack extension consolidation  
Working Topic: Domo-style ETL mapping into modular UMG blocks, layered blueprint, operator equivalence, flow-to-code conversion, trading-stack extension  
Review Status: REVIEWED  
Disposition: ACCEPT_AS_EVIDENCE

## Source Snapshot
The source is a structured consolidation of a chat that mapped a visual Domo-style ETL workflow into a modular UMG-style architecture.
The discussion first translated ETL nodes into reusable block/operator equivalents and organized them into a layered blueprint:
ingest,
sanitize,
logic/value,
structure,
join/merge,
export,
plus optional feedback/automation.
A second image expanded the operator mapping to include joins, grouping, pivoting, unpivoting, and rank/window logic.
The conversation then extended the same modular/layered approach into a stock-trading-oriented stack with market, signal, strategy, alert, simulation, and optional execution blocks.
Because the source is a derived summary rather than a locked implementation or canon spec, it should be treated as strong evidence of translation architecture, layered block taxonomy, and app/tool design direction, but not as automatic canon.

## Chat-Level Summary
This batch is strongest as a practical translation pattern:
take an existing visual workflow and reframe it as reusable UMG logic.
Its central contribution is the layered blueprint.

Instead of treating a Domo flow as a fixed visual recipe, the chat treats it as a reusable, upgradeable modular system.
That is the main semantic move:
treat ETL as an app.

The source also contributes a clear rendering/logic separation:
the visual ETL interface is the source surface,
while the UMG representation is the modular logical target.
This is reinforced by the proposed flow-to-code converter and the idea of a drag-and-drop surface backed by code or logic modules.

The trading extension is also useful because it demonstrates how a general ETL base can be extended into a more domain-specific stack without abandoning the same layered modular logic.

## UMG-Relevant Extraction
The total logic flow is repeatedly summarized as staged transformation:
input,
sanitize,
derive,
structure refinement,
advanced logic,
output.

The source explicitly frames ETL as a “modular upgrade pattern.”
It also uses phrases such as:
- layered blueprint
- modular logic blocks
- treat ETL as an app
- forkable and interactive
- versioned UMG blocks

The block/operator family introduced in the source includes candidate types such as:
- `SourceBlock`
- `TransformBlock`
- `LogicBlock`
- `DataFlowBlock`
- `ExportBlock`

Later operator mappings add more concrete reusable equivalents:
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

The source also presents a strong layer taxonomy:
- Ingest Layer
- Sanitize Layer
- Logic/Value Layer
- Structure Layer
- Join & Merge Layer
- Export Layer
- Optional Feedback Loop & Automation Layer

A concrete schedule-style automation example appears:
`automation.schedule('daily', finalStep);`
This is relevant as a trigger-like scheduled execution example, though no broader trigger canon is formalized.

Merge logic is clear in the source:
append and join are treated as distinct operations,
a dedicated join/merge layer exists,
and `logic.join()` is the core table-combination representation.
The flow emphasizes meaningful combination of data sources before export.

The source introduces a named stack concept:
`UMG.TradeFlow`.
This trading extension adds candidate domain blocks such as:
- `MarketDataBlock`
- `SignalDetectionBlock`
- `StrategyBlock`
- `AlertBlock`
- `PortfolioSimulatorBlock`
- `ExecutionBlock`

The execution block is marked optional and accompanied by caution language suggesting SafeMode or dry-run behavior.
That indicates boundedness for higher-risk action layers.

The source also proposes product/tooling concepts:
- flow-to-code converter
- import screenshots/configs, output UMG JSON or JSX
- drag-and-drop strategy builder
- canvas-style drag-and-drop + code fusion editor
- versioned reusable workflow modules

## Independent Review
This batch has high Stage 1 value because it shows how UMG can absorb an existing visual/business workflow without flattening it into static prose or one-off code.
The strongest contribution is the translation architecture itself:
visual flow → modular block/operator representation → layered blueprint → app/tool possibility.

The rendering/logic separation is particularly strong.
It gives the project a concrete example of how a source UI can remain distinct from the target modular logic layer.
That is directly relevant to future compiler, Studio, and builder tooling.

The trading extension is useful not because it finalizes trading architecture, but because it stress-tests the generality of the layered approach.
It shows that a base ETL architecture can accept domain-specific layers while keeping the same modular logic style.

Main cautions:
- much of the terminology remains exploratory
- operator names may be mapping conveniences rather than canon-approved vocabulary
- pseudocode does not establish real APIs or runtime contracts
- the converter concept is strong directionally but mechanically underdefined
- execution control in the trading example remains local and provisional

## Roadmap Mapping
Primary domain: visual-workflow translation, layered blueprinting, and domain-stack extension

Roadmap phases touched:
PHASE_2_COMPILER_IMPACT
PHASE_3_DOCUMENTATION_IMPACT
PHASE_4_SKILL_ALIGNMENT
PHASE_5_PRD_AND_STAGING
PHASE_7_RELEASE_READINESS
PHASE_8_POST_RELEASE_EXPANSION

Key phase implications:
Phase 2: supports a translation layer from visual nodes to UMG block/operator representations and ordered layered execution structure.
Phase 3: provides documentation-ready layer taxonomy and node-to-block equivalence vocabulary.
Phase 4: suggests new skill/tool workflows such as flow-to-code conversion and reusable workflow modularization.
Phase 5: contributes PRD-grade ideas for ETL designer tooling, code/UI dual surfaces, and modular export targets.
Phase 7: supports product packaging ideas such as starter zips, PWA apps, or editor prototypes.
Phase 8: shows how a base ETL architecture can be extended into domain stacks such as trading with signals, alerts, simulation, and bounded execution.

## Action Outcome
Accepted as evidence.
Frozen as a Stage 1 intake pack.
Optional compiler extract, NeoStructure extract, canon candidates, and contradiction flags are justified because the source contains layered taxonomy, operator mapping, visual-to-logic translation doctrine, and unresolved naming/tooling boundaries.

## Recommended Next Decision
Control-room review should decide how to normalize and promote:
1. layered blueprint taxonomy for workflow translation
2. node-to-block/operator equivalence documentation
3. visual-surface versus modular-logic separation rules
4. flow-to-code converter as tooling direction versus formal compiler subsystem
5. general ETL base stack versus domain-specific extensions such as trading
