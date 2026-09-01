# Multi-Agent Coordination

Multi-agent coordination is the architecture applied once a system design needs several AI agents: how work is divided among agents, how they hand work to each other, and what keeps the whole inspectable and recoverable. It sits beside [Agentic System Design](../agentic-system-design/page.md), which owns the human-led method for deciding what to build and where judgment stays.

The pattern set comes from a wiki synthesis of 14 sources on agent teams^\[1\]^[^data:240] and a control-plane synthesis for a persistent marketing strategist.^\[2\]^[^data:270] Both draw on creator write-ups and one inspected repository; the sources repeatedly caveat that specific claims are creator recommendations rather than comparative evidence,^\[3\]^[^data:240] and the chief-of-staff pattern's reported demo — 14 discovered problems, four specialists completing in 27 minutes — is not independently reproduced or Pam-validated.^\[4\]^[^data:270]

## Specialize before orchestrating

Useful agent teams separate responsibility before they add coordination.^\[5\]^[^data:240] A broad “do everything” agent inherits the same ambiguity and attention problems as an overloaded human role.^\[6\]^[^data:240] One source's construction order for a content team runs role, workflows/SOPs, steps, tested skills, agents, explicit handoffs — with human QC between roles as part of the handoff contract rather than an implied final glance^\[7\]^[^data:240] — though it defines no permissions, recovery, or objective evaluation method.

## Bounded jobs and working boundaries

Job titles and personas are not the mechanism. The working boundary is scope plus tools plus edit authority plus isolated context plus a return contract.^\[8\]^[^data:240] Project-specific facts and rules live in the shared house file, while portable role behavior lives in the agent definition.^\[9\]^[^data:240] The control-plane synthesis extends this layering: project truth in the house file, portable policy in the agent definition, per-initiative evidence as per-run working context, and persistent initiative state in a durable substrate rather than hidden conversation memory.^\[10\]^[^data:270]

## The non-editing chief as control plane

In the chief-of-staff crew pattern, the chief surveys a bounded work surface, classifies observed problems, writes a visible board, routes each problem to the specialist who owns that discipline, waits for all reports, and recommends the final result — the chief fixes nothing.^\[11\]^[^data:240] Specialists edit disjoint files; the auditor reads across the system and does not edit the code it evaluates.^\[12\]^[^data:240] A persistent agent built on this pattern should own objectives and constraints, the initiative and experiment portfolio, decision-ready briefs, routing, reconciliation, and learning from evidence — while execution and audit remain independently owned and state lives outside its context window.^\[13\]^[^data:270]

## File-defined stages versus live delegation

Coordination architecture follows workflow shape, not “one agent versus many”: sequential work with inspectable handoffs may need only file-defined stage contracts; concurrent specialists with live dependencies can use bounded messaging; either architecture without explicit jobs, permissions, verification, and recovery multiplies ambiguity.^\[14\]^[^data:240] Where agents do message, coordination is a narrow interface — dependency updates and targeted questions carried as a short note — not ambient shared memory.^\[15\]^[^data:240]

## Coordination scaling thresholds

The guidance is worktree isolation when editors can collide, a scripted workflow once live delegation grows beyond roughly five agents, and managed infrastructure for unattended, scheduled work with persistent state.^\[16\]^[^data:240] The “roughly five” threshold is artifact guidance, not a measured performance boundary; the durable rule is to externalize workflow state when coordination starts dominating the work.^\[17\]^[^data:270] Persistent execution adds lifecycle ownership: context thresholds, restart conditions, handoff artifacts, and failure recovery must be explicit before a daemon makes the system more reliable.^\[18\]^[^data:240] Retained project context and a monitor role also solve different jobs — context reduces repeated re-briefing, the monitor organizes concurrent work^\[19\]^[^data:240] — and a shared skill library solves distribution, not coordination.^\[20\]^[^data:240]

## Independent evaluation

Review must be independent by design: asking the same conversation to critique its own output preserves the context and assumptions that produced the mistake,^\[21\]^[^data:240] so reviewers get the artifact, acceptance criteria, and a bounded lens without inheriting the creator's whole rationale.^\[22\]^[^data:240] In the control-plane loop, an independent evaluator compares the result with the predeclared experiment contract before a keep, revise, stop, or escalate decision.^\[23\]^[^data:270]

## Related pages

Governance surfaces — permissions, audit, recovery, data isolation — belong to [AI Agent Governance](../ai-agent-governance/page.md); memory and durable state to [Agent Memory](../agent-memory/page.md); the human-delegated counterpart to agent orchestration is [Human Judgment & Delegation](../human-judgment-delegation/page.md).

[^data:240]: [wiki/pages/themes/ai-agent-teams.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/wiki/pages/themes/ai-agent-teams.md)
[^data:270]: [wiki/pages/syntheses/persistent-strategist-control-plane.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/wiki/pages/syntheses/persistent-strategist-control-plane.md)
