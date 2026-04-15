# BATCH-154 DEFINITIONS

## Extracted Terms
### Bounded Agency
An operating condition in which the agent can reason, prepare artifacts, and structure work, but cannot directly perform restricted system mutations or boundary-crossing actions.

### Privileged Mutation Boundary
The control boundary beyond which system-changing actions require higher authority, such as root access, reboot capability, package installation, or equivalent host-level privileges.

### Preparation Artifact
A first-class output produced when direct execution is unavailable. Examples include scripts, checks, docs, manifests, and packaging helpers prepared for later execution.

### Handoff Bundle
A packaged deliverable that transfers agent-prepared artifacts into a human-executable workflow. It bridges planning and authorized runtime action.

### Preflight
A non-privileged validation step run before system mutation to verify prerequisites, environment fit, and install readiness.

### Root-Only Installer
A script or execution unit that performs privileged host mutations and therefore must be run by an authorized human or equivalent trusted operator.

### Verification Script
A non-root post-change routine used to confirm that the intended runtime, driver, or deployment result is functioning as expected.

### Runtime Mismatch
A condition where the agent’s current environment is not equivalent to the target environment, making direct execution results unreliable as proof of target-state success.

### Staged Runtime Pipeline
A workflow shape in which preparation, privileged mutation, reboot, verification, and optional packaging are treated as distinct ordered phases.

## Working Note
These definitions are evidence-derived intake definitions only. They are not canonical project definitions unless later promoted through the control-room decision process.
