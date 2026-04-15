# BATCH-160 — NeoStructure Extract

## Proposed structural architecture
### Recommended multi-repo organization
- `umg-meta` = thin meta repo with docs/scripts and cross-repo maintenance
- `umg-core` = canon; vault/blocks, sleeves, spines, triggers
- `umg-datasets` = raw/curated/recipes/export
- `umg-evals` = suites/runners/reports
- `poe-os` = operator; tools/middleware/clients
- `umg-autotrainer` = Space + local training service; app/docker/pipelines

## Runtime stack signals
- System prompt / runtime assembly:
  - Alignment Spine
  - Sleeve
  - Overlay
  - active Stack header
- Operator/runtime remains separate from model weights
- Eval/reporting remains separate from training
- Space control plane remains separate from core canon

## Structural value
This source provides a strong candidate separation between:
1. canon
2. dataset
3. eval
4. operator/runtime
5. trainer/deployment

That separation should be preserved as evidence for architecture review.
