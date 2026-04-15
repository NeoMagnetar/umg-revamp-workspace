# BATCH-068 COMPILER EXTRACT

## Compiler / Runtime-Relevant Findings

### 1. Terminology Must Be Correct Before Architecture Work
- WINA was initially misinterpreted.
- User correction materially changed the technical meaning of the whole discussion.
- Any future spec must explicitly use:
  - **Weight Informed Neuron Activation for Accelerating Large Language Model Inference**

### 2. Runtime Layers Are Not the Same as Logic Layers
This batch clearly separated:
- **WINA layer** -> neuron/tensor/dense-layer inference optimization
- **UMG layer** -> MOLT/block/cognitive orchestration

Compiler implication:
- do not collapse sparsity optimization into MOLT control without a demonstrated bridge.

### 3. Relevance-Based Activation Is a Candidate Research Surface
Conceptual idea only:
- some logic clusters may be heavier
- some may be lighter
- a runtime might eventually expose selective activation policies

Possible future research questions:
- can UMG logic groups be assigned cost classes?
- can lightweight profiles disable or defer some reasoning layers?
- can reflection budget be adjusted dynamically?

### 4. Candidate Optimization Targets
- lower latency
- lower power draw
- more local/offline feasibility
- more reflection cycles per compute budget

### 5. Possible Follow-Up Spec Items
- WINA-aware deployment note
- constrained-device UMG profile
- lighter/heavier logic-layer classification
- experimental relevance-based block activation policy
- benchmark harness separating:
  - model-runtime acceleration effects
  - UMG-level behavior effects

## Suggested Follow-Up Spec Items
- define optimization-only versus architecture-level claims
- add low-power deployment profile concept
- avoid canonizing neuron/MOLT coupling without evidence
