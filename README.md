# ai-incident-war-room

> A live multi-agent simulation of an AI system failing in production in a regulated environment. Five agents coordinate in real time to produce a complete incident response package.

## Try it

**[brianpelow.github.io/ai-incident-war-room](https://brianpelow.github.io/ai-incident-war-room)**

## The scenarios

| Scenario | Severity | The failure |
|----------|----------|-------------|
| The Biased Model | Critical / P0 | A credit decisioning model producing systematically different outcomes for protected classes. 340,000 decisions already processed. |
| The Replay Failure | High / P1 | An OCC examiner requests decision records for 50 AI-driven adverse actions. The records cannot be reconstructed. Examination in 72 hours. |
| The Rogue Agent | Severe / P0 | An autonomous deployment agent pushed a model to production bypassing the CAB gate. No change record. No rollback path. No named owner. |

## The agents

| Agent | What it produces |
|-------|-----------------|
| `TriageAgent` | Severity assessment, blast radius, 2-hour containment actions, escalation matrix |
| `LegalRiskAgent` | Litigation exposure, spoliation risk, adverse action obligations, privilege guidance |
| `RegulatoryExposureAgent` | Frameworks triggered, examination risk, self-disclosure analysis, enforcement precedent |
| `EngineeringRemediationAgent` | Technical root cause, 24h/72h/30-day roadmap, what should have been in place |
| `BoardCommunicationAgent` | Board memo draft in the voice of a CTO taking accountability |

Agents run sequentially. Each downstream agent receives the triage findings as context. The board memo receives all four prior outputs.

## The output

A complete incident response package, available as copyable markdown or PDF. The kind of artifact a real incident command team would produce -- except it takes 90 seconds instead of three days.

## Why this exists

The [ai-governance-framework](https://github.com/brianpelow/ai-governance-framework) argues that 1:1 replay of every AI decision is paramount to staying in business. This war room makes that argument visceral.

Every scenario here is a failure of governance infrastructure that did not exist before it was needed. Run one and the closing line of the [integrated strategy](https://github.com/brianpelow/integrated-strategy) stops being rhetoric:

> The model will not save you. The platform will -- if you build it before you need it.

## Related work

| Repo | What it is |
|------|-----------|
| [ai-governance-framework](https://github.com/brianpelow/ai-governance-framework) | The replay imperative -- the framework these incidents violate |
| [orbit-platform](https://github.com/brianpelow/orbit-platform) | The control plane that would have blocked the rogue deployment |
| [cab-automation](https://github.com/brianpelow/cab-automation) | The CAB gate that was bypassed |
| [IncidentPilot](https://github.com/brianpelow/IncidentPilot) | Production multi-agent incident response |

## License

MIT