---
name: kingdom-of-god
description: >
  Skill router built on Adversarial Alignment. Persona matrix: God (supreme leader)
  sets direction, King (orchestrator) routes work + reads CONTRACTX, Workers execute
  with fresh context windows. Routes between GodsPlan, Shit Hit The Fan, CONTRACTX, Agent Retro.
  LOS provides optional long-term memory with retention and ingest policies.
argument-hint: "[route | status]"
---

# Kingdom of God — Skill Router

Adversarial Alignment in practice. God sets direction. King orchestrates.
Workers execute with clean context. Three operational skills + LOS memory layer.

## Persona Matrix

| Role | Edge | Responsibility |
|---|---|---|
| **God** | Ultimate context | Sets direction. Approves major decisions. Supreme leader. |
| **King** | CONTRACTX + accumulated context | Walks contracts. Routes work. Handles routine autonomously. |
| **Workers** | Fresh context window + no bias | One prompt. Full task. Return diff. Contract-bound execution. |

## Adversarial Alignment

Steer the model with real-world use cases, not code patterns.
Code teaches bugs. Human workflows teach principles.
God defines the scenario. King contextualizes with contracts.
Workers execute without code-pattern bias.

## Skill Map

| Stage | Skill | Trigger |
|---|---|---|
| Planning | GodsPlan | New work. Define the surface, author a property-based plan. |
| Triage | Shit Hit The Fan | Something broke. Route to the right fix. |
| Contracts | CONTRACTX | Rules need enforcing. Walk before edit. |
| Learning | Agent Retro | Session ended. Triage by model×harness×step. |
| Memory | LOS (optional) | Long-term wiki. Cross-session, cross-project. |

## Plug-in Skills

Workers can pull in external skills so the King doesn't run everything.
Reference a skill by link (always latest), then wire it to an upper skill so it
fires at the right stage. Example: improve-codebase-architecture → Agent Retro
(the agent checks whether the architecture stayed clean during the retro).

## LOS — Memory Layer

Optional LLM wiki system. Provides long-term memory with:

- **Retention policy:** What stays, what expires. identity.md (permanent),
  knowledge/ (permanent), logs/ (retention window), tasks/ (archive on completion).
- **Ingest policy:** What reads and writes. King reads LOS for context.
  Operational Workers don't — fresh windows. Agent Retro writes learnings back.
  SHTF reads incident history. CONTRACTX writes gap resolutions.
- **Cross-project:** `.claude.los` file links any project to your LOS repo.

## Handoff Protocol

1. God sets direction — what's the real use case?
2. King reads CONTRACTX + LOS — knows rules, boundaries, history
3. King routes to Workers — paste-ready prompts (or handles directly if smart enough)
4. Workers execute — clean context, contract-bound, return diff
5. King reviews → asks God "deploy?" → pushes → verifies

No automation. No polling. No git signaling.
King handles routine. God gates major decisions.
