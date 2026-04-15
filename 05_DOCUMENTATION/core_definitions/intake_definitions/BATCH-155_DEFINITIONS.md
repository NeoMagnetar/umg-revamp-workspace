# BATCH-155_DEFINITIONS

## Intake Definitions Extract

### Cognitive OS
The broader locally runnable AI / UMG-aligned system being built on the laptop in this source.

### Port Poe
Re-point or adapt Poe so it runs against a local model-serving stack rather than a fixed hosted backend.

### One endpoint for many brains
A single stable API surface used by the agent while different model backends can be swapped underneath it.

### Core I/O
The runtime substrate in this batch, mapped to Docker Desktop and WSL2.

### Cognition
The model-serving layer in this batch, mapped to Ollama and/or vLLM.

### Protocol
The API normalization layer in this batch, mapped to an OpenAI-compatible `/v1` endpoint and optionally LiteLLM Router.

### Memory
Optional persistence / retrieval infrastructure, mapped here to Postgres plus pgvector.

### Envoy (Poe)
The agent/client surface that talks to the protocol layer while backend providers remain swappable.

### CPU baseline
The lowest-friction local serving starting point before GPU complexity is introduced.

### GPU path
A later-stage local inference route using laptop GPU acceleration for stronger model performance.
