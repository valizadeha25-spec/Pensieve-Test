# Multi-Agent Coordination

Multi-agent coordination is the architecture applied once a system design needs several AI agents: how work is divided among agents, how they hand work to each other, and what keeps the whole inspectable and recoverable. It sits beside [Agentic System Design](../agentic-system-design/page.md), which owns the human-led method for deciding what to build and where judgment stays.

The pattern set comes from a wiki synthesis of 16 sources on agent teams[^\[1\]^](https://app.pensieve.uk/r/506/data/297) and a control-plane synthesis for a persistent marketing strategist.[^\[2\]^](https://app.pensieve.uk/r/506/data/270) Both draw on creator write-ups and one inspected repository.[^\[3\]^](https://app.pensieve.uk/r/506/data/270) The sources repeatedly caveat that specific claims are creator recommendations rather than comparative evidence,[^\[4\]^](https://app.pensieve.uk/r/506/data/297) and the chief-of-staff pattern's reported demo — 14 discovered problems, four specialists completing in 27 minutes — is not independently reproduced or Pam-validated.[^\[5\]^](https://app.pensieve.uk/r/506/data/270)

## Specialize before orchestrating

Useful agent teams separate responsibility before they add coordination.[^\[6\]^](https://app.pensieve.uk/r/506/data/297) A broad “do everything” agent inherits the same ambiguity and attention problems as an overloaded human role.[^\[7\]^](https://app.pensieve.uk/r/506/data/297) One source's construction order for a content team runs role, workflows/SOPs, steps, tested skills, agents, explicit handoffs, with human QC between roles as part of the handoff contract rather than an implied final glance — though that source defines no permissions, recovery, or objective evaluation method.[^\[8\]^](https://app.pensieve.uk/r/506/data/297)

## Bounded jobs and working boundaries

Job titles and personas are not the mechanism. The working boundary is scope plus tools plus edit authority plus isolated context plus a return contract.[^\[9\]^](https://app.pensieve.uk/r/506/data/297) Project-specific facts and rules live in the shared house file, while portable role behavior lives in the agent definition.[^\[10\]^](https://app.pensieve.uk/r/506/data/297) The control-plane synthesis extends this layering: project-specific truth in the house file, portable role preferences in the agent definition, per-initiative evidence as per-run working context, and persistent initiative state in a durable substrate rather than hidden conversation memory.[^\[11\]^](https://app.pensieve.uk/r/506/data/270)

## The non-editing chief as control plane

In the chief-of-staff crew pattern, the chief surveys a bounded work surface, classifies observed problems, writes a visible board, routes each problem to the specialist who owns that discipline, waits for all reports, and recommends the final result — the chief fixes nothing.[^\[12\]^](https://app.pensieve.uk/r/506/data/297) Specialists edit disjoint files; the auditor reads across the system and does not edit the code it evaluates.[^\[13\]^](https://app.pensieve.uk/r/506/data/297) A persistent agent built on this pattern should own objectives and constraints, the initiative and experiment portfolio, decision-ready briefs, routing, reconciliation, and learning from evidence — while execution and audit remain independently owned and state lives outside its context window.[^\[14\]^](https://app.pensieve.uk/r/506/data/270)

## File-defined stages versus live delegation

The useful distinction is workflow shape, not “one agent versus many”: sequential work with inspectable handoffs may need only file-defined stage contracts; concurrent specialists with live dependencies can use bounded messaging; either architecture without explicit jobs, permissions, verification, and recovery multiplies ambiguity.[^\[15\]^](https://app.pensieve.uk/r/506/data/297) Where agents do message, coordination is a narrow interface — dependency updates and targeted questions carried as a short note rather than the whole conversation or all files — not ambient shared memory.[^\[16\]^](https://app.pensieve.uk/r/506/data/297)

## Staged briefings as visible handoffs

A staged briefing pattern makes a bounded handoff visible: identify a repeated feature request, hand the already approved direction to a developer agent, then return the implementation for human review.[^\[17\]^](https://app.pensieve.uk/r/506/data/297) As a demo grammar — show the observable trigger, name the owner, show the returned artifact, and stop at the approval boundary — it is a presentation of role boundaries, not a proof that delegation replaces audit, permissions, or recovery, and it does not validate the specific integrations, completion rate, or implementation quality.[^\[18\]^](https://app.pensieve.uk/r/506/data/297)

## Coordination scaling thresholds

The guidance is worktree isolation when editors can collide, a scripted workflow once live delegation grows beyond roughly five agents, and managed infrastructure for unattended, scheduled work with persistent state.[^\[19\]^](https://app.pensieve.uk/r/506/data/297) The “roughly five” threshold is artifact guidance, not a measured performance boundary; the durable lesson is to externalize workflow state when coordination starts dominating the work.[^\[20\]^](https://app.pensieve.uk/r/506/data/270) Persistent execution adds lifecycle ownership: context thresholds, restart conditions, handoff artifacts, and failure recovery must be explicit before a daemon makes the system more reliable.[^\[21\]^](https://app.pensieve.uk/r/506/data/297) Retained project context and a monitor role also solve different jobs — context reduces repeated re-briefing, the monitor organizes concurrent work[^\[22\]^](https://app.pensieve.uk/r/506/data/297) — and a shared skill library solves distribution, not coordination.[^\[23\]^](https://app.pensieve.uk/r/506/data/297)

## Independent evaluation

Review must be independent by design: asking the same conversation to critique its own output preserves the context and assumptions that produced the mistake,[^\[24\]^](https://app.pensieve.uk/r/506/data/297) so reviewers get the artifact, acceptance criteria, and a bounded lens without inheriting the creator's whole rationale.[^\[25\]^](https://app.pensieve.uk/r/506/data/297) In the control-plane loop, an independent evaluator compares the result with the predeclared experiment contract before a keep, revise, stop, or escalate decision.[^\[26\]^](https://app.pensieve.uk/r/506/data/270)

## Related pages

Governance surfaces — permissions, audit, recovery, data isolation — belong to [AI Agent Governance](../ai-agent-governance/page.md); memory and durable state to [Agent Memory](../agent-memory/page.md); the human-delegated counterpart to agent orchestration is [Human Judgment & Delegation](../human-judgment-delegation/page.md).
