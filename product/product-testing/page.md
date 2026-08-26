# Product Testing

Product testing is PamAI's durable process for running a friend/beta testing cohort.^\[1\]^ (`data:74`) `testing-playbook.md` is the Phase 1 testing process, covering call scripts, journey stages, and question-game design.^\[2\]^ (`data:56`) It is marked as distinct from live Network OS records.^\[3\]^ (`data:56`) Discovery/outreach calls are documented as an earlier stage than `testing-playbook.md`; this page therefore starts with cohort testing rather than the earlier discovery stage. See [Customer Discovery](../../go-to-market/customer-discovery/page.md).^\[4\]^ (`data:56`)

## Round goals

Every round must answer two questions: does the morning brief trigger genuine return without a reminder, and does the user trust Pam enough to act on its suggestions by Day 3?^\[5\]^ (`data:74`)

A build-in-public draft records Pam in a limited private MVP test rather than a public launch, with Amir also using it himself.^\[6\]^ (`data:37`) The test is aimed at whether Pam takes the management weight off a user's day rather than at feature or UI coverage.^\[7\]^ (`data:37`) It watches daily-brief quality, whether generated plans are useful and grounded, cognitive load, and cost.^\[8\]^ (`data:37`)

## Testing journey

The documented sequence is pre-call preparation, a live intro, self-guided onboarding, and three follow-up touchpoints.^\[9\]^ (`data:74`)

1. **Pre-call preparation** — before reaching out.
2. **Intro call** — about 20 minutes, scripted minute by minute, including a live demonstration of Pam.
3. **Self-guided onboarding** — the tester goes through Foundation and Planning alone.
4. **Day 1 touchpoint** — a 5–7-minute corrective check on whether onboarding felt like theirs.
5. **Day 3 touchpoint** — a 15-minute key call asking whether the morning brief pulled the tester back on its own and whether they acted on a suggestion.
6. **Day 7–10 or Day 16 touchpoint** — a 20-minute open-ended follow-up on whether the tester would open Pam every morning without a reminder.

Each touchpoint has a scripted opener, a data-capture template, and green, amber, and red signal definitions. A pre-priming question is sent before the intro call about the tester's biggest day-to-day frustration managing work, projects, ideas, or responsibilities.^\[10\]^ (`data:74`)

## Assessment and diagnosis

The framework assesses eight areas—Problem Validation, First Moment of Truth, Onboarding UX, Activation Funnel, Trigger Effectiveness, Behavioural Adoption, Workflow Integration, and Messaging Clarity—using a testing method, signal, and success or failure criteria for each.^\[11\]^ (`data:74`)

A signal map turns result patterns into diagnosis: when Q1 return is NO across the majority of testers, the playbook treats it as a brief-redesign problem rather than a scale problem.^\[12\]^ (`data:74`) A 5–10-person round cannot establish scalability, long-term value, cold-user activation, or statistical significance; it produces directional signal only.^\[13\]^ (`data:74`)

## Evidence capture and boundaries

Each tester is one canonical `network_people` row, belongs to a testing program through `network_program_memberships`, and each touchpoint becomes a `pam_test` activity with sourced facts, observations, and follow-up tasks.^\[14\]^ (`data:74`) The resulting operational records feed [Network OS](../../systems/network-os/page.md); this page retains the repeatable method rather than individual tester histories.

The playbook describes the durable process those records follow, rather than a result ledger.^\[15\]^ (`data:74`) In the source material, the tracking spreadsheets were mostly empty and only a single real logged session existed. The instruction is to treat Network OS as the fresh, live version of that tracking rather than backfill the old spreadsheets.^\[16\]^ (`data:74`)

The interactive "drift game" is a separate onboarding design layer, not the testing process itself. It uses five staged scenarios with deliberately plausible multiple-choice options and is the artifact test subjects go through during Stage 3.^\[17\]^ (`data:74`) For the user-facing ritual layer, see [Product Rituals](../product-rituals/page.md). For the adjacent prospect and problem-understanding work, see [Customer Discovery](../../go-to-market/customer-discovery/page.md).

## Sources
- [domains/product/testing-playbook.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/product/testing-playbook.md) (`data:74`)
- [domains/product/README.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/product/README.md) (`data:56`)
- [domains/content/journey/founding-story.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/content/journey/founding-story.md) (`data:37`)
