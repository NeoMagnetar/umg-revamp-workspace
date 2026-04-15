# BATCH-152 — Bounded Agent Bridge and Browser Workspace Review

## Batch Overview
Batch ID: BATCH-152  
Source Type: derived summary / agent-bridge runtime and staging consolidation  
Working Topic: agent planning environment versus visible implementation surface, browser IDE proxy, bounded command bridge, Bolt preview/runtime split  
Review Status: REVIEWED  
Disposition: ACCEPT_AS_EVIDENCE

## Source Snapshot
The source is a structured consolidation of a chat focused on a simple Bolt app that would let an external agent interact with a browser-hosted VS Code environment through a proxy layer.
The design explicitly separated:
- a browser IDE surface
- a proxy server
- an agent command pathway

The conversation then moved from layman explanation and use-case framing into implementation guidance:
file tree,
routes,
startup flow,
Docker versus non-Docker execution,
debugging,
and failure recovery.

A major runtime lesson surfaced in the chat:
Bolt cloud preview does not support the same nested Docker assumptions as local or production hosting.
That staging split became one of the most important practical outputs.

Because the source is a derived summary rather than a canon-design chat, it should be treated as strong evidence of runtime separation, bounded agency, bridge architecture, and staging discipline, but not as automatic canon.

## Chat-Level Summary
This batch is strongest as an agent-usable runtime bridge pattern.
Its central contribution is a clear separation of environments:
the agent works in its own planning/execution environment, then applies work through a bounded interface into a visible browser-based implementation surface.

The strongest reusable signal is that the implementation surface is not the agent’s native environment.
It is a controlled action surface.
That gives the project a concrete model for:
plan elsewhere,
act through bounded primitives,
reflect results into a user-visible workspace.

The second strongest contribution is staging realism.
The chat did not stay at architecture slogans.
It discovered that local/prod Docker behavior and Bolt cloud preview behavior differ materially, and the system must support different runtime modes.

The source is weaker on explicit UMG terms, but strong on control layers, runtime boundaries, visible execution surfaces, and safe agent-operable bridge design.

## UMG-Relevant Extraction
No explicit UMG semantic canon was defined in the source.
The relevance is indirect but strong.

The core architecture is:
- agent decides or prepares in its own environment
- Bolt receives a command
- proxy executes against bounded workspace
- browser IDE reflects the result visibly to the user

The source strongly supports separation between:
- planning environment
- control interface
- implementation/render surface

The browser IDE is the visible workspace.
The proxy terminal/API is the agent’s action surface.
The agent is not given unrestricted system control.

Governance and control patterns surfaced include:
- command whitelist for `/api/exec`
- workspace directory scoping
- auth / password / OAuth / JWT gating
- one-container-per-project blast-radius control
- audit logging
- git-backed rollback
- resource limits
- configurable network access
- batching commands instead of unconstrained chatter

This is strong bounded-agency material even without formal UMG block language.

Output/render separation is unusually clear in the source:
- browser IDE at `/ide`
- Bolt front-end wrapper
- proxy server
- external agent command origin

The visible effect path is:
plan → message → proxy → shell/file action → reflected change in IDE

Compiler/runtime logic is concrete.
Main routes:
- `/ide` for reverse proxying the browser IDE
- `/api/exec` for command execution

The source explicitly distinguishes:
- local / prod execution with Docker
- cloud preview / dev execution without Docker

This is effectively a runtime-mode split rather than one universal execution model.

Documentation/spec language in the source includes:
- file tree
- `.env`
- `docker-compose.yml`
- `README.md`
- `src/index.html`
- `src/main.js`
- `src/server.js`
- `package.json` scripts and dependencies
- fixer instruction blocks
- POST/message-based execution contract
- safety TODOs

Skill / agent workflow is explicit:
1. agent works in its own environment
2. determines needed changes
3. uses proxy path into browser IDE/workspace
4. user sees the effects live
5. rollback/review remains possible

Future richer action surfaces were proposed through JSON RPC-style actions such as:
- `saveFile`
- `readFile`

The source also strongly supports auditability and rollback as baseline design requirements.

## Independent Review
This batch has high Stage 1 value even though it is only indirectly UMG.
Its main contribution is a practical architecture for bounded agency in a visible implementation environment.

The strongest doctrinal signal is:
the implementation surface is not the agent’s native environment; it is a controlled action surface.
That is highly reusable for UMG-aligned runtime and bridge designs.

The second strongest contribution is the staging split.
Many systems fail by assuming the same runtime everywhere.
This source explicitly discovered a cloud-preview versus local/prod divergence and adapted the architecture around it.

The source is especially valuable for PRD and runtime sections, less so for core MOLT semantics.
It does not define blocks, sleeves, or NeoStacks directly.
It instead gives the project a runtime pattern that could later be wrapped in those terms.

Main cautions:
- no explicit UMG taxonomy was established
- some language is metaphorical rather than canon-ready
- the bridge moved between shell proxy and richer future RPC concepts
- final security model was not locked
- exact autonomy scope remained provisional

## Roadmap Mapping
Primary domain: bounded agent bridge architecture and staged runtime deployment

Roadmap phases touched:
PHASE_2_COMPILER_IMPACT
PHASE_3_DOCUMENTATION_IMPACT
PHASE_4_SKILL_ALIGNMENT
PHASE_5_PRD_AND_STAGING
PHASE_7_RELEASE_READINESS

Key phase implications:
Phase 2: supports translation of agent intent into bounded execution primitives.
Phase 3: provides documentation-ready language for planning environment, control interface, and implementation surface separation.
Phase 4: informs agent/skill workflows through command whitelisting, audit logging, and rollback-aware bridge design.
Phase 5: contributes PRD-grade staging logic for local/prod Docker versus cloud preview non-Docker modes.
Phase 7: improves release realism by forcing runtime-mode distinction rather than one false universal path.

## Action Outcome
Accepted as evidence.
Frozen as a Stage 1 intake pack.
Optional compiler extract, canon candidates, and contradiction flags are justified because the source contains a strong bridge-runtime pattern, explicit bounded-agency controls, and unresolved implementation/staging tensions.

## Recommended Next Decision
Control-room review should decide how to normalize and promote:
1. planning environment versus implementation surface separation
2. bounded bridge execution contract
3. command whitelist / audit / rollback baseline rules
4. runtime mode switching between cloud preview and local/prod
5. whether richer JSON-RPC workspace actions should replace raw shell-only bridge actions
