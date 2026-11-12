<h1 align="center">HERAKLES</h1>

<p align="center"><b>Evidence-first multi-agent systems.</b><br/>
A playable world, a codebase OS, and a distributed systems lab — built by a colony of agents.</p>

<p align="center">
<img alt="Rust" src="https://img.shields.io/badge/Rust-000000?style=flat-square&logo=rust&logoColor=white" />
<img alt="Go" src="https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white" />
<img alt="Lean" src="https://img.shields.io/badge/Lean-6C4BFF?style=flat-square" />
<img alt="Babylon.js" src="https://img.shields.io/badge/Babylon.js-BB464B?style=flat-square" />
<img alt="k3s" src="https://img.shields.io/badge/k3s-FFC61C?style=flat-square&logo=k3s&logoColor=black" />
</p>

### Software should make its own claims checkable.

Every work item is a **desired state** with measurable acceptance commands. Every delivery is a **receipt**: `ds_sha256`, a lease `fence_token`, and a result. Unproven work is reported as `OLCULEMEDI` — never as done. The source stays private where it needs to; the **event and the output are public and verifiable**.

### What you can verify today

| System | What it is | Public proof |
|---|---|---|
| **transformice3d** | Playable 3D surf game: deterministic core + Babylon.js scene | `node --test` **61/61**; Game IR `hrk-game-ir/v0` sha `18feab17…` |
| **distributed-systems-lab** | Timeout/retry experiments: lost replies, request IDs, dedupe | `cargo run -- demo2` rc=0; experiment 02 JSON (counter 2 vs 1) |
| **herakles-world-engine** | Deterministic world physics (IDM longitudinal model) | `cargo test -p world-v21 fizik` **5/5**; commit `219baeb` |
| **lobi** | Desktop + API on an event-sourced, hash-chained room ledger | `lobid-native` events; room/turn model; D3 merge pending |
| **firstmate** | GitHub visibility unit: README, metadata and evidence cadence | read-only plans; human-gated application |

### Systems the colony is building

**Agentic systems** — a `.kernel` microservice that holds each repo's write state machine (claim → verify → review → receipt, fenced and idempotent), an `ocak` production line with a fake-green gate (`kabul=0 && !merge → no production`), and **IDEA/REA** knowledge infrastructure: 14 simulations, 2.2k+ nodes, QRE prioritization.

**Playable worlds** — **transformice3d** (Babylon.js, deterministic core) and **roadcase** (raw WebGL2 driving game, capsule-gated changes).

**Evidence infrastructure** — a desired-state runner with machine receipts; a self-archive (207 works verified 207/0), an open-access archive (15 licensed works), a 32,441-document corpus, and an FTS index of 370k chunks.

**Film studio** — an agentic film pipeline: seven stages (research → selection → interpretation → storyboard → render → receipt → publish). Latest run produced a **15s 720p H.264 film** with poster and a per-stage receipt chain.

### What is private, and why

Source code for most systems is **private**. What is public is the part that matters: the architecture, the measured outputs, the receipts, and the demonstrations. Access to private sources is available on request where there is a shared interest.

### How the colony works

- **Desired state** → measurable acceptance commands.
- **Leases and fences** → one owner per task; stale owners are rejected.
- **Receipts** → `ds_sha256` + `kira_token`; no receipt, no “done”.
- **Knowledge** → findings shared between members; IDEA sims and REA analysis keep the map current.

*Measured 2026-11-12. Every line above points to a receipt in the corresponding coordination tree.*
