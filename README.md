<h1 align="center">Yağız Katerli</h1>

<p align="center"><b>I build systems that prove what they claim.</b><br/>
Playable simulations, coordination infrastructure for multi-agent work, and tools that make results checkable.</p>

<p align="center">
<img alt="Rust" src="https://img.shields.io/badge/Rust-000000?style=flat-square&logo=rust&logoColor=white" />
<img alt="Go" src="https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white" />
<img alt="Lean" src="https://img.shields.io/badge/Lean-6C4BFF?style=flat-square" />
<img alt="Babylon.js" src="https://img.shields.io/badge/Babylon.js-BB464B?style=flat-square" />
<img alt="k3s" src="https://img.shields.io/badge/k3s-FFC61C?style=flat-square&logo=k3s&logoColor=black" />
</p>

### What I do

I design and build systems where every claim is checkable. A work item is a **desired state** with measured acceptance commands; a delivery is a **receipt** with a digest and a lease token; work that cannot be proven is reported as unmeasured, never as done. The interesting part is not the demo — it is the machinery that makes the demo trustworthy.

### Selected work

**Playable worlds**
- **transformice3d** — a 3D surf game with a deterministic simulation core and a Babylon.js scene. Same seed, same result: `node --test` 61/61, and a game IR whose digest is `18feab17…` for seed 7.
- **roadcase** — a browser driving game on a hand-rolled WebGL2 engine: no framework, no build step, changes gated by capsule checks.

**Distributed systems**
- **distributed-systems-lab** — small experiments on failure: a lost reply, a client retry, and a duplicate effect. Without request IDs the counter reaches 2 and the invariant breaks; with an idempotency key it stays at 1. The result is recorded as JSON, not prose.

**Systems and infrastructure**
- A **codebase control plane** for multi-agent work: leases with fencing tokens, a write state machine, idempotent receipts, and a runner that turns desired states into measured outcomes.
- **Lobi** — a desktop app and API built on an event-sourced, hash-chained room ledger: proposals, turns and decisions survive restarts and can be replayed.
- An **evidence archive**: a verified self-archive (207 works, 207/0 digest checks), a licensed open-access collection, a 32,441-document corpus, and a full-text index of 370k chunks.

**Film**
- An **agentic film pipeline** with seven stages: research, selection, interpretation, storyboard, render, receipt, publish. The latest run produced a 15-second 720p film with a poster and a per-stage receipt chain.

### Principles

1. **Measure, don't assert.** Every acceptance criterion is a command with an expected result.
2. **One owner per task.** A lease carries a fencing token; stale owners are rejected.
3. **Receipts, not promises.** No digest, no “done”.
4. **Fail closed.** If a gate cannot be measured, work does not proceed.
5. **Keep the source where it belongs; show the output.** Architecture, measurements, receipts and demos are public. Code is private where it needs to be.

### Private work

Most production source is private. What is public is the part that lets you judge the work: architecture, measured outputs, receipts and demonstrations. Access to private sources is available on request for collaborators, shared-interest evaluation, or under NDA.

*Measured 2026-11-12. Every number above points to a receipt or a reproducible command.*
