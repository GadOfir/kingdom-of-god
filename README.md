# Kingdom of God

**Adversarial Alignment in practice.** Steer models with real-world use cases,
not code. God rules. King orchestrates. Workers execute with fresh context.

## The persona matrix

| Role | Edge | What |
|---|---|---|
| **God** | Ultimate context | Sets direction. The supreme leader. |
| **King** | CONTRACTX + context | Walks contracts. Routes work. Deploys. |
| **Workers** | Fresh context, no bias | One prompt. Full task. Return diff. |

## The skills

| Skill | Stage | URL |
|---|---|---|
| GodsPlan | Planning | https://gadofir.github.io/godsplan/ |
| Shit Hit The Fan | Triage | https://gadofir.github.io/shit-hit-the-fan/ |
| CONTRACTX | Contracts | https://gadofir.github.io/contractx-starter/ |
| Agent Retro | Learning | https://gadofir.github.io/agent-retro/ |
| LOS | Memory (optional) | https://gadofir.github.io/LOS-starter/ |

## Plug-in skills

You don't have to make the King run everything. Drop external skills into the
registry below the Workers — Workers pull them in on demand, so the King stays
focused on routing and contracts.

- **Reference by link, not by copy.** Point to a skill's repo/page and the agent
  fetches the latest version every run — no stale copies.
- **Wire each plug-in to an upper skill** so it fires at the right stage.

Example: wire [improve-codebase-architecture](https://github.com/mattpocock/skills/tree/main/skills/engineering/improve-codebase-architecture)
to **Agent Retro** — during the retro the agent references what a good
architecture looks like and checks whether its changes drifted the structure.

## LOS — Memory Layer

Optional LLM wiki. Retention policy governs what persists. Ingest policy
governs what reads/writes. Cross-project via `.claude.los` file.

## Quick start

```bash
git clone https://github.com/GadOfir/kingdom-of-god.git
cp SKILL.md .claude/skills/kingdom-of-god/
```

Tell your agent: **"Route this through Kingdom of God."**

## Adversarial Alignment

Models learn wrong from code. A code snippet is as likely to be a bug as a
feature. Steer the model with real-world use cases — human workflows, actual
decisions, genuine tradeoffs. God defines the scenario. King contextualizes.
Workers execute without code-pattern bias.

## License

MIT
