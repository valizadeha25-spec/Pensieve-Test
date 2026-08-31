# Agentic System Design

Agentic system design starts with the operator’s knowledge, lived workflow, and judgment rather than with a ready-made agent. The human remains the source of substance; AI amplifies, shapes, and scales it rather than originating it.^\[1\]^ (`data:34`) Designing a system rather than copying one is intended to make it understandable enough to diagnose and repair while building the transferable skill of designing systems.^\[2\]^ (`data:34`)

The concept is still seed-stage and unbounded: it records that it is “seed, not developing” and that its two gates are empty.^\[3\]^ (`data:34`)

## Design loop

### 0. Establish a shared knowledge foundation

Create a durable context layer before a workflow. In the Company Brain build, a layered knowledge base sat underneath every workflow, carrying durable material such as identity, purpose, values, and audience rather than recreating that context for each task.^\[4\]^ (`data:34`) The substrate can be a folder or knowledge base; the mechanism matters less than having something to build on.^\[5\]^ (`data:34`)

### 1. Observe the manual work

Keep doing the work by hand while watching it. Map the actual workflow, record its pain points, and learn which parts matter before designing automation.^\[6\]^ (`data:34`) Start from a felt gap rather than a generic feature request: Negin’s design method treats the question as something that appears when a person feels something wrong, ambiguous, or missing, then moves through why and who.^\[7\]^ (`data:41`)

### 2. Study existing approaches as inputs

Only after the manual workflow is understood, study videos, GitHub, existing products, and other agentic systems. The method places this step after observation and treats what is found as inspiration, never as a copy.^\[8\]^ (`data:34`) A reference-led approach makes that discipline concrete: collect examples for a known reason, identify the component or quality being borrowed, combine selected traits rather than copying one reference, and critique the result against the original direction.^\[9\]^ (`data:103`)

### 3. Build a narrow version and idealize it continuously

Build with AI inside the foundation, then start narrow and iterate. The concrete articulation is: “start narrow, keep idealizing, keep iterating, don’t give up early.”^\[10\]^ (`data:34`) Idealization is not a one-time perfect-state exercise; it is a continuous re-imagining toward the way the operator naturally thinks and wants to work.^\[11\]^ (`data:34`) Add the next workflow only when it is needed, rather than designing an entire department in advance.^\[12\]^ (`data:34`)

### 4. Keep the judgment layer and close the loop

Decide explicitly what remains the operator’s. The method calls this the authenticity core: the operator remains the source.^\[13\]^ (`data:34`) AI can handle aggregation and pattern-detection while people retain approval for consequential actions.^\[14\]^ (`data:236`) The operator also retains selection and taste rather than delegating the direction itself.^\[15\]^ (`data:103`)

A workflow is not mature merely because it can call tools or run without supervision. Define the goal, verify the result against it, stop or retry within a bounded condition, and evaluate tool calls, intermediate behavior, and final output.^\[16\]^ (`data:236`)

## Constraints that keep the system yours

### Synthesize; do not copy

Existing resources are ingredients, not substitutes for thinking. The method is to extract first-principles thinking, analyze the operator’s own problem and workflow, combine lessons, add original ideas, and design that synthesis.^\[17\]^ (`data:34`) Copying a workflow without understanding it creates dependence: when output drifts or breaks, the user may not be able to tell that it is wrong or fix where the problem began, and the user does not build the skill of designing workflows.^\[18\]^ (`data:42`)

### Earn complexity through friction

AI makes building easy, which creates a temptation to add capabilities before they are needed. Amir’s hard-won lesson is that every addition can actively create more failure.^\[19\]^ (`data:42`) Company Brain’s build discipline was to add each road only after its friction had been felt by hand, because every system brings maintenance, cleanup, mental, and token costs.^\[20\]^ (`data:35`)

More instructions are not automatically more reliable. Over-constraining an agent can make it brittle; the recorded repair was to remove instructions and simplify the prompt and environment.^\[21\]^ (`data:35`) Pam’s founding account gives the same lesson: the fix was to simplify and give the model more room rather than add more structure and constraints.^\[22\]^ (`data:37`)

### Own the substrate without assuming a bespoke application

Ownership is the enabler of adaptability: building rather than renting lets the system keep changing its tools, skills, automations, triggers, and workflows.^\[23\]^ (`data:34`) Adaptation does not always mean building more software; the right substrate may be the least layered option that matches the operator’s tolerance for setup and need for portability.^\[24\]^ (`data:105`)

## Architecture boundary

This method is not the same thing as a context-orchestration architecture. A key prior-art comparison is the Interpretable Context Methodology (ICM), a March 2026 paper by Van Clief and McDermott (arXiv 2603.16021) arguing that for sequential, human-reviewed, repeatable workflows a folder hierarchy plus markdown prompts plus local scripts is itself the architecture, formalised as a five-layer context hierarchy, five design principles, and Inputs/Process/Outputs stage contracts.^\[25\]^ (`data:241`) The current concept describes the distinction as provisional: ICM is about how to structure context for an agent, while this method is about how a human decides what to build and where to keep judgment.^\[26\]^ (`data:34`)

ICM is intentionally bounded. Its synthesis excludes real-time multi-agent collaboration, high-concurrency systems, and complex automated branching; it also notes that it has not been tested through a controlled comparison and has been tested within a single model family.^\[27\]^ (`data:241`)

