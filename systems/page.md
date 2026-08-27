# Systems

PamAI’s systems estate connects persistent work context and structured project state.^\[1\]^ (`data:186`) It also includes an AI request path, integrations, and supporting services.^\[2\]^ (`data:9`) The main system homes are [Product Architecture](./product-architecture/page.md) for the current product and data foundation, [Company Brain](./company-brain/page.md) for layered internal context, and [Network OS](./network-os/page.md) for operational relationship records.

## Architecture at a glance

PAM currently separates project information into two durable substrates: structured work and execution state in Supabase Postgres, and rich context in files in Supabase Object Storage.^\[3\]^ (`data:186`) Drizzle schema is the code-level source of truth for structured work, while Postgres stores file metadata, hashes, storage paths, ingestion records, and search/index records but the document content remains file/object data.^\[4\]^ (`data:186`)

Foundation’s concise canonical foundation is held in `project.md`.^\[5\]^ (`data:187`) Planning reads the foundation and writes Fronts, Milestones, Batches, and Items into Postgres.^\[6\]^ (`data:186`) This is current behavior, while whether the separation remains the right long-term ontology is explicitly unresolved.^\[7\]^ (`data:187`)

Web and Desktop use one project model rather than separate ones. Postgres remains authoritative for structured data on both surfaces, Object Storage remains the durable cloud source for files, and Desktop keeps an authorized local copy for native agent execution and synchronization; Desktop SQLite handles local operational state and synchronization bookkeeping rather than acting as a second structured project database.^\[8\]^ (`data:186`) Routing across the substrates is mainly enforced through agent instructions and skills, not one universal data abstraction.^\[9\]^ (`data:186`)

## Context and operational systems

The working Company Brain taxonomy has a most-fundamental, roughly always-loaded layer for `CLAUDE.md` and `RESOLVER.md`, narrower domain and capability layers, database rows for tracked and queryable state, and provisional `memory/` that can be promoted when it proves durable.^\[10\]^ (`data:31`)

[Network OS](./network-os/page.md) is PAM’s operational network system. It lives in Supabase and is surfaced through the existing Company Brain dashboard and agent tools; its database is the canonical operational record, and a person’s profile or timeline is not mirrored into Markdown.^\[11\]^ (`data:50`)

## AI path, integrations, and service dependencies

PamAI sends user content to AI models through the Vercel AI Gateway.^\[12\]^ (`data:9`) By default, AI requests use Zero Data Retention (ZDR), provider pinning restricts inference to a vetted allowlist of US/EU or Western/GDPR-aligned hosts, and interactive-conversation training is an explicit profile opt-in that is off by default.^\[13\]^ (`data:9`)

PamAI stores and retrieves workspaces, projects, messages, files, and memory and runs user-requested integrations and imports.^\[14\]^ (`data:9`) The documented integration surface includes Telegram, WhatsApp, Google Calendar, Notion, ClickUp, and coding-agent client data; listed subprocessors include hosting, storage, authentication, AI inference, messaging, email, sandbox compute, error monitoring, and payment providers.^\[15\]^ (`data:9`)

See [Product](../product/page.md) for user-facing workflows and capabilities, and [Privacy & Data Protection](../privacy-data-protection/page.md) for personal-data governance and provider-specific handling.

## Architecture status and boundaries

Current claims about PAM’s implementation must be grounded in Amir’s direct account and the current PAM codebase; current implementation, current assumptions, and possible redesigns remain visibly separate, and an ontology brainstorm does not authorize a schema, storage, or business-logic decision.^\[16\]^ (`data:184`)

The current architecture record is explicitly current-state technical grounding, not a future architecture proposal.^\[17\]^ (`data:186`) The ontology brainstorm is a working exploration rather than standing doctrine; it proposes a possible reality layer of Person, Commitment, Event, Decision, Dependency, Claim, Outcome, and Constraint beneath the existing project-structure layer, but no future ontology has been chosen.^\[18\]^ (`data:185`) No future data model has been selected.^\[19\]^ (`data:189`) Detailed storage boundaries, runtime authority, and the remaining architecture questions are maintained in [Product Architecture](./product-architecture/page.md).

## Sources
- [domains/product/philosophy/architecture.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/product/philosophy/architecture.md) (`data:186`)
- [https://pamai.pm/privacy](https://pamai.pm/privacy) (`data:9`)
- [domains/product/philosophy/foundation-and-planning.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/product/philosophy/foundation-and-planning.md) (`data:187`)
- [domains/content/journey/concepts/_spine.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/content/journey/concepts/_spine.md) (`data:31`)
- [domains/network/README.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/network/README.md) (`data:50`)
- [domains/product/README.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/product/README.md) (`data:184`)
- [domains/product/ontology-brainstorm/README.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/product/ontology-brainstorm/README.md) (`data:185`)
- [domains/product/philosophy/version-history-and-open-questions.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/product/philosophy/version-history-and-open-questions.md) (`data:189`)
