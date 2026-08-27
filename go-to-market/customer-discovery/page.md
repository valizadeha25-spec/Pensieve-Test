# Customer Discovery

Customer discovery is PamAI’s repeatable practice for finding and qualifying prospective users, testers, and relevant founder contacts, then turning their conversations into evidence about the problem, current workflow, product or ICP, and next step. PamAI’s network objective is to create qualified relationships with people likely to test, teach the team about the problem, refer relevant users, or become advocates; V1 measures conversations and tests rather than impressions or raw connection count.^\[1\]^ (`data:57`)

This is a working learning layer, not settled market truth: the discovery doctrine calls its tester-recruitment ICP a working ICP, not PAM’s final market ICP.^\[2\]^ (`data:49`) Individual outreach mechanics belong in [Outbound Prospecting](../outbound-prospecting/page.md), channel-level sequencing in [Demand Validation](../demand-validation/page.md), and the post-acceptance tester journey in [Product Testing](../../product/product-testing/page.md). The Product domain likewise places testing sessions and observed feedback in the Network OS rather than in Product-domain prose.^\[3\]^ (`data:178`) Negin’s documented role includes owning outreach and approaching people to join Pam’s first testing group.^\[4\]^ (`data:16`)

## Finding the right people

Discovery starts with problem context rather than a title. The relevant person is close to decisions and execution, has a live project with multiple moving parts, lacks enough project-management support to make the problem disappear, and can use PAM repeatedly during a real project.^\[5\]^ (`data:49`) Useful signals include personally owning product, delivery, GTM, operations, or several at once; concurrent client or internal projects; active building or launching; and explicit overload, fragmentation, prioritization, follow-through, or project drift.^\[6\]^ (`data:49`)

The three active problem-context hypotheses are:

- **Founder-builder carrying the company:** an early software/product founder personally coordinating product, customer work, GTM, and operations.
- **AI-native multi-project independent:** an independent builder or small agency/product-studio owner coordinating client delivery, internal products, contractors, and AI workflows.
- **Founder-adjacent small-team operator:** an operations, product, chief-of-staff, or delivery owner inside a founder-led team translating direction into daily execution without dedicated project-management capacity.^\[7\]^ (`data:49`)

The recruitment motion described by the network strategy focuses on English-speaking people personally carrying project execution, prioritizing the UK, UAE, US, Canada, Australia, and Western Europe; it starts with organizations around 1–20 people where a potential tester is close to decisions, lacks dedicated project-management capacity, and has a live project suitable for a 7–10-day test.^\[8\]^ (`data:57`) Titles such as founder or operator are retrieval handles, not qualification.^\[9\]^ (`data:49`)

## Qualification and evidence

Qualification scores sourced discovery evidence and separates observed facts from inference.^\[10\]^ (`data:49`) The scorecard uses five dimensions:

| Dimension | Points | What must be evidenced |
|---|---:|---|
| Live problem likelihood | 0–3 | Current role compression, concurrent projects, execution language, or explicit coordination pain |
| Hands-on authority | 0–2 | Personally decides, builds, delivers, or changes the working system |
| Testing readiness | 0–2 | Active project and plausible ability to use PAM repeatedly for 7–10 days |
| Relationship fit | 0–2 | English-capable, reachable on LinkedIn, credible reason for a founder-to-founder relationship |
| Evidence quality | 0–1 | Multiple consistent fields or one direct statement; no material contradiction |

^\[11\]^ (`data:49`) Qualification requires at least 7/10 overall, at least 2/3 for live problem likelihood, at least 1/2 for hands-on authority, and no hard exclusion.^\[12\]^ (`data:49`) Hard exclusions include title-only matches with no hands-on execution, no active project or plausible 7–10-day testing context, sales-funnel profiles, and low-trust or contradictory identities.^\[13\]^ (`data:49`)

A candidate record preserves LinkedIn identity and profile image, current role/company/location/size, company details where returned, the exact search hypothesis and actor input, direct versus inferred signals, score by dimension, rejection reason, and the raw actor row. Deep profile and post research is post-acceptance; pre-connection qualification may use the rich discovery row and a visible profile-state check but may not invent pain from a title.^\[14\]^ (`data:49`)

## Structured conversation capture

