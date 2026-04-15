# BATCH-106_COMPILER_EXTRACT

## Scope
Compiler/runtime-relevant signals extracted from BATCH-106.

## High-Signal Candidates

### 1. Metadata normalization before filesystem routing
The batch shows that raw repository metadata cannot be trusted blindly.

Compiler consequences:
- normalize `category` and `molt_type` before routing
- define alias/case handling rules
- detect missing metadata before move execution
- avoid mass fallback into `Misc/Unknown`

### 2. Reorganization script as proto-compiler
The source describes a concrete transform pipeline:
- read metadata
- compute target path
- dry-run plan
- execute moves
- verify
- validate

Implementation pressure:
- preserve plan/execute separation
- generate machine-readable reports
- support rollback/checkpoint strategy
- treat repository transforms as staged operations rather than ad hoc scripts

### 3. Validation after transform
Validation is acting as a post-transform type checker.

Compiler/runtime consequences:
- require validation after reorganization
- distinguish routing errors from schema errors
- surface unexpected-field failures and content-type failures clearly
- block downstream runtime usage when repository integrity is compromised

### 4. Canonical field policy is still unresolved
Validation failures cluster around:
- `content`
- `merge_logic`
- `color`
- `export_config`

Implementation pressure:
- settle allowed field list
- decide whether to reject, normalize, or migrate extension fields
- make schema evolution/versioning explicit
- avoid silent field loss during normalization

### 5. Release hygiene intersects with compiler workflow
Secret exposure and history rewrite materially affected release flow.

Staging implications:
- enforce `.env` exclusion and secret scanning
- add pre-commit or pre-push gates
- preserve backup/tag checkpoints
- separate repository cleanup from block normalization where possible

## Suggested Audit Angles
- define a single canonical reorg tool and retire script proliferation
- formalize metadata normalization rules before routing
- define strict versus compatibility validation modes
- document field whitelist and `content` type policy
- integrate validation and secret scanning into staged release workflow

## Confidence
High for operational workflow relevance, medium for final schema policy.
The batch is concrete about what broke and how recovery proceeded, but it does not settle the final canonical block contract.
