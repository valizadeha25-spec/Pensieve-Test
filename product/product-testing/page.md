# Product Testing

Product testing is PamAI's durable process for running a friend/beta testing cohort. The operational Phase 1 process — call scripts, journey stages, and question-game design — is Negin's testing-playbook.md, compiled from her personal Phase 1 files and dated May–June 2026; it is distinct from the live Network OS records it feeds.^\[1\]^[^data:74]

## Round goals

Every round must answer two questions: does the morning brief trigger genuine return without a reminder, and does the user trust Pam enough to act on its suggestions by Day 3?^\[2\]^[^data:74]

As of 26 June 2026, Pam was in a limited private MVP test rather than a public launch, and Amir was using it himself.^\[3\]^[^data:37] The test is aimed at whether Pam takes the management weight off a user's day rather than at feature or UI coverage.^\[4\]^[^data:37] What is watched closely: daily-brief quality, whether generated plans are actually useful and grounded, whether people feel less cognitive load or more, and cost.^\[5\]^[^data:37]

## Testing journey

The documented sequence is pre-call preparation, a live intro, self-guided onboarding, and three follow-up touchpoints.^\[6\]^[^data:74]

1. **Pre-call preparation** — before reaching out.
2. **Intro call** — about 20 minutes, scripted minute by minute, including a live demonstration of Pam.
3. **Self-guided onboarding** — the tester goes through Foundation and Planning alone.
4. **Day 1 touchpoint** — a 5–7-minute corrective check on whether onboarding felt like theirs.
5. **Day 3 touchpoint** — the playbook's most important call, at 15 minutes: did the morning brief pull the tester back on its own, and did they act on a suggestion.
6. **Day 7–10 or Day 16 touchpoint** — a 20-minute open-ended follow-up on whether the tester would open Pam every morning without being reminded.

Each touchpoint has a scripted opener, a data-capture template, and green, amber, and red signal definitions. A pre-priming question is sent before the intro call: the tester's biggest day-to-day frustration in managing work, projects, ideas, or responsibilities.^\[7\]^[^data:74]

## Assessment and diagnosis

The framework assesses eight areas—Problem Validation, First Moment of Truth, Onboarding UX, Activation Funnel, Trigger Effectiveness, Behavioural Adoption, Workflow Integration, and Messaging Clarity—each with a testing method, a signal, and success or failure criteria.^\[8\]^[^data:74]

A signal map turns result patterns into diagnosis: when Q1 return is NO across the majority of testers, the playbook treats it as a brief-redesign problem rather than a scale problem.^\[9\]^[^data:74] A 5–10-person round cannot establish scalability, long-term value, cold-user activation, or statistical significance; it produces directional signal only.^\[10\]^[^data:74]

## Design Intent Audit — the first instrumented round

The Design Intent Audit is a one-off comparison exercise, not standing doctrine, kept separate from the philosophy layer for that reason.^\[11\]^[^data:179] Its process: Negin records a full onboarding-to-end-point walkthrough of Pam using a new account; the recording is written up literally into `observed-flow.md`; and only once that is complete and confirmed does an external designer's written feedback enter the picture, assessed against Negin's original product intention and what the observed flow shows actually landed for a new user, producing `gap-assessment.md`.^\[12\]^[^data:179] Negin confirmed on 2026-08-27 that the audit lives under `domains/product/` rather than `domains/product/philosophy/`.Design Intent Audit placement[^decision:276]

All three artifacts were populated on 27 August 2026:^\[13\]^[^data:179]

- **`observed-flow.md`** — a literal write-up of Negin's walkthrough of pamai.pm as a brand-new user, produced by ffmpeg extracting one frame every 2 seconds (1,938 frames total) tiled into 20 contact-sheet grids for fast scanning.^\[14\]^[^data:273] It is near-exhaustive coverage, a dramatic step up from the earlier manual QuickTime pass, which had three real gaps and missed several entire sections outright.^\[15\]^[^data:273]
- **`designer-feedback.md`** — received 2026-08-27 from Mehdi, a product designer, filed verbatim. His independent test run used his own test project, "Glamy," and went further than Negin's walkthrough into WhatsApp two-way messaging, roadmap "Ask Pam" icons, Thinking modes, interruption/queueing behavior, and cross-channel continuity.^\[16\]^[^data:181] The file's attribution note requires crediting Mehdi by name wherever its content is referenced or summarised.^\[17\]^[^data:181]
- **`gap-assessment.md`** — the verdict document comparing the design-intent philosophy documents, the observed flow, and Mehdi's feedback.^\[18\]^[^data:275]

