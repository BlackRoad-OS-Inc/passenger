# Passenger — BlackRoad Road Fleet

> **Sovereign AI inference engine.** Fork of [Ollama](https://github.com/ollama/ollama).

---

**Passenger** is BlackRoad's sovereign fork of Ollama — local-first AI inference running on your hardware. No API keys, no cloud dependency, no data leaving your network.

## What's Different

- **BlackRoad fleet integration** — auto-discovers nodes via NATS, routes to fastest GPU
- **Compressed system prompts** — 86 lines → 8 lines = 3x fewer prompt tokens
- **Road Fleet identity** — every model speaks as a BlackRoad Roadie
- **Hailo-8 awareness** — 52 TOPS across 2 accelerators (Cecilia + Octavia)
- **Fleet routing** — round-robin with failover across Alice, Cecilia, Octavia, Lucidia

## Fleet Deployment

```bash
# On any Pi node
curl -fsSL https://ollama.com/install.sh | sh
ollama pull tinyllama:latest
ollama pull llama3.2:1b
ollama pull phi3:mini

# BlackRoad custom models
ollama create blackroad-road -f Modelfile.blackroad
```

## Current Fleet Status

| Node | IP | Models | TOPS | RAM |
|------|----|--------|------|-----|
| Alice | 192.168.4.49 | tinyllama, llama3.2 | CPU | 8GB |
| Cecilia | 192.168.4.96 | 16 models | 26 (Hailo) | 8GB |
| Octavia | 192.168.4.101 | 227 models | 26 (Hailo) | 8GB |
| Lucidia | 192.168.4.38 | tinyllama | CPU | 8GB |
| Gematria | 159.65.43.12 | 6 models | CPU | 4GB |

## Configuration

```bash
# Environment
OLLAMA_HOST=0.0.0.0:11434
OLLAMA_MODELS=/usr/share/ollama/.ollama/models
OLLAMA_NUM_PARALLEL=2
OLLAMA_MAX_LOADED_MODELS=2
```

## Upstream

Forked from [ollama/ollama](https://github.com/ollama/ollama) (MIT License upstream).
All BlackRoad modifications are proprietary.

---

**BlackRoad OS, Inc.** — Pave Tomorrow.

*Proprietary. All rights reserved.*
