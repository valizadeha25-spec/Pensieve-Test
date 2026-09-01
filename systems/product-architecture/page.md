# Product Architecture

PamAI's product architecture separates structured project and execution state in Supabase Postgres from rich contextual knowledge held as files in Supabase Object Storage.^\[1\]^[^data:186]^\[2\]^[^data:186] This is verified current-state grounding rather than a future architecture proposal: recorded on 2026-08-27 from Amir's direct explanation, PAM Web at commit `cc37dbaa`, PAM Desktop at commit `1e9b28d0`, and the current Drizzle schema, in line with the product domain's rule that implementation claims be grounded in Amir's direct account and the current codebase.^\[3\]^[^data:186]^\[4\]^[^data:186]^\[5\]^[^data:184]

## Structured work and execution data

Structured work and execution state lives in Supabase Postgres, with the Drizzle schema as the code-level source of truth.^\[6\]^[^data:186] The product's main work vocabulary is the planning hierarchy `Workspace → Project → Front → Milestone → Batch → Item`, with daily plan entries and weekly allocations beside it as the time/execution layer.^\[7\]^[^data:186]^\[8\]^[^data:186] The hierarchy describes how planned work is broken down; the physical data model is intentionally not a strict tree, because a Milestone may require several Fronts and a Batch may contribute to several Milestones.^\[9\]^[^data:186]^\[10\]^[^data:186] Item is currently the unit of countable work inside PAM.^\[11\]^[^data:186]

| Concept | Stored shape |
|---|---|
| Workspace | Membership and account boundary; can contain multiple projects and members. |
| Project | Belongs to one workspace; holds name, description, visual metadata, lifecycle status, and creator metadata. |
| Front | Belongs to one project; a durable domain or angle of work. |
| Milestone | Belongs to one project; a project-level state that can intentionally link to multiple Fronts through `milestone_fronts`. |
| Batch | Stored in the legacy `workstreams` table but called Batch in the product; belongs to a project, may point to a Front, and can link to multiple Milestones through `workstream_milestones`. |
| Item | The smallest structured unit of project work; belongs to one batch and project, and may link to a milestone, parent item, assignee, status, priority, tags, and dates. |

Item dependencies are directional item-to-item relationships stored in `item_dependencies`.^\[12\]^[^data:186] A daily plan entry is a dated time block for one user that may link to an item but is neither an item nor a strict child of the project hierarchy, while an allocation is a recurring weekly block of project capacity or unavailable time with no work-completion state.^\[13\]^[^data:186]^\[14\]^[^data:186] Postgres also stores the operational records around this model: users, memberships, project shares, conversations, messages, scheduled routines and runs, and integration accounts.^\[15\]^[^data:186]

## File-backed context and memory

Rich context lives as files in Supabase Object Storage, primarily in the private `agent-files` bucket; Postgres stores file metadata, hashes, storage paths, ingestion records, and search/index records, while the document content itself remains file/object data.^\[16\]^[^data:186]^\[17\]^[^data:186] The durable file model gives the main paths distinct roles:

- `memory/user.md` — stable information about the person across projects.^\[18\]^[^data:186]
- `memory/memory.md` — durable cross-project facts, rules, constraints, and context.^\[19\]^[^data:186]
- `project/project.md` — the project's strategic foundation.^\[20\]^[^data:186]
- `project/playbook.md` — instructions for how PAM should organize and maintain the project's knowledge.^\[21\]^[^data:186]
- `project/mind/` — the growing project knowledge layer: named entities, concepts, research, work products, notebooks, lessons, health artifacts, reflection records, and routine state.^\[22\]^[^data:186]

PAM gives the agent filesystem tools to read, search, create, edit, move, and delete authorized files. On Web, files are hydrated from Object Storage into a temporary Daytona runtime and flushed back to durable storage; on Desktop, authorized account and project files are synchronized to a local filesystem and changes are published back through PAM's synchronization system.^\[23\]^[^data:186] This file system is PAM's current equivalent of a persistent context layer.^\[24\]^[^data:186] For the memory model in depth — the three-layer reading and confirmation-gated promotion — see [Agent Memory](../../ai-practice/agent-memory/page.md).

## Boundary and runtime routing

The current placement rule separates the substrates by content type: clear status, owner, dates, dependencies, or scheduling goes to a structured database record, while rich explanation, strategy, research, narrative context, history, or generated work goes to a file.^\[25\]^[^data:186]^\[26\]^[^data:186] The intended benefit is reliable operational structure in Postgres alongside the depth and flexibility the model needs to reason over files — a separation chosen before the team had its practical Company Brain experience, and a current implementation choice rather than a proven final answer.^\[27\]^[^data:186]^\[28\]^[^data:186]

Runtime flows across both substrates:

