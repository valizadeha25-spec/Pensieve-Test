# Production Readiness

Production readiness tracks the demo-to-production gap: the delta between an AI agent that works in a sandbox and one that works under real conditions.^\[1\]^ (`data:144`) A scout synthesis found all five clusters independently asking how to take what works in the demo and make it work when real users hit it.^\[2\]^ (`data:140`) The focus here is the engineering behavior and verification needed to cross that boundary. For the deeper memory subject, see [Agent Memory](../agent-memory/page.md); governance is covered separately in [AI Agent Governance](../ai-agent-governance/page.md).

## Failure surfaces beyond the sandbox

The documented failure surfaces are named explicitly rather than collapsed into a generic claim that an agent breaks in production.^\[3\]^ (`data:144`)

- **Context bloat under sustained load.** As conversations lengthen, context windows fill; an agent that works flawlessly in a 5-turn demo can break at turn 50 when the context is saturated.^\[4\]^ (`data:144`)
- **Concurrent-user state collapse.** Single-user sandbox testing does not reveal race conditions, shared state conflicts, or queue saturation; production adds concurrency.^\[5\]^ (`data:144`)
- **Memory replay gaps.** An agent that remembers everything during a single session can forget it all on restart; true persistence requires an explicit memory layer.^\[6\]^ (`data:144`) See [Agent Memory](../agent-memory/page.md) for the deeper treatment of this surface.
- **Cost and latency at scale.** The contrast is explicit: a demo runs 10 queries while production runs 10,000; token costs can become untenable and latency that feels acceptable in a sandbox compounds under real load.^\[7\]^ (`data:144`)
- **Shared-state consistency.** Even with one user, state that works in a sequential demo can fail when multiple agents read and write the same state simultaneously in a multi-agent architecture.^\[8\]^ (`data:144`)

## Verification gates

The verification framework starts before implementation: design verifiable checkpoints before writing code and use end-to-end tests for the happy path plus two error cases as verification gates, rather than relying on unit tests that are too implementation-specific to sanity-check.^\[9\]^ (`data:144`)

Verification should also match the part being changed. The framework distinguishes leaf nodes, which are safe to vibe code and verify with tests, from trunks, which are core architecture where every line should be read.^\[10\]^ (`data:144`)

These gates make the production boundary concrete: a controlled prototype must be tested against the sustained-load, concurrency, restart, shared-state, and scale conditions that its sandbox can conceal.^\[11\]^ (`data:144`)

## Sources
- [wiki/pages/themes/demo-to-production-gap.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/wiki/pages/themes/demo-to-production-gap.md) (`data:144`)
- [wiki/pages/syntheses/linkedin-scout-2026-06-16.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/wiki/pages/syntheses/linkedin-scout-2026-06-16.md) (`data:140`)
