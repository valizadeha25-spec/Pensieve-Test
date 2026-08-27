# Systems

PamAI’s systems estate joins persistent work context, an AI request path, user-selected integrations, and supporting operational services.^\[1\]^ (`data:9`) The two detailed systems below separate the context substrate from network operations. [Company Brain](./company-brain/page.md) is presented as the built proof of Pam’s durable-context approach.^\[2\]^ (`data:36`) [Network OS](./network-os/page.md) is the operational network system surfaced through the Company Brain dashboard and agent tools.^\[3\]^ (`data:50`)

## Context substrate and synchronization

The product direction confirmed 24 August 2026 positions PAM Desktop as a primary foundation for the future PAM product rather than merely a local Web version or a cheaper chat client.^\[4\]^ (`data:62`) It describes the longer-term system as an opinionated, managed context environment for a person, team, and company, built from files and folders, structured project data, sources, and connections that a native AI agent can understand and use.^\[5\]^ (`data:62`) Synchronization is a first-class part of that direction: PAM is building native synchronization of context files across Desktop, Web/cloud, and machines, eventually extending to team members.^\[6\]^ (`data:62`)

The Golden Context working concept describes the compounding mechanism as context that persists and layers rather than evaporates. It presents Company Brain as the built proof: every prompt is a deposit opportunity, durable material is captured at the right layer, and the per-task ask stays disposable.^\[7\]^ (`data:36`)

An internal ontology brainstorm proposes a candidate reality layer beneath PAM’s existing project-structure layer, with Person, Commitment, Event, Decision, Dependency, Claim, Outcome, and Constraint as candidate ontology elements.^\[8\]^ (`data:183`) The brainstorm is explicitly a working exploration rather than standing doctrine: nothing in it is decided, and it asks Amir to establish authoritative technical, architectural, and data-model documentation.^\[9\]^ (`data:183`)

## AI request path

PamAI sends user content to AI models through the Vercel AI Gateway. By default, requests use Zero Data Retention: providers do not retain prompts or outputs after service or use them to train their models.^\[10\]^ (`data:9`) Provider pinning limits inference to vetted US/EU or Western/GDPR-aligned hosts; requests fail outside the allowlist, and PamAI does not route user data to first-party China AI endpoints.^\[11\]^ (`data:9`) Interactive conversation training is an explicit profile opt-in and is off by default; background and system jobs remain Zero Data Retention even if a user opts in.^\[12\]^ (`data:9`)

## Integrations and supporting services

PamAI stores and retrieves workspaces, projects, messages, files, and memory, and runs user-requested integrations and imports.^\[13\]^ (`data:9`) The documented integration surface includes Telegram, WhatsApp, Google Calendar, Notion, ClickUp, and coding-agent client data; supporting subprocessors cover hosting, storage, authentication, AI inference, messaging, email, sandbox compute, error monitoring, and payment services.^\[14\]^ (`data:9`)

Google Calendar illustrates the connector boundary: PamAI accesses only the Google data needed for requested features, encrypts Google OAuth access and refresh tokens at rest, transmits Google data over HTTPS/TLS, and limits access to authorized systems and personnel. Disconnecting the account stops new Calendar sync and deletes or deactivates stored OAuth tokens.^\[15\]^ (`data:9`)

## Operational records and controls

Network OS lives in Supabase and is surfaced through the existing Company Brain dashboard and agent tools. Its database is the canonical operational record for network data; a person’s profile or timeline is not mirrored into Markdown.^\[16\]^ (`data:50`)

As of the 18 July 2026 cost and actor-contract audit, network discovery had spent $1.246 while the Company Brain ledger reported $0.16, and two apparent Code Crafter zero-result failures were actually returned results misparsed with Harvest’s camelCase contract instead of Code Crafter’s snake_case contract.^\[17\]^ (`data:52`) As of that audit, paid discovery and connection sending were paused pending typed actor adapters, atomic budget reservation, settled provider cost, one problem-context hypothesis, and the specified scorecard.^\[18\]^ (`data:52`)

For the user-facing workflows and capabilities, see [Product](../product/page.md). For personal-data governance and provider boundaries, see [Privacy & Data Protection](../privacy-data-protection/page.md).

## Sources
- [https://pamai.pm/privacy](https://pamai.pm/privacy) (`data:9`)
- [domains/content/journey/concepts/golden-context.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/content/journey/concepts/golden-context.md) (`data:36`)
- [domains/network/README.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/network/README.md) (`data:50`)
- [domains/product/philosophy/architecture.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/product/philosophy/architecture.md) (`data:62`)
- [domains/product/ontology-brainstorm/README.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/product/ontology-brainstorm/README.md) (`data:183`)
- [domains/network/learnings/discovery.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/network/learnings/discovery.md) (`data:52`)