A discovery call is the earlier cold or warm conversation before it is known whether someone becomes a tester, distinct from the tester journey after entry into a program.^\[15\]^ (`data:60`) After the call, Negin provides the transcript and identity, the agent extracts a fixed six-field capture, logs or finds the person and organization, records the interaction, and decides whether a follow-up task is needed.^\[16\]^ (`data:60`)

The six fields are:

1. **Who & where they’re at** — name, company, stage, team size, role.
2. **Did it click** — whether the core idea resonated, in the person’s own reaction.
3. **Current workflow** — what they use today instead of Pam.
4. **Strongest reaction or quote** — the line worth keeping verbatim.
5. **ICP or product insight** — what this call sharpens about who Pam is for or what it should do.
6. **Outcome / next step** — access granted, follow-up booked, declined, or nothing needed.^\[17\]^ (`data:60`)

The workflow replaces unused tracking spreadsheets and treats the Network OS, backed by Supabase, as the live system with no parallel spreadsheet to keep in sync.^\[18\]^ (`data:60`) People, calls, activities, facts, and follow-ups are operational records in Supabase; the database is canonical and a person’s profile or timeline should not be mirrored into Markdown.^\[19\]^ (`data:50`) The call record is for relationship learning. Competitive or partnership intelligence that outlives one contact is captured separately, relevant prospect terminology can be adopted when building for that person, and an unbuilt feature is never promised in writing.^\[20\]^ (`data:60`)

## Interpreting what people say

Questions should ask for specific past behavior—“what do you do about this today, walk me through the last time it happened”—rather than hypothetical “would you use this?” questions.^\[21\]^ (`data:59`) Resonance, current workflow, the strongest quote, product or ICP insight, and outcome are recorded separately so a conversation can teach without being mistaken for acceptance.

A 29 July 2026 discovery call shows why the distinction matters: the tester did not trust an AI tool to decide things for her through the morning brief, but independently described a screen-free future workflow; Negin read the screen-fatigue reaction as support for the underlying problem even though the specific solution did not land at her current stage.^\[22\]^ (`data:41`)

Replies and signups are curiosity signals, not evidence of willingness to pay; PamAI treats real validation as a time commitment such as a pilot or a money commitment such as a deposit, LOI, or pre-payment.^\[23\]^ (`data:59`) Customer discovery records this outcome, while [Demand Validation](../demand-validation/page.md) owns the broader sequential channel test.

## Search controls and lessons

Search is hypothesis-led: each run uses one problem-context hypothesis rather than broad titles, industries, and generic keywords; its usefulness is measured by provider and run cost, normalized and raw rows, candidates reaching each score threshold, rejection reasons, cost per qualified candidate, and the next parameter or hypothesis to change.^\[24\]^ (`data:49`) No connection stage begins until a reconciled run produces a trustworthy qualified queue.^\[25\]^ (`data:49`)

The 18 July 2026 audit found that broad retrieval did not represent an ICP: founder/owner matching returned weak problem-fit rows, and a small company plus a founder title was not qualification.^\[26\]^ (`data:52`) Two supposed zero-result Code Crafter searches had actually returned 100 and 60 rows but were parsed with Harvest’s contract; “the actor did not fail; the adapter did.”^\[27\]^ (`data:52`) The audit recorded paid discovery and connection sending as paused pending typed actor adapters, atomic budget reservation, settled provider cost, one problem-context hypothesis, and the scorecard.^\[28\]^ (`data:52`)

The durable chain is hypothesis → sourced qualification → structured conversation → product or ICP learning → explicit outcome and follow-up. Use [Network OS](../../systems/network-os/page.md) for the relationship and activity records, and [Network Strategy](../network-strategy/page.md) for the surrounding relationship doctrine and audience.

## Sources
- [domains/network/strategy.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/network/strategy.md) (`data:57`)
- [domains/network/discovery.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/network/discovery.md) (`data:49`)
- [domains/product/README.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/product/README.md) (`data:178`)
- [core/negin.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/core/negin.md) (`data:16`)
- [domains/product/discovery-call-workflow.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/product/discovery-call-workflow.md) (`data:60`)
- [domains/network/README.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/network/README.md) (`data:50`)
- [domains/product/gtm-validation-plan.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/product/gtm-validation-plan.md) (`data:59`)
- [domains/content/journey/negin-product-philosophy.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/content/journey/negin-product-philosophy.md) (`data:41`)
- [domains/network/learnings/discovery.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/network/learnings/discovery.md) (`data:52`)
