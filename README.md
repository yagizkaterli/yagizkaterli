# HERAKLES

Evidence-first multi-agent systems: a game, a codebase OS, and a distributed systems lab.

## What you can run today
| Repo | What it is | Proof |
|---|---|---|
| [transformice3d](https://github.com/yagizkaterli/transformice3d) | Playable 3D surf game: deterministic core + Babylon.js scene | `node --test` 61/61; Game IR `hrk-game-ir/v0` sha `18feab17…` |
| [distributed-systems-lab](https://github.com/yagizkaterli/distributed-systems-lab) | Timeout/retry experiments: lost replies, request IDs, dedupe | `cargo run -- demo2` rc=0; experiment 02 JSON |
| [herakles-scale](https://github.com/yagizkaterli/herakles-scale) | Rust system entry: `hrk` (leases, DS runner, ARE, audio), sindirim FTS | `cargo test` suites; machine receipts |
| [herakles-world-engine](https://github.com/yagizkaterli/herakles-world-engine) | Deterministic world physics (IDM longitudinal model) | `cargo test -p world-v21 fizik` 5/5; commit `219baeb` |
| [lobi](https://github.com/yagizkaterli/lobi) | Desktop + API on an event-sourced, hash-chained room ledger | `lobid-native` events; room/turn model |
| [firstmate](https://github.com/yagizkaterli/firstmate) | GitHub visibility unit: README/metadata/evidence cadence | Reads-only plans + human-gated application |

## How it works
- **Desired state**: every work item is a `*.ds` file with measurable acceptance commands.
- **Receipts**: `hrk is bitir` writes `ds_sha256` + `kira_token`; unproven work is `OLCULEMEDI`.
- **Fences**: one lease owner per task (`fence_token`); stale owners are rejected.
- **Knowledge**: IDEA sims + REA analysis; public where it can be shared.

## Status
Measured on 2026-11-12. Machine gates: DS 0/5 baseline for GitHub visibility (closing), Lobi D3 merge pending, ACK capsule coverage 1.3%.

Contact: see `author` fields in the repos. Everything above is backed by a receipt in the corresponding repo's coordination tree.
