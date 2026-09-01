# Company Brain

Company Brain is a layered AI work environment: its context taxonomy separates foundational instructions, domain material, skills, database state, and provisional memory, while its workflows turn captured material into reusable artifacts.^\[1\]^[^data:31] ^\[2\]^[^data:241]

## Layered context architecture

The system’s central move is layered scope: the human designs the layers and the AI sorts context against them. The working taxonomy puts `CLAUDE.md` and `RESOLVER.md` in the most fundamental, ~always-loaded layer; `core/` below it; `domains/<x>/` and skills files at narrower scopes; database rows for tracked and queryable state; and `memory/` as provisional material that can be promoted when it proves durable.^\[3\]^[^data:31]

An ICM comparison describes Company Brain as structurally ICM-shaped. Stable reference is mapped to `wiki/pages/`, `domains/`, `memory/learnings/`, and `core/`, while per-run artifacts are mapped to `posts` rows in Supabase; the two-substrate rule treats files as stable reference and the database as per-run working state.^\[4\]^[^data:241] Company Brain’s `wiki_item_links` and `post_library_provenance` provide a working, if partially populated, implementation of output provenance from published posts back to library and wiki sources.^\[5\]^[^data:241] The same comparison identifies unfinished infrastructure: no enforced Inputs/Process/Outputs stage contracts, no incremental recompilation tracking, and no phrase-level provenance within a single post.^\[6\]^[^data:241]

## Control plane: the proposed next layer

A pending Company Brain synthesis proposes extending the system beyond context holding: a persistent strategist role designed as a control plane that owns direction, the initiative portfolio, experiment contracts, routing, reconciliation, and learning, and routes execution to bounded specialists instead of producing content itself.^\[7\]^[^data:270] Its initiative loop runs from strategy state through one bounded, predeclared experiment to routing, independent evaluation, and a decision written back to durable state before the next loop opens.^\[8\]^[^data:270] The state boundary it proposes maps directly onto the layered architecture above: project truth in the house file, portable role behavior in the agent definition, initiative evidence as per-run context, specialist summaries returning to the control plane rather than merging whole contexts, and durable initiative state in a substrate that outlives any context window rather than in conversation memory.^\[9\]^[^data:270] It builds on a chief-of-staff crew pattern whose ICM comparison adds as a neighbouring architecture — a non-editing chief routing specialists with disjoint file ownership under a control plane — alongside the live scaling guidance to isolate colliding editors with worktrees and move beyond roughly five live agents into scripted workflow.^\[10\]^[^data:241] The strategist proposal itself is explicitly not validated: it applies a pattern demonstrated only on a website-repair crew, and its claims are not independently reproduced Pam outcomes.^\[11\]^[^data:270] For the broader doctrine, see [Agentic System Design](../../ai-practice/agentic-system-design/page.md).

## Earned infrastructure

The content system began as an empty directory; voice capture, per-person/per-channel voice files, persistent memory, and the Content Library were added when friction became real rather than designed up front.^\[12\]^[^data:35] This is an operating discipline: every paved road needs maintenance and cleanup and adds mental and token cost to future runs, so infrastructure is earned by driving the dirt road first.^\[13\]^[^data:31]

The content-research requirement has a distinct boundary in [Content Library](./content-library/page.md): a browsable, persistent, tagged corpus that agents can search and synthesise against, rather than a report that is generated and then lost.^\[14\]^[^data:45] As of 2026-08-25, LinkedIn’s execution cycle was deliberately parked pending a platform-research round, making the library shape an architecture requirement rather than a tuning request.^\[15\]^[^data:45]

## Structured operational memory

Discovery-call intake shows how transient material becomes durable, queryable records. After a call, the transcript is dropped into chat; the agent extracts six fixed fields, creates or finds the person and organisation, records the interaction in [Network OS](../network-os/page.md), and creates a follow-up task when needed. Competitive or partnership intelligence that outlives a contact is separated from the relationship record and filed independently.^\[16\]^[^data:60]

## Human control

A working internal framing calls the human responsibility the “judgment layer”: define the system’s layered scope and retain foundational decisions such as the data model and architecture before delegating downstream work. The handle is explicitly not committed, so Company Brain records this as an evolving design principle rather than a settled doctrine.^\[17\]^[^data:31] For the broader doctrine, see [Human Judgment & Delegation](../../ai-practice/human-judgment-delegation/page.md); here the operational consequence is narrower: the AI sorts against layers while foundational decisions remain with the human before downstream delegation.^\[18\]^[^data:31]

[^data:31]: [domains/content/journey/concepts/_spine.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/content/journey/concepts/_spine.md)
[^data:241]: [wiki/pages/syntheses/icm-interpretable-context-methodology.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/wiki/pages/syntheses/icm-interpretable-context-methodology.md)
[^data:270]: [wiki/pages/syntheses/persistent-strategist-control-plane.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/wiki/pages/syntheses/persistent-strategist-control-plane.md)
[^data:35]: [domains/content/journey/log.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/content/journey/log.md)
[^data:45]: [domains/content/linkedin/strategy.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/content/linkedin/strategy.md)
[^data:60]: [domains/product/discovery-call-workflow.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/product/discovery-call-workflow.md)
