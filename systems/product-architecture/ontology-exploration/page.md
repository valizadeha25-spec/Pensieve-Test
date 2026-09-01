# Ontology Exploration

Ontology Exploration tracks the open question of whether PAM should grow a structured "reality layer" beneath its existing project-structure layer — the brainstorm material arguing for it, the stress test run against it, and the unresolved decision that would turn any of it into doctrine. It is exploratory by design and distinct from [Product Architecture](../page.md), which owns the verified current-state architecture and approved data model.

**Status:** no future ontology has been chosen. Whether the current separation of a relational work hierarchy from a file/object-storage context layer remains correct, and whether concepts such as Commitment, Decision, Event, Claim or Risk become structured objects, are open design questions; the brainstorm folder remains input, not doctrine.^\[1\]^[^data:185]

## Where the material came from

Negin explored ontology and epistemology as design disciplines for agentic AI products (referencing Palantir's Ontology and AWS Context among others) with ChatGPT, applying that lens to what PAM is trying to be — not another PM tool, but infrastructure that absorbs coordination work itself.^\[2\]^[^data:185] Mid-conversation, a question about PAM's actual data model was put to the Company Brain, answered from the brain's own documentation and evidence, and fed back into the conversation — after which ChatGPT proposed a candidate ontology of Person, Commitment, Event, Decision, Dependency, Claim, Outcome and Constraint as a possible reality layer underneath PAM's existing project-structure layer.^\[3\]^[^data:185]

The brainstorm folder hands the whole thread to Amir as onboarding material with an explicit ask: he is to write and maintain the authoritative technical foundation, architecture and data-model documentation of PAM from his own knowledge of the actual system, not from product-side inference.^\[4\]^[^data:185] Claude's companion analysis is explicitly analysis, not a spec: Part 1 was answered from the brain alone, before Negin brought the ChatGPT conversation in,^\[5\]^[^data:264]^\[6\]^[^data:264] and everything in it is inference from the outside pending Amir's confirmation of the actual engineering model.^\[7\]^[^data:264]

## The candidate ontology (v0.1)

ChatGPT's first draft, PAM Ontology v0.1, keeps PROJECT pursuing an OUTCOME through COMMITMENT as the spine, adds PERSON, TIME, ARTIFACT, EVENT, DECISION, CONSTRAINT, ASSUMPTION and RISK around it, and underpins everything with a CLAIM object carrying source, timestamp, confidence, provenance, status and supersedes.^\[8\]^[^data:263]^\[9\]^[^data:263] Its central argument is that facts, beliefs, decisions, commitments, assumptions, goals, events and constraints are different epistemic and ontological types — an LLM sees them all as sentences, and PAM should not.^\[10\]^[^data:263] On sequencing it recommends ontology first, storage architecture second, so engineering can afterwards choose relational tables, graph edges, an event store, typed objects or another substrate.^\[11\]^[^data:263] Existing surfaces — Front, Milestone, Plan, Morning Brief, Routine — would partly become views and computations generated from that reality rather than the only reality PAM knows.^\[12\]^[^data:263]

ChatGPT's own assessment of where PAM stands: the experience vision is quite close, but the underlying ontology is halfway there — strong representations for project, structure, milestones, time, sources and memory, but weak or no first-class representation for people relationships, commitments, events, dependencies, decisions, assumptions, risks and changing truth.^\[13\]^[^data:263]

## Stress test against recorded behavior

Claude's Part 2 stress-tested the proposed entity set against real things that happened around PAM that week, using primary sources ChatGPT did not have — it was working from a summary and had no access to the repo's primary sources.^\[14\]^[^data:264] The proposed ontology passed: every real event expresses cleanly as Person / Commitment / Event / Decision / Dependency / Claim, nothing forced.^\[15\]^[^data:264] A notable validation signal came from outside the product: every collab/ thread in the repo already carries a status: waiting-for-<person> field — a hand-maintained Commitment-like primitive, arrived at independently.^\[16\]^[^data:264]

The test also surfaced three gaps the proposal must resolve:

- **Risk has nowhere to live.** Pam's own onboarding conversation, already running in production, elicits a Risk and a Decision-in-progress from the user and then has nowhere to put them except inside prose in a notebook.^\[17\]^[^data:264]
- **Source lifecycle is missing from the Claim model.** ChatGPT's Claim has a source and a status but no notion of whether that source is a frozen one-time pull or live-watched. Without encoding it, the migration-not-sync decision — where once a connector reports back, PAM rather than the external tool is authoritative — gets silently violated. The proposed fix is a source_mode of migrated-snapshot, live-observed or user-stated, keeping this a deliberate per-claim choice rather than an accident of the storage layer.^\[18\]^[^data:264]^\[19\]^[^data:264]
- **About Your Human versus Person.** ChatGPT's Person entity and PAM's existing per-person profile (Profile / Working Preferences / Goals / Constraints) do overlapping work; whether Person absorbs About Your Human or the two stay separate should be decided explicitly.^\[20\]^[^data:264]

## The open decision

The proposal is real architecture input for Amir's system, arriving while he rebuilds structure for Desktop — but it is his domain to receive, not Negin's or Claude's to hand over finished.^\[21\]^[^data:264] Whether any of this becomes doctrine, and what PAM's authoritative data model actually is underneath its observed behavior, can only be settled by him documenting the actual system; until then this page records the exploration, and current state stays on [Product Architecture](../page.md). The ontology-as-design-lens also informs [Agentic System Design](../../../ai-practice/agentic-system-design/page.md).

[^data:185]: [domains/product/ontology-brainstorm/README.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/product/ontology-brainstorm/README.md)
[^data:264]: [domains/product/ontology-brainstorm/claude-analysis.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/product/ontology-brainstorm/claude-analysis.md)
[^data:263]: [domains/product/ontology-brainstorm/chatgpt-conversation.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/product/ontology-brainstorm/chatgpt-conversation.md)
