# Product Architecture

As last verified on 2026-08-27^\[1\]^ (`data:186`), PamAI’s current product architecture separates structured project and execution data in Supabase Postgres^\[2\]^ (`data:186`) from rich contextual knowledge in Supabase Object Storage^\[3\]^ (`data:186`). The architecture is current-state technical grounding, not a future architecture proposal.^\[4\]^ (`data:186`)

## Structured work and execution

Structured work and execution state lives in Supabase Postgres, with the Drizzle schema as the code-level source of truth.^\[5\]^ (`data:186`) The main work vocabulary is `Workspace → Project → Front → Milestone → Batch → Item`; daily plan entries and weekly allocations sit beside that hierarchy as the time/execution layer.^\[6\]^ (`data:186`)

The product explanation is hierarchical, but the physical data model is intentionally not a strict tree: a Milestone may require several Fronts, and a Batch may contribute to several Milestones.^\[7\]^ (`data:186`) Item is currently the unit of countable work inside PAM.^\[8\]^ (`data:186`) The main records are:

- Workspace is the membership and account boundary and can contain multiple projects and members.^\[9\]^ (`data:186`)
- Project belongs to one workspace and carries its name, description, visual metadata, lifecycle status, and creator metadata.^\[10\]^ (`data:186`)
- Front belongs to one project and represents a durable domain or angle of work.^\[11\]^ (`data:186`)
- Milestone belongs to a project and can intentionally link to multiple Fronts; it is project-level state rather than something owned by one Front.^\[12\]^ (`data:186`)
- Batch is stored in the legacy `workstreams` table, belongs to a project, may point to a Front, and can intentionally link to multiple Milestones.^\[13\]^ (`data:186`)
- Item is the smallest structured unit of project work. It belongs to a Batch and Project and may carry a milestone link, parent item, assignee, status, priority, tags, and dates.^\[14\]^ (`data:186`)

Item dependencies are directional item-to-item relationships. Daily plan entries are dated user time blocks rather than items or strict children of the project hierarchy, while allocations represent recurring project capacity or unavailable time and have no work-completion state.^\[15\]^ (`data:186`) Postgres also stores the operational records around this model, including users, memberships, project shares, conversations, messages, scheduled routines and runs, and integration accounts.^\[16\]^ (`data:186`)

## File-backed context

Rich context lives as files in the private `agent-files` bucket in Supabase Object Storage. Postgres stores file metadata, hashes, storage paths, ingestion records, and search/index records, while the document content remains file/object data.^\[17\]^ (`data:186`) The durable file model gives the main paths distinct roles:

- `memory/user.md` holds stable information about the person across projects, while `memory/memory.md` holds durable cross-project facts, rules, constraints, and context.^\[18\]^ (`data:186`)
- `project/project.md` holds the project’s strategic foundation, and `project/playbook.md` contains instructions for how PAM should organize and maintain that project’s knowledge.^\[19\]^ (`data:186`)
- `project/mind/` is the growing project knowledge layer for named entities, concepts, research, work products, notebooks, lessons, health artifacts, reflection records, and routine state.^\[20\]^ (`data:186`)

PAM gives the agent filesystem tools to read, search, create, edit, move, and delete authorized files. On Web, files are hydrated from Object Storage into a temporary Daytona runtime and flushed back to durable storage; on Desktop, authorized account and project files are synchronized to a local filesystem and then published through PAM’s synchronization system.^\[21\]^ (`data:186`) This file system is PAM’s current equivalent of a persistent context layer.^\[22\]^ (`data:186`)

## Boundary and runtime routing

The current placement rule is operationally simple: clear status, owner, dates, dependencies, or scheduling belongs in a structured database record^\[23\]^ (`data:186`), while rich explanation, strategy, research, narrative context, history, or generated work belongs in a file.^\[24\]^ (`data:186`) The intended benefit is reliable operational structure in Postgres alongside the depth and flexibility needed for model reasoning in files, but the separation is a current implementation choice rather than a proven final answer.^\[25\]^ (`data:186`)

Foundation learns the stable project shape through conversation and writes the canonical strategic result to `project.md`, retaining a richer extraction trail in the foundation notebook under `project/mind/`.^\[26\]^ (`data:186`) Planning reads that foundation and writes Fronts, Milestones, Batches, and Items into Postgres, while non-operational rationale and supporting context remain in files when needed.^\[27\]^ (`data:186`)

Normal conversation routes a concrete execution change, such as an item starting or finishing, to structured project state; strategic context, rationale, research, a named person, or a durable lesson goes to the appropriate file. A message may affect both, but PAM is instructed not to duplicate the same truth blindly across both surfaces. This routing is currently enforced mainly through agent instructions and skills, not through one universal data abstraction.^\[28\]^ (`data:186`) Morning Brief, Fulfillment, Project Health, and Reflection read from both substrates, and the agent interprets them together to decide what matters, what changed, what should happen today, and whether the plan is drifting.^\[29\]^ (`data:186`)

## Retrieval, provenance, and authority

PAM does not currently have one unified ontology or query layer spanning all project knowledge.^\[30\]^ (`data:186`) Structured records are queried through database tools; files are navigated and searched through filesystem tools and the project `mind/map.md` convention; uploaded documents can be chunked and indexed for search; and conversation history is stored separately. The agent reconciles these sources at runtime using instructions, tool results, and judgment.^\[31\]^ (`data:186`)

Provenance is partial: timestamps, creator kind, source metadata, file hashes, message identity, and ingestion/search records exist, but there is not one consistent evidence model for every statement in every substrate.^\[32\]^ (`data:186`) When sources conflict, current instructions tell PAM to surface the conflict rather than silently pick a winner. Imported material remains reference until the user or an authorized workflow accepts its effect on canonical project truth.^\[33\]^ (`data:186`)

Web and Desktop do not own separate project models.^\[34\]^ (`data:186`) Postgres remains authoritative for structured project data on both surfaces, Object Storage remains the durable cloud source for files, and Desktop keeps an authorized local copy for native agent execution and synchronization. Desktop SQLite stores operational state, visible conversations, provider continuity, recovery, and synchronization bookkeeping; it is not a second structured project database. Structured Desktop actions call authenticated PAM server tools against the same records used by Web.^\[35\]^ (`data:186`)

## Open architecture questions

The current implementation does not choose a future ontology or authorize a data-model change.^\[36\]^ (`data:186`) A separate ontology brainstorm is explicitly “a working exploration, not standing doctrine.”^\[37\]^ (`data:185`) It proposes a candidate reality layer of Person, Commitment, Event, Decision, Dependency, Claim, Outcome, and Constraint beneath PAM’s existing project-structure layer, but no future ontology has been chosen.^\[38\]^ (`data:185`)

Open questions include whether the structured hierarchy and file system remain the right long-term model, whether information now held in prose should become typed structured data, whether both layers need a shared semantic map, evidence layer, or retrieval interface, whether Item remains the lowest fundamental unit of work, and whether a relational, graph, event-based, file-native, or hybrid model best fits PAM.^\[39\]^ (`data:186`) No knowledge graph, event-sourced redesign, migration away from the current hierarchy, or merger of database and file truth has been approved.^\[40\]^ (`data:186`)

## Sources
- [domains/product/philosophy/architecture.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/product/philosophy/architecture.md) (`data:186`)
- [domains/product/ontology-brainstorm/README.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/product/ontology-brainstorm/README.md) (`data:185`)