- Foundation learns the stable project shape through conversation and writes the canonical strategic result to `project.md`, keeping a richer extraction trail in the foundation notebook under `project/mind/`.^\[29\]^[^data:186]^\[30\]^[^data:186]
- Planning reads the foundation and writes Fronts, Milestones, Batches, and Items into Postgres, keeping non-operational rationale and supporting context in files when needed.^\[31\]^[^data:186]^\[32\]^[^data:186]
- In normal conversation, a concrete execution change such as an item starting or finishing should update structured project state, while strategic context, rationale, research, a named person, or a durable lesson should update the appropriate file.^\[33\]^[^data:186]^\[34\]^[^data:186] A message may affect both, but PAM is instructed not to duplicate the same truth blindly across both surfaces; routing is enforced mainly through agent instructions and skills, not one universal data abstraction.^\[35\]^[^data:186]^\[36\]^[^data:186]
- Morning Brief, Fulfillment, Project Health, and Reflection read from both substrates, and the agent interprets them together to decide what matters, what changed, what should happen today, and whether the plan is drifting.^\[37\]^[^data:186]^\[38\]^[^data:186]

## Retrieval, provenance, and authority

PAM does not currently have one unified ontology or query layer spanning all project knowledge.^\[39\]^[^data:186] Structured records are queried through database tools; files are navigated and searched through filesystem tools and the project `mind/map.md` convention; uploaded documents can be chunked and indexed for search, with evidence records in Postgres and content in Object Storage; and conversation history is stored separately, read when recent statements matter. The agent reconciles these sources at runtime using instructions, tool results, and judgment.^\[40\]^[^data:186]^\[41\]^[^data:186]^\[42\]^[^data:186]^\[43\]^[^data:186]^\[44\]^[^data:186]

Provenance is partial: timestamps, creator kind, source metadata, file hashes, message identity, and ingestion/search records exist, but there is not one consistent evidence model applying to every statement in every substrate.^\[45\]^[^data:186] When sources conflict, current instructions tell PAM to surface the conflict rather than silently pick a winner, and imported material remains reference until the user or an authorized workflow accepts its effect on canonical project truth.^\[46\]^[^data:186]^\[47\]^[^data:186] Connectors are migrate-once rather than continuously reconciled — a connector is read once, reports back, the user confirms, and from then on Pam, not the external tool, is authoritative.^\[48\]^[^data:264]

Web and Desktop do not own separate project models: Postgres remains authoritative for structured project data on both surfaces and Object Storage the durable cloud source for files, while Desktop keeps an authorized local copy of files for native agent execution and synchronization.^\[49\]^[^data:186]^\[50\]^[^data:186]^\[51\]^[^data:186]^\[52\]^[^data:186] Desktop SQLite stores Desktop operational state, visible conversations, provider continuity, recovery, and synchronization bookkeeping — it is not a second structured project database — and structured Desktop actions still call authenticated PAM server tools against the same records used by Web.^\[53\]^[^data:186]^\[54\]^[^data:186]

## Open questions and the ontology brainstorm

The current implementation explicitly does not choose a future ontology or authorize a data-model change, and nothing redesigning it has been approved: no knowledge graph, no event-sourced redesign, no migration away from the current hierarchy, and no merger of database and file truth.^\[55\]^[^data:186]^\[56\]^[^data:186]^\[57\]^[^data:186]^\[58\]^[^data:186]^\[59\]^[^data:186] The document leaves open whether the structured hierarchy plus file system remains the right long-term model; whether some information currently held in prose should become typed structured data; whether the two layers need a shared semantic map, evidence layer, or retrieval interface; whether Item remains the lowest fundamental unit of work; and whether a relational, graph, event-based, file-native, or hybrid model best fits PAM.^\[60\]^[^data:186]^\[61\]^[^data:186]^\[62\]^[^data:186]^\[63\]^[^data:186]^\[64\]^[^data:186]

That future direction is explored in [Ontology Exploration](./ontology-exploration/page.md), which tracks the brainstorm itself. In outline, a ChatGPT conversation shared by Negin proposes a candidate ontology of Person, Commitment, Event, Decision, Dependency, Claim, Outcome and Constraint as a possible reality layer underneath PAM's existing project-structure layer,^\[65\]^[^data:185] underpinned by a Claim epistemic object carrying source, timestamp, confidence, provenance, status, and supersedes;^\[66\]^[^data:263] and Claude's companion analysis stress-tests it against recorded product behavior, finding it fits real events while surfacing gaps the abstract proposal could not see: Pam's own onboarding conversation, running in production, elicits a Risk with nowhere to store it as one, and a future Claim/Source model needs an explicit source-lifecycle field (`source_mode: migrated-snapshot | live-observed | user-stated`) or the migration-not-sync connector behavior recorded above gets silently violated.^\[67\]^[^data:264]^\[68\]^[^data:264] The folder remains brainstorm input, not doctrine: no future ontology has been chosen, and whether concepts such as Commitment, Decision, Event, Claim, or Risk become structured objects remains an open design question — one that per the product domain's rule stays open until Amir and Negin explicitly decide it.^\[69\]^[^data:185]^\[70\]^[^data:184]

[^data:186]: [domains/product/philosophy/architecture.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/product/philosophy/architecture.md)
[^data:184]: [domains/product/README.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/product/README.md)
[^data:264]: [domains/product/ontology-brainstorm/claude-analysis.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/product/ontology-brainstorm/claude-analysis.md)
[^data:185]: [domains/product/ontology-brainstorm/README.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/product/ontology-brainstorm/README.md)
[^data:263]: [domains/product/ontology-brainstorm/chatgpt-conversation.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/product/ontology-brainstorm/chatgpt-conversation.md)
