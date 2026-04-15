# BATCH-034 Compiler Extract

## Compiler-Relevant Signal
This batch preserves a repeated baseline mapping that can be compared against later corrected mappings to isolate where field binding failed.

## Preserved Baseline Map
- Subject: trip to nearby car wash
- Use: immediate practical decision
- Aim: minimize friction
- Need: fast recommendation
- Primary: distance
- Philosophy: least necessary effort

## Compiler/Normalization Relevance
- Supports before/after comparison for Subject and Primary rebinding
- Useful for testing whether later resolver/prepass logic changes candidate generation and ranking
- Can act as a negative baseline in evaluation cases for goal-function coherence

## Candidate Follow-On Task
Define a compact evaluation harness that compares:
1. baseline location-first map
2. corrected goal-function map
3. final runtime selection behavior
