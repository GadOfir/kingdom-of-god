---
name: kingdom-of-god
description: >
  Skill router built on Adversarial Alignment. Persona matrix: God (supreme leader)
  sets direction, King (orchestrator) routes work + reads CONTRACTX, Workers execute
  with fresh context windows. Routes between GodsPlan, Shit Hit The Fan, CONTRACTX,
  Agent Retro, TechDebt. LOS provides optional long-term memory.
  Every skill works standalone; the wiring below is advisory — use a skill if it is
  installed, otherwise use your own equivalent.
argument-hint: "[route | status]"
---

# Kingdom of God — Skill Router

Adversarial Alignment in practice. God sets direction. King orchestrates.
Workers execute with clean context.

## Standalone-first

Every skill in this map runs on its own. Nothing here is a hard dependency.
The connections are **advice, not requirements**:

- **Use a skill if it is present.** "If CONTRACTX is installed, walk it. If not,
  route from your own specs." Same for every other pairing below.
- **No skill is required by another.** Install one, some, or all. Each degrades
  gracefully to its own inputs when a sibling is absent.
- **Wiring is a suggestion the King makes**, not a gate that blocks work.

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

Every skill is optional and usable on its own. Install what you need.

| Stage | Skill | Trigger | Invocation |
|---|---|---|---|
| Planning | GodsPlan | New work. Define the surface, author a property-based plan. | Operator |
| Triage | Shit Hit The Fan | Something broke. Route to the right fix. | User-only (automate later) |
| Contracts | CONTRACTX | Rules need enforcing. Walk before edit. | Model or user |
| Learning | Agent Retro | Session ended. Triage what the agent got wrong. | Operator |
| Drift | TechDebt | Recurring debt. Scan the codebase for architecture drift. | User / CI |
| Memory | LOS (optional) | Long-term wiki. Cross-session, cross-project. | Reads on demand |

### Filing contracts across skills

When CONTRACTX is present, any skill (Agent Retro, TechDebt, a Worker) **may file a
CX gap** through the normal gap workflow — tag the source and dedupe before writing.
The King owns *resolving* gaps. When CONTRACTX is absent, each skill records its
finding wherever your project already keeps rules. No single mandatory writer.

## Plug-in Skills

Workers can pull in external skills so the King doesn't run everything.
Reference a skill by link (always latest), then wire it to an upper skill so it
fires at the right stage. Example: improve-codebase-architecture → Agent Retro
(the agent checks whether the architecture stayed clean during the retro).

## LOS — Memory Layer (optional)

LOS is its own standalone system. If you run it, the Kingdom can use it as long-term
memory — if you don't, everything else still works. When present:

- **Retention policy:** What stays, what expires. identity.md (permanent),
  knowledge/ (permanent), logs/ (retention window), tasks/ (archive on completion).
- **Ingest policy (advisory):** *If LOS is present*, King reads it for context.
  Operational Workers don't — fresh windows. *If Agent Retro is present*, it writes
  learnings back. SHTF reads incident history. Gap resolutions land in LOS if you keep
  them there. None of this is required — skip any hook whose skill you haven't installed.
- **Autonomy note:** LOS's own "never stop" loop is scoped to LOS. Under the Kingdom,
  God gates major decisions — God-gating wins over LOS autonomy.
- **Cross-project:** `.claude.los` file links any project to your LOS repo.

## Handoff Protocol

1. God sets direction — what's the real use case?
2. King reads CONTRACTX + LOS *if present* — knows rules, boundaries, history
3. King routes to Workers — paste-ready prompts (or handles directly if smart enough)
4. Workers execute — clean context, contract-bound, return diff
5. King reviews → asks God "deploy?" → pushes → verifies

No automation. No polling. No git signaling.
King handles routine. God gates major decisions.
