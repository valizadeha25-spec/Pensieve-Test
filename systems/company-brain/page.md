# Company Brain

Company Brain is a layered AI work environment: its context taxonomy separates foundational instructions, domain material, skills, database state, and provisional memory, while its workflows turn captured material into reusable artifacts.^\[1\]^ (`data:31`) ^\[2\]^ (`data:241`)

## Layered context architecture

The system’s central move is layered scope: the human designs the layers and the AI sorts context against them. The working taxonomy puts `CLAUDE.md` and `RESOLVER.md` in the most fundamental, ~always-loaded layer; `core/` below it; `domains/<x>/` and skills files at narrower scopes; database rows for tracked and queryable state; and `memory/` as provisional material that can be promoted when it proves durable.^\[3\]^ (`data:31`)

An ICM comparison describes Company Brain as structurally ICM-shaped. Stable reference is mapped to `wiki/pages/`, `domains/`, `memory/learnings/`, and `core/`, while per-run artifacts are mapped to `posts` rows in Supabase; the two-substrate rule treats files as stable reference and the database as per-run working state.^\[4\]^ (`data:241`) Company Brain’s `wiki_item_links` and `post_library_provenance` provide a working, if partially populated, implementation of output provenance from published posts back to library and wiki sources.^\[5\]^ (`data:241`) The same comparison identifies unfinished infrastructure: no enforced Inputs/Process/Outputs stage contracts, no incremental recompilation tracking, and no phrase-level provenance within a single post.^\[6\]^ (`data:241`)

## Earned infrastructure

The content system began as an empty directory; voice capture, per-person/per-channel voice files, persistent memory, and the Content Library were added when friction became real rather than designed up front.^\[7\]^ (`data:35`) This is an operating discipline: every paved road needs maintenance and cleanup and adds mental and token cost to future runs, so infrastructure is earned by driving the dirt road first.^\[8\]^ (`data:31`)

The content-research requirement has a distinct boundary in [Content Library](./content-library/page.md): a browsable, persistent, tagged corpus that agents can search and synthesise against, rather than a report that is generated and then lost.^\[9\]^ (`data:45`) As of 2026-08-25, LinkedIn’s execution cycle was deliberately parked pending a platform-research round, making the library shape an architecture requirement rather than a tuning request.^\[10\]^ (`data:45`)

## Structured operational memory

Discovery-call intake shows how transient material becomes durable, queryable records. After a call, the transcript is dropped into chat; the agent extracts six fixed fields, creates or finds the person and organisation, records the interaction in [Network OS](../network-os/page.md), and creates a follow-up task when needed. Competitive or partnership intelligence that outlives a contact is separated from the relationship record and filed independently.^\[11\]^ (`data:60`)

## Human control

A working internal framing calls the human responsibility the “judgment layer”: define the system’s layered scope and retain foundational decisions such as the data model and architecture before delegating downstream work. The handle is explicitly not committed, so Company Brain records this as an evolving design principle rather than a settled doctrine.^\[12\]^ (`data:31`) For the broader doctrine, see [Human Judgment & Delegation](../../ai-practice/human-judgment-delegation/page.md); here the operational consequence is narrower: the AI sorts against layers while foundational decisions remain with the human before downstream delegation.^\[13\]^ (`data:31`)

## Sources
- [domains/content/journey/concepts/_spine.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/content/journey/concepts/_spine.md) (`data:31`)
- [wiki/pages/syntheses/icm-interpretable-context-methodology.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/wiki/pages/syntheses/icm-interpretable-context-methodology.md) (`data:241`)
- [domains/content/journey/log.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/content/journey/log.md) (`data:35`)
- [domains/content/linkedin/strategy.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/content/linkedin/strategy.md) (`data:45`)
- [domains/product/discovery-call-workflow.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/product/discovery-call-workflow.md) (`data:60`)