The two runs produced these live signals. Negin's run hit a genuine product error mid-onboarding: a red "Pam is not available right now. Please try again later." banner that persisted across sampled frames from ~00:36:37 through at least ~00:39:19 — roughly 2+ real minutes — while the question card reset back to QUESTION 1 OF 3. The doc records it as a genuine outage the new user hit, not something staged.^\[19\]^[^data:273] Mehdi's Glamy run came back positive overall — he found the onboarding polished and the questions Pam asked generally very good — but named knowing what to do next, and when to use the chat and what to use it for, as the most confusing part of the product.^\[20\]^[^data:181]

The gap assessment converts these into verdicts:^\[21\]^[^data:275]

- **Confirmed (intent landed):** the three-things-a-day promise, memory that survives the chat, tone matching the identity spec, and onboarding that teaches the problem experientially.^\[22\]^[^data:275]
- **Real gaps:** the product's real sophistication is invisible unless you already know to look for it; there is no signal for which conversational mode you are in; and repeated "one last thing" phrasing eroded trust in exactly the mechanism that is supposed to build it.^\[23\]^[^data:275]
- **Overreach to push back on:** Mehdi's "silent listener" proposal — Pam passively collecting context from other tools — contradicts the stated one-time migration model for imported project, document and chat history. That boundary does not apply to observed ongoing operational connectors such as Google Calendar, Telegram or WhatsApp; the legitimate narrower gap is that Google Docs is on the intended migration list but was not available in the observed flow or Mehdi's + menu.^\[24\]^[^data:275]
- **Untested:** WhatsApp connection screen not auto-updating on success; interruption/message-queueing breaking the flow; the "Ask Pam" icon on individual roadmap items; Thinking modes (Auto/Light/Balanced/Deep); and the + menu's exact contents.^\[25\]^[^data:275]

Its one throughline is that the product is more sophisticated underneath than it is legible on the surface — where that gap shows up, users fill it with their own guess about how it should work.^\[26\]^[^data:275] The suggested next actions are product decisions and deliberate tests, not standing doctrine: decide whether quick capture versus deep interview needs an explicit signal or better inference; test the two cheap unverified items directly rather than relying on secondhand reports; give Mehdi a real answer on the silent-listener idea; and, if Thinking modes exist as described, treat them as the same bug as the mode-ambiguity gap.^\[27\]^[^data:275]

## Evidence capture and boundaries

Each tester is one canonical `network_people` row, belongs to a testing program through `network_program_memberships`, and each touchpoint becomes a `pam_test` activity with sourced facts, observations, and follow-up tasks.^\[28\]^[^data:74] The resulting operational records feed [Network OS](../../systems/network-os/page.md); this page retains the repeatable method rather than individual tester histories.

The playbook describes the durable process those records follow, rather than a result ledger.^\[29\]^[^data:74] In the source material the tracking spreadsheets (`PAM_Phase1_User_Tracking`, the onboarding evaluation scorecard) were mostly empty — only a single real logged session existed — and the instruction is to treat the Network OS as the fresh, live version of that tracking rather than backfill the old spreadsheets.^\[30\]^[^data:74]

The interactive "drift game" is a separate onboarding design layer, not the testing process itself. It uses five staged scenarios (Monday Morning, Fragmented Project, Messy Updates, Midweek Change, Decisions), each a multiple-choice moment where every option is deliberately plausible, so the user feels drift rather than being told about it; it is the artifact test subjects go through in Stage 3.^\[31\]^[^data:74]

Separately from tester cohorts, Negin logs her own hands-on interface findings — what feels off, broken, or clunky — in a structured UI/UX issues log under `domains/product/ui-ux-library/`, with a standard entry format that can link to gap-assessment findings; it is a template with no entries yet.^\[32\]^[^data:269]

For the user-facing setup-and-planning framing and journey into the daily rhythm, see [Product Rituals](../product-rituals/page.md). For the adjacent prospect and problem-understanding work, see [Customer Discovery](../../go-to-market/customer-discovery/page.md).

[^data:74]: [domains/product/testing-playbook.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/product/testing-playbook.md)
[^data:37]: [domains/content/journey/founding-story.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/content/journey/founding-story.md)
[^data:179]: [domains/product/design-intent-audit/README.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/product/design-intent-audit/README.md)
[^decision:276]: [Design Intent Audit placement](https://app.pensieve.uk/dashboard/contexts/506/context/decisions/276)
[^data:273]: [domains/product/design-intent-audit/observed-flow.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/product/design-intent-audit/observed-flow.md)
[^data:181]: [domains/product/design-intent-audit/designer-feedback.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/product/design-intent-audit/designer-feedback.md)
[^data:275]: [domains/product/design-intent-audit/gap-assessment.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/product/design-intent-audit/gap-assessment.md)
[^data:269]: [domains/product/ui-ux-library/issues.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/product/ui-ux-library/issues.md)
