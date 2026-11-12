<h1 align="center">Yağız Katerli</h1>

<p align="center"><b>I build systems that prove what they claim.</b><br/>
Verifiable agent systems, deterministic simulations, and the evidence machinery underneath them.</p>

<p align="center">
<img alt="Rust" src="https://img.shields.io/badge/Rust-000000?style=flat-square&logo=rust&logoColor=white" />
<img alt="Go" src="https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white" />
<img alt="Lean" src="https://img.shields.io/badge/Lean-6C4BFF?style=flat-square" />
<img alt="Babylon.js" src="https://img.shields.io/badge/Babylon.js-BB464B?style=flat-square" />
</p>

### Three tools told me a job succeeded today. All three were wrong.

`git push` returned exit 0 and printed `[new branch]` — nothing reached GitHub, because `origin` pointed at a local directory.

`git merge-tree` reported clean on 10 open pull requests — a real rebase conflicted on all 10.

`lake build` printed `Build completed successfully` with RC=0 — every theorem in the file was `sorry`.

None of these is a bug. Each tool answered the question it was asked. The failure is that an agent reading the exit code cannot tell the difference between **“it worked”** and **“it worked against the thing I meant.”**

That silent success is the most expensive thing I measure, because it looks identical to progress. So I build the test that runs both arms of the same question, reports where they disagree, and ships with its own falsifiers. A claim you cannot break is not evidence.

### Selected work

**Verifiable agent systems**
- A **codebase control plane**: leases with fencing tokens, a write state machine, idempotent receipts. One owner per task; stale owners are rejected; no digest means no “done”.
- **Evaluation infrastructure**: desired states with measurable acceptance commands, machine receipts, and a runner that reports unmeasured work as unmeasured.

**Deterministic simulations**
- **transformice3d** — a 3D surf game with a deterministic core and a Babylon.js scene. Same seed, same result: `node --test` 61/61, and a game IR digest of `18feab17…` for seed 7.
- **roadcase** — a browser driving game on a hand-rolled WebGL2 engine: no framework, no build step, changes gated by capsule checks.

**Distributed systems**
- **distributed-systems-lab** — small failure experiments: a lost reply, a client retry, and a duplicate effect. Without request IDs the counter reaches 2 and the invariant breaks; with an idempotency key it stays at 1. Recorded as JSON, not prose.
- **Lobi** — a desktop app and API on an event-sourced, hash-chained room ledger: proposals, turns and decisions survive restarts and can be replayed.

**Film and knowledge**
- An **agentic film pipeline** with seven stages — research, selection, interpretation, storyboard, render, receipt, publish. Latest run: a 15-second 720p film with a poster and a per-stage receipt chain.
- An **evidence archive**: 207 verified works (207/0 digest checks), a licensed open-access collection, a 32,441-document corpus, and a full-text index of 370k chunks.

### How I measure

1. **Measure, don’t assert.** Every acceptance criterion is a command with an expected result.
2. **One owner per task.** A lease carries a fencing token; stale owners are rejected.
3. **Receipts, not promises.** No digest, no “done”.
4. **Fail closed.** If a gate cannot be measured, work does not proceed.
5. **Show the output; keep the source.** Architecture, measurements, receipts and demos are public. Source stays private where it needs to be.

### Private work

Most production source is private. What is public is the part that lets you judge the work: architecture, measured outputs, receipts, and demonstrations. Access is available on request for collaborators, shared-interest evaluation, or under NDA.

*Measured 2026-11-12. Every number above points to a receipt or a reproducible command.*
