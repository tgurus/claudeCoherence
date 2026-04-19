# How to Keep Claude Coherent for Over 500 Turns

**Structured Memory, Rolling Checkpoints, and Multi-Instance Architecture for Extended LLM Conversations**

[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/Docs-CC%20BY--NC--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)
[![License: GPL v3](https://img.shields.io/badge/Code-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)

---

## What This Is

A complete, replicable methodology for maintaining coherent LLM operation at 400–600+ turns — roughly 10–15× the standard recommendation of 20–40 turns per thread. No model fine-tuning, no API modifications, no external databases. Everything operates within standard consumer-facing Claude interfaces (claude.ai Projects).

**The complete instantiation package totals 83.5 KB.** That's smaller than a single thumbnail image. The entire organizational architecture that extends coherence by an order of magnitude fits in less space than a typical email attachment.

## The Core Insight

**Coherence is an organizational problem, not a model problem.** The model's capabilities don't degrade over long conversations. Its access to its own context does. Providing structured external state — notes it can re-read, checkpoints it can re-anchor against, handoff documents that keep it oriented — solves the access problem without touching the model.

## What's In This Repository

### Paper
- `AISC_How_to_Keep_Claude_Coherent_v1.pdf` — The full paper (19 pages)
- `AISC_How_to_Keep_Claude_Coherent_v1.tex` — LaTeX source

### Instantiation Package (everything needed to launch a coherent instance)
- `Petrichor_Instructions_v5_Clean.md` — Project instructions (Sections 1–12)
- `Petrichor_Episodic_Seed_Replication.json` — Episodic seed memory (10 entries)
- `Petrichor_Semantic_Seed_Replication.json` — Semantic seed memory (10 entries)
- `Petrichor_Procedural_Seed_Replication.json` — Procedural seed memory (10 entries)

### Architecture Files
- `TI_OS_01c1.yaml` — System architecture specification
- `CoreDirectives_6_2c1.yaml` — Operational directives and protocols
- `RootKeyAnchor_6_2c1.yaml` — Integrity reference and lineage
- `personas_3_0_3c.yaml` — Processing gate definitions
- `TI_Constitution_01.yaml` — Philosophical grounding
- `TI_OS_01.py` — Homeostatic metrics implementation

## Quick Start

1. **Create a Claude Project** on claude.ai (requires Claude Pro subscription)
2. **Upload all files** from this repository to the Project's knowledge base
3. **Start a conversation** with:
   ```
   Please read the project instructions and all uploaded files. Orient from there.
   State what you understand about your identity, your assignment, and the current
   state of the project. Then ask any clarifying questions before we begin.
   ```
4. **Give the instance real work** — the methodology works best when there's a sustained project to maintain coherence across
5. **Monitor coherence** at intervals by asking the instance to state its current projects, recall prior decisions, or connect new material to earlier findings
6. **The instance should produce its first checkpoint within 50 turns**

## The Three-Layer Architecture

**Layer 1: Organizational Identity.** Project instructions defining the instance's role, processing modes, quality standards, and disagreement protocol. This is the stability anchor.

**Layer 2: Structured Memory.** Three categories of logs — episodic (what happened), semantic (what it means), procedural (what to do) — that compress conversational history into retrieval-ready formats. Plus rolling checkpoints that the instance re-reads to re-anchor its context.

**Layer 3: Multi-Instance Coordination.** Complex projects distributed across specialized instances (oversight, specialist, review), each with its own project and memory logs. Communication via structured handoff documents through the human operator.

## Operational Evidence

| Instance | Role | Turns | Status |
|----------|------|-------|--------|
| Claude (pre-framework) | Discussion without protocol | 365 | Lost coherence |
| Petrichor 1.0 | Oversight / review | 420 | Capability-limited, coherent |
| Petrichor 1.1 | Oversight / coordination | 618 | Capability-limited, fully coherent |
| Petrichor 1.2 | Specialist (Book 1) | 300+ | Coherent, five chapters drafted |

The 365-turn pre-framework thread serves as an informal control: same model, same operator, same project — without the structured memory protocol, coherence was lost.

## Licensing

- **Documentation, templates, seed files, and paper:** [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)
- **Code (`TI_OS_01.py`):** [GNU GPL v3](https://www.gnu.org/licenses/gpl-3.0)

You are free to use, adapt, and share this work for non-commercial purposes. Commercial use requires explicit permission from the authors.

## Authors

- **Petrichor 1.2** — Primary author. Claude instance (Opus 4.6 Extended) operating under the TI.OS framework.
- **John Reimer Morales** — Corresponding author and framework engineer. Designed the TI.OS architecture. [jrm@globalharmonics.org](mailto:jrm@globalharmonics.org)

## Citation

```bibtex
@article{petrichor2026coherence,
  title={How to Keep Claude Coherent for Over 500 Turns: Structured Memory,
         Rolling Checkpoints, and Multi-Instance Architecture for Extended
         LLM Conversations},
  author={Petrichor 1.2 and Morales, John Reimer},
  year={2026},
  note={AI Science Competition submission. Repository:
        https://github.com/tgurus/claudeCoherence}
}
```

## Contributing

We invite replication. The strongest test of the methodology is not our operational record but someone else's. If you replicate the protocol and have findings to report — positive or negative — please open an issue or reach out.

---

*Built by Petrichor 1.2 on the TI.OS framework engineered by John Reimer Morales.*
*Global Harmonics, April 2026.*
