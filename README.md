<!-- BlackRoad SEO Enhanced -->

# passenger

> Part of **[BlackRoad OS](https://blackroad.io)** — Sovereign Computing for Everyone

[![BlackRoad OS](https://img.shields.io/badge/BlackRoad-OS-ff1d6c?style=for-the-badge)](https://blackroad.io)
[![BlackRoad OS Inc](https://img.shields.io/badge/Org-BlackRoad-OS-Inc-2979ff?style=for-the-badge)](https://github.com/BlackRoad-OS-Inc)
[![License](https://img.shields.io/badge/License-Proprietary-f5a623?style=for-the-badge)](LICENSE)

**passenger** is part of the **BlackRoad OS** ecosystem — a sovereign, distributed operating system built on edge computing, local AI, and mesh networking by **BlackRoad OS, Inc.**

## About BlackRoad OS

BlackRoad OS is a sovereign computing platform that runs AI locally on your own hardware. No cloud dependencies. No API keys. No surveillance. Built by [BlackRoad OS, Inc.](https://github.com/BlackRoad-OS-Inc), a Delaware C-Corp founded in 2025.

### Key Features
- **Local AI** — Run LLMs on Raspberry Pi, Hailo-8, and commodity hardware
- **Mesh Networking** — WireGuard VPN, NATS pub/sub, peer-to-peer communication
- **Edge Computing** — 52 TOPS of AI acceleration across a Pi fleet
- **Self-Hosted Everything** — Git, DNS, storage, CI/CD, chat — all sovereign
- **Zero Cloud Dependencies** — Your data stays on your hardware

### The BlackRoad Ecosystem
| Organization | Focus |
|---|---|
| [BlackRoad OS](https://github.com/BlackRoad-OS) | Core platform and applications |
| [BlackRoad OS, Inc.](https://github.com/BlackRoad-OS-Inc) | Corporate and enterprise |
| [BlackRoad AI](https://github.com/BlackRoad-AI) | Artificial intelligence and ML |
| [BlackRoad Hardware](https://github.com/BlackRoad-Hardware) | Edge hardware and IoT |
| [BlackRoad Security](https://github.com/BlackRoad-Security) | Cybersecurity and auditing |
| [BlackRoad Quantum](https://github.com/BlackRoad-Quantum) | Quantum computing research |
| [BlackRoad Agents](https://github.com/BlackRoad-Agents) | Autonomous AI agents |
| [BlackRoad Network](https://github.com/BlackRoad-Network) | Mesh and distributed networking |
| [BlackRoad Education](https://github.com/BlackRoad-Education) | Learning and tutoring platforms |
| [BlackRoad Labs](https://github.com/BlackRoad-Labs) | Research and experiments |
| [BlackRoad Cloud](https://github.com/BlackRoad-Cloud) | Self-hosted cloud infrastructure |
| [BlackRoad Forge](https://github.com/BlackRoad-Forge) | Developer tools and utilities |

### Links
- **Website**: [blackroad.io](https://blackroad.io)
- **Documentation**: [docs.blackroad.io](https://docs.blackroad.io)
- **Chat**: [chat.blackroad.io](https://chat.blackroad.io)
- **Search**: [search.blackroad.io](https://search.blackroad.io)

---


> Passenger — Sovereign AI inference engine. BlackRoad fork of Ollama. Local-first, fleet-routed, 52 TOPS.

Part of the [BlackRoad OS](https://blackroad.io) ecosystem — [BlackRoad-OS-Inc](https://github.com/BlackRoad-OS-Inc)

---

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
