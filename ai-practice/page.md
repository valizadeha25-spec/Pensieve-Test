# AI Practice

AI Practice is PamAI’s durable body of principles and research for designing, contextualizing, delegating, governing, and operating AI-enabled work. Its organizing question is which judgment layer the human should keep while a well-designed system carries everything below it.[^\[1\]^](https://app.pensieve.uk/r/506/data/31)

## From assistance to leverage

AI-enabled work moves beyond chatbot assistance when AI gets access to complex tools and products and is allowed to do the work, while the human keeps the decisions that make the output authentic.[^\[2\]^](https://app.pensieve.uk/r/506/data/42) The leverage claim is about throughput—many jobs running in parallel while the operator does something else—not that any single task is 10x faster.[^\[3\]^](https://app.pensieve.uk/r/506/data/42)

AI should amplify, shape, and scale human substance; it should never originate it.[^\[4\]^](https://app.pensieve.uk/r/506/data/34) Delegation is strongest where work is repeatable, mechanical, or distributable: humans retain approval for consequential actions, and a workflow is ready to delegate when its process and quality bar can be made explicit.[^\[5\]^](https://app.pensieve.uk/r/506/data/296)

## The design discipline

The judgment layer is a function of task difficulty relative to the suitability of the model, harness, and environment or architecture: strong pillars and an easy task allow more deferral; a hard task or weak pillars require the human to keep more judgment.[^\[6\]^](https://app.pensieve.uk/r/506/data/31) Foundational decisions such as data models and architecture stay human-held before downstream work is delegated, because the more foundational and irreversible the decision, the lower the layer the human must personally hold.[^\[7\]^](https://app.pensieve.uk/r/506/data/31)

The build method starts with a shared knowledge foundation before any workflow, observes manual work and its pain points, studies existing approaches as inspiration rather than a copy, then builds narrowly and continuously idealizes toward the operator’s natural way of working.[^\[8\]^](https://app.pensieve.uk/r/506/data/34) Systematization is earned through repeated firsthand friction: the signal to pave a road is friction felt by the operator’s own hands more than once, and every paved road carries maintenance, mental, and token costs.[^\[9\]^](https://app.pensieve.uk/r/506/data/31)

## Context that compounds

Context is the substrate of compounding leverage: better context produces better output, and every conversation can improve the next output when what matters is captured at the right layer rather than one undifferentiated bucket.[^\[10\]^](https://app.pensieve.uk/r/506/data/36)[^\[11\]^](https://app.pensieve.uk/r/506/data/36) Selective persistence is essential: not all context is golden, over-capturing creates context bloat, and one-off task context can remain disposable.[^\[12\]^](https://app.pensieve.uk/r/506/data/36)

[Golden Context](./golden-context/page.md) covers selecting, layering, and reusing context; [Agent Memory](./agent-memory/page.md) covers the runtime architecture of state, retrieval, and learning.

## Delegation with control

The operator keeps the layer that defines meaning and consequences while AI handles volume below; because the layers were designed deliberately, the operator can still tell when the result is wrong.[^\[13\]^](https://app.pensieve.uk/r/506/data/31) A workflow should define a goal, let the agent work, verify the result against the goal, and stop or continue within a bounded condition.[^\[14\]^](https://app.pensieve.uk/r/506/data/296) Maturity is measured, not assumed: a workflow is not mature merely because it can call tools or run without supervision, and knowing whether it performs reliably is a separate capability from building the workflow.[^\[15\]^](https://app.pensieve.uk/r/506/data/296) The operator-facing form of the aggregation-versus-judgment rule is a briefing chain from operating signal → interpretation → bounded action → human review, not a dashboard tour, ending at a decision boundary the operator accepts or changes; the demonstrated briefings are creator-staged examples, not evidence the workflows run reliably.[^\[16\]^](https://app.pensieve.uk/r/506/data/296)

Where delegation extends to several agents, the same control logic applies before orchestration: responsibility is separated before coordination is added, and evaluation is kept independent of the work it judges.[^\[17\]^](https://app.pensieve.uk/r/506/data/311)[^\[18\]^](https://app.pensieve.uk/r/506/data/311) [Multi-Agent Coordination](./multi-agent-coordination/page.md) carries the full pattern set.

Production readiness is the gap between an agent that works in a sandbox and one that works under real conditions.[^\[19\]^](https://app.pensieve.uk/r/506/data/144) The named failure surfaces include context bloat under sustained load, concurrent-user state collapse, memory-replay gaps, cost and latency at scale, and state consistency under concurrent access.[^\[20\]^](https://app.pensieve.uk/r/506/data/144) Verification starts before implementation with verifiable checkpoints and end-to-end tests covering the happy path and two error cases.[^\[21\]^](https://app.pensieve.uk/r/506/data/144)

Governance makes autonomous action observable, policy-bounded, and recoverable through monitoring, policy enforcement, and recovery.[^\[22\]^](https://app.pensieve.uk/r/506/data/97) Persistent state is an accountability concern: a system that cannot remember what it did cannot be audited.[^\[23\]^](https://app.pensieve.uk/r/506/data/142) Runtime controls are a distinct layer from project context: project context can express intent, while a pre-tool control can enforce a command policy before execution and apply it to every new agent without another briefing.[^\[24\]^](https://app.pensieve.uk/r/506/data/311) The governance material is research-backed, not a documented claim of Amir-specific production experience, and the runtime-controls demonstration is staged rather than proof that its checkpoints are sufficient governance.[^\[25\]^](https://app.pensieve.uk/r/506/data/97)[^\[26\]^](https://app.pensieve.uk/r/506/data/311)

## Technical boundary

MCP stays at the integration boundary: its official architecture focuses on context exchange and does not dictate how AI applications use LLMs or manage the context they receive.[^\[27\]^](https://app.pensieve.uk/r/506/data/161) Governance answers what happens when the integration contract is violated, so MCP and governance remain complementary layers rather than substitutes.[^\[28\]^](https://app.pensieve.uk/r/506/data/145)

## Reading this branch

[Agentic System Design](./agentic-system-design/page.md) covers the build loop; [Human Judgment & Delegation](./human-judgment-delegation/page.md) sets the delegation boundary; [AI-Native Work](./ai-native-work/page.md) carries the business-side operating model; [AI Agent Governance](./ai-agent-governance/page.md) and [Production Readiness](./production-readiness/page.md) cover trust and reliable operation; [Multi-Agent Coordination](./multi-agent-coordination/page.md) covers orchestration; [Model Context Protocol](./model-context-protocol/page.md) covers standardized context exchange; [Golden Context](./golden-context/page.md) and [Agent Memory](./agent-memory/page.md) separate reusable context from runtime state. PamAI’s user-facing behavior remains in [Product](../product/page.md); its owned implementation remains in [Systems](../systems/page.md).