A live crew is the neighbouring architecture rather than a replacement for ICM: one non-editing chief classifies and routes work to specialists with disjoint file ownership and receives summaries from an auditor and the editors, while ICM runs one agent through sequential stage contracts and the crew runs several isolated working contexts in parallel under a control plane.^\[28\]^ (`data:241`) The crew becomes preferable only when work can be partitioned cleanly enough that parallelism is real and reconciliation is cheaper than sequential execution.^\[29\]^ (`data:241`)

Conceptual modeling is an open boundary rather than settled doctrine; as of 2026-08-27, no future ontology has been chosen.^\[30\]^ (`data:185`) A working brainstorm treats ontology and epistemology as design disciplines for agentic AI products and proposes a possible reality layer beneath PAM’s existing project-structure layer, with Person, Commitment, Event, Decision, Dependency, Claim, Outcome, and Constraint as candidate entities.^\[31\]^ (`data:185`) PAM’s current implementation combines a relational work hierarchy with a file/object-storage context layer; whether that separation remains correct, and whether concepts such as Commitment, Decision, Event, Claim, or Risk become structured objects, remain open design questions.^\[32\]^ (`data:185`) The brainstorm remains input to a design conversation and asks Amir to write and maintain PAM’s real technical foundation, architecture, and data-model documentation.^\[33\]^ (`data:185`)

When a design does require several agents, separate responsibility before adding coordination. Sequential work with inspectable handoffs may use file-defined stages; concurrent specialists with live dependencies may need bounded messaging; either architecture still needs explicit jobs, permissions, verification, and recovery.^\[34\]^ (`data:240`) A chief is a control plane, not a more powerful specialist: it surveys the bounded work surface, classifies observed problems, routes each to the specialist who owns that discipline, and recommends the final result while fixing nothing, with specialists editing disjoint files and an auditor reading across the system without editing what it evaluates.^\[35\]^ (`data:240`) The crew's creator guidance also sets scaling thresholds: isolate colliding editors with worktrees, move beyond roughly five live agents into scripted workflow, and use managed infrastructure for unattended schedules and persistent state — with the durable lesson to externalize workflow state once coordination starts dominating the work.^\[36\]^ (`data:240`) Job titles and personas are not the mechanism — the working boundary is scope plus tools plus edit authority plus isolated context plus a return contract, with project-specific facts and rules in a shared house file and portable role behavior in agent definitions.^\[37\]^ (`data:240`) Memory is another separate architecture choice: retrieval-only memory and persistent state are different architectures, and retrofitting true state persistence is not trivial.^\[38\]^ (`data:142`) See [Agent Memory](../agent-memory/page.md) for that layer.

## Lived evidence

Company Brain provides a concrete example of the loop. It began as an empty directory; nothing was designed up front, and each piece was built when friction became real. As the system evolved, recurring thinking was held by the environment rather than redone manually.^\[39\]^ (`data:35`) See [Company Brain](../../systems/company-brain/page.md).

Pam provides a second product-design example: its team mapped the current “doing a project” domain and workflow in detail before designing anything new on top of it.^\[40\]^ (`data:41`) The product question then became how to design around AI rather than simply add AI to project management.^\[41\]^ (`data:65`) These examples demonstrate the method without defining it by Pam’s particular product workflows.

## Current boundary

The method should not yet be presented as a universal recipe. Its open questions are when copy-and-move-on is genuinely the right call, when keeping judgment becomes a bottleneck, and whether manual-first observation makes sense for very small tasks.^\[42\]^ (`data:34`) For now, its durable scope is narrower: understand the work and the system being built, use existing approaches as ingredients, keep the human source of substance and judgment visible, and earn the next layer through observed friction and evaluation.^\[43\]^ (`data:34`)

Related reading: [Human Judgment & Delegation](../human-judgment-delegation/page.md), [Agent Memory](../agent-memory/page.md), [AI Agent Governance](../ai-agent-governance/page.md), [Production Readiness](../production-readiness/page.md), and [Company Brain](../../systems/company-brain/page.md).

## Sources
- [domains/content/journey/concepts/agentic-system-design.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/content/journey/concepts/agentic-system-design.md) (`data:34`)
- [domains/content/journey/negin-product-philosophy.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/content/journey/negin-product-philosophy.md) (`data:41`)
- [wiki/pages/themes/reference-driven-design.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/wiki/pages/themes/reference-driven-design.md) (`data:103`)
- [wiki/pages/themes/ai-marketing-workflows.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/wiki/pages/themes/ai-marketing-workflows.md) (`data:236`)
- [domains/content/journey/teaching-bank.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/content/journey/teaching-bank.md) (`data:42`)
- [domains/content/journey/log.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/content/journey/log.md) (`data:35`)
- [domains/content/journey/founding-story.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/content/journey/founding-story.md) (`data:37`)
- [wiki/pages/themes/software-adapts-to-you.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/wiki/pages/themes/software-adapts-to-you.md) (`data:105`)
- [wiki/pages/syntheses/icm-interpretable-context-methodology.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/wiki/pages/syntheses/icm-interpretable-context-methodology.md) (`data:241`)
- [domains/product/ontology-brainstorm/README.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/product/ontology-brainstorm/README.md) (`data:185`)
- [wiki/pages/themes/ai-agent-teams.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/wiki/pages/themes/ai-agent-teams.md) (`data:240`)
- [wiki/pages/themes/agent-memory.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/wiki/pages/themes/agent-memory.md) (`data:142`)
- [domains/product/philosophy/product-values.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/product/philosophy/product-values.md) (`data:65`)
