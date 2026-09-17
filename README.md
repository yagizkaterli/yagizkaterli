# Yağız Katerli

**Building agent systems that have to prove the work happened.**

Mathematical Engineering @ Istanbul Technical University · Istanbul

I work on autonomous agent infrastructure, evaluation, formal verification, and operator tooling. The recurring problem is simple to state and hard to enforce:

> **When an agent says it delivered something, what evidence is sufficient to believe it?**

My current work treats that as an engineering problem rather than a prompting problem: claims are bound to artifacts, receipts, runtime observations, falsifiers, and — where the property is actually formal — Lean proofs.

## Current research

### CapsuleBench — proof of delivery for autonomous agents

The core object is an evidence chain:

```text
claim -> evidence -> binding -> falsifier -> verdict
```

I use it to study failure modes that ordinary "task completed" evaluation misses: stale artifacts, wrong run identity, measurement-vs-success confusion, locally correct measurements taken from the wrong system layer, verifier bugs, and cases where an agent updates its belief but not its behavior.

The goal is not to make agents sound more certain. It is to make unsupported certainty expensive.

### LeanPy — proof-carrying agent computation

A Python program or agent computes a candidate. Lean checks a critical property of the **concrete result** before that result is admitted into a trusted path.

```text
live state -> Python / agent -> candidate + witness -> Lean gate -> accept / reject -> action
```

This is deliberately narrower than "formally verified Python": the proof has to be bound to the exact input, candidate, contract and verifier result. `PROOF != BINDING`, and a type-checking theorem is not automatically evidence about a live system.

Current implementation work lives in a private research repository while the interface and enforcement boundary are still moving.

### Herakles

Herakles is the larger experimental system around these ideas: persistent agents, parallel execution, context recovery, receipts, evaluation, formal gates, runtime observation, and operator surfaces.

A small public skeleton of the current harness direction is in [herakles-harness-os](https://github.com/yagizkaterli/herakles-harness-os). The active system is broader than that repository, so I do not treat the public skeleton as a complete representation of the live system.

## What I care about

- **Verification over consensus.** More agents repeating a claim does not make it true.
- **Evidence identity.** A receipt has to refer to the exact artifact/run it claims to verify.
- **Fail-closed boundaries.** Unknown, stale, unmeasured, or mismatched evidence should not silently become green.
- **Verifier accountability.** A failing verifier can itself be wrong; the verifier needs falsifiers too.
- **Context recovery.** In long-lived agent systems, finding the authoritative current system layer is part of the task.
- **Human-verifiable compression.** Large execution histories should compress into small evidence graphs without compressing away accountability.

## Public work

| repository | what it is |
|---|---|
| [herakles-harness-os](https://github.com/yagizkaterli/herakles-harness-os) | early public skeleton for a single Herakles harness surface with mechanical / Lean-provable acceptance |
| [chess-tui](https://github.com/yagizkaterli/chess-tui) | terminal chess work |
| [treehouse](https://github.com/yagizkaterli/treehouse) | public systems work / experiments |
| [foundation](https://github.com/yagizkaterli/foundation) · [frictionless](https://github.com/yagizkaterli/frictionless) · [human-steps](https://github.com/yagizkaterli/human-steps) · [perfect-form](https://github.com/yagizkaterli/perfect-form) · [idea-boost](https://github.com/yagizkaterli/idea-boost) · [tahmin](https://github.com/yagizkaterli/tahmin) | small extracted methods / skills |

Some of the most active repositories — including the current agent-fleet, LeanPy and evaluation work — are private while their contracts are changing quickly. I would rather expose a smaller claim than a larger one that cannot be independently checked.

## Current engineering direction

`Go` · `Rust` · `Lean 4` · `Python` · `TypeScript`

Agent orchestration · evaluation harnesses · proof-carrying decisions · terminal/operator tooling · provenance · receipts · context retrieval · CI gates · observability

## Background

I study Mathematical Engineering at Istanbul Technical University. Outside software: jazz drums, mathematics, film, and philosophy.

**Open to:** research engineering, agent infrastructure, evaluation, and formal-methods-adjacent work.

📫 yagizkaterli@gmail.com · [LinkedIn](https://linkedin.com/in/yagizkaterli)
