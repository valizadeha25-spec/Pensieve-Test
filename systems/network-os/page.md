# Network OS

Network OS is PAM's operational system for its network. It lives in Supabase and is surfaced through the existing [Company Brain](../company-brain/page.md) dashboard and agent tools.^\[1\]^[^data:50] Its canonical records cover people, organizations, profiles, contact methods, meetings, PAM tests, calls, introductions, messages, notes, other activities, facts, provenance, program memberships, and follow-ups.^\[2\]^[^data:50] The database is the canonical operational record; a person's profile or timeline is not mirrored into Markdown.^\[3\]^[^data:50]

## Boundary and ownership

Strategy, ICP reasoning, relationship doctrine, and channel policy remain in deliberately authored Network-domain material. Feature design and implementation are maintained in `docs/network-os/`, while proven repeatable workflows belong in the agent skill directories.^\[4\]^[^data:50] See [Network Strategy](../../go-to-market/network-strategy/page.md) for the reasoning layer; this page follows the live records and execution controls.

## Intake and relationship records

Negin's documented role includes owning outreach—emailing and approaching people to join Pam's first testing group—and building a professional LinkedIn presence to open a network for recruiting testers.^\[5\]^[^data:16]

The documented discovery-call intake uses a fixed six-field capture. The agent then creates or finds the person and organization, records the call with its extracted facts, and creates a follow-up task when needed.^\[6\]^[^data:60] Old tracking-spreadsheet templates were never really used; the workflow treats the Supabase `network_*` tables as the live system, with no parallel spreadsheet to keep in sync.^\[7\]^[^data:60]

The testing playbook feeds the same operational substrate: each tester is one canonical `network_people` row, belongs to a testing program through `network_program_memberships`, and each touchpoint becomes a `pam_test` activity plus sourced facts, observations, and follow-up tasks.^\[8\]^[^data:74]

## LinkedIn relationship operations

The documented LinkedIn operating policy specifies Amir's normal Chrome profile, device, and IP, a maximum of 10 ordinary no-note requests per Istanbul day, high-value profiles queued for Amir within five personalized notes per month, and no LinkedIn message sending by Codex, although inboxes and replies may be inspected.^\[9\]^[^data:55] Operations must stop and pause on CAPTCHA, verification, account warning, invitation-limit UI, unexpected login, Chrome failure, or unusual friction; acceptance rate, pending buildup, and warnings are tracked. Owner approval does not make unauthorized automation compliant, so account risk remains nonzero.^\[10\]^[^data:55]

Connection records are proof-gated: the authoritative send proof is an `Invitation sent to <name>` alert or the target profile's `Pending` action, and database activity is recorded only after one appears.^\[11\]^[^data:53] Identity safety is part of the operating boundary. A page-wide `Invite .* to connect` lookup is unsafe because profile pages include recommendation cards with unrelated Connect buttons; one documented failure sent a request to Rashid ElTinay while Gastón Zelarayan's profile was open.^\[12\]^[^data:53] Before each request, read the database counter; after each proven send, record it immediately; after the batch, perform one sent-manager reconciliation. The sent-invitations total may rise by fewer rows than the database send count when a request is accepted immediately.^\[13\]^[^data:53]

See [LinkedIn Connection Operations](./linkedin-connection-operations/page.md) for the detailed identity checks, stop conditions, proof-gated recording, human handoffs, and batch reconciliation.

[^data:50]: [domains/network/README.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/network/README.md)
[^data:16]: [core/negin.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/core/negin.md)
[^data:60]: [domains/product/discovery-call-workflow.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/product/discovery-call-workflow.md)
[^data:74]: [domains/product/testing-playbook.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/product/testing-playbook.md)
[^data:55]: [domains/network/linkedin/README.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/network/linkedin/README.md)
[^data:53]: [domains/network/learnings/browser-operations.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/network/learnings/browser-operations.md)
