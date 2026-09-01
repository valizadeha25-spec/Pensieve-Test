# Product Rituals

PamAI's ritual layer turns stored project state and context into recurring judgment and action. It moves from establishing why and what, through choosing today's work and recording what happened, to monitoring trajectory and consciously changing strategy.^\[1\]^[^data:188]

The division of labor is that Pam carries the complexity while the user does the work. The product-values framing says, “PAM carries the complexity, the user does the doing”; the user does three tasks a day and informally updates Pam at the end of the day, while storing, documenting, planning, deciding, and reflecting sit with Pam.^\[2\]^[^data:65] The intended user-facing orientation is deliberately narrow: what to do today and where the user is in the roadmap.^\[3\]^[^data:37]

## Setup and planning

Foundation is a conversational workflow that establishes seven durable parts of a project: identity, direction, situation, constraints, decisions, priorities, and goals.^\[4\]^[^data:187]

Foundation creates strategic context for Planning rather than Fronts, Milestones, Batches, or Items. Planning translates that foundation into structured records: Fronts are durable domains or angles, Milestones are project-level binary states, Batches are definitional components of one or more milestones, and Items are the smallest structured, countable units of work.^\[5\]^[^data:187]

The first planning flow:

1. Reads the foundation and relevant notebooks or imported material.
2. Establishes real team capacity and timeline constraints.
3. Proposes Fronts and the Milestone arc.
4. Identifies the highest-risk or most central Batch in the first Milestone.
5. Creates only the Items supported by the user's information.
6. Hands the user to Home to set recurring time allocations.

Confirmed project structure is written into Postgres as the conversation progresses.^\[6\]^[^data:187]

Pam keeps work and time distinct: an Item is work, a Daily plan entry is scheduled time on a specific date that may link to an Item, and an Allocation is recurring weekly capacity for a project.^\[7\]^[^data:187]

## Daily operating rhythm

### Calendar setup

Calendar setup records recurring project capacity as Allocations and reads connected calendar events as fixed commitments. Allocations determine when a project is expected to receive time and remain separate from Items and Daily plan entries.^\[8\]^[^data:188]

### Morning Brief

Morning Brief reads:

- today's project allocations and fixed calendar commitments;
- current Items, Milestones, priorities, dates, and dependencies;
- yesterday's unfinished work;
- recent user statements;
- the latest project Health and routine state.

It chooses the most important work, writes dated Daily plan entries linked to Items, explains why those actions matter today, and gives recent explicit user intent precedence over the recurring schedule.^\[9\]^[^data:188]

### Fulfillment

Fulfillment reads the day's plan and activity, asks the user what moved, updates Item state, and captures durable lessons when the user's answer changes project understanding. Silence is not treated as proof that an Item is done or blocked.^\[10\]^[^data:188]

### Project Health

Health reads both substrates: structured project progress and dependencies from Postgres, plus foundation, lessons, contradictions, prior judgments, and recent context from files and chat. It produces a file-based Health artifact describing trajectory, dominant pattern, named risk, evidence, and next review point; it does not restructure the plan automatically.^\[11\]^[^data:188]

### Reflection

Reflection reviews accumulated contradictions, lessons, recent Health, and changes in the user's thinking. It can update the foundation only after the user explicitly decides that the strategic truth changed, and it preserves its session record and unresolved items as files.^\[12\]^[^data:188]

### Scheduled routines

Postgres stores routine definitions, schedules, model settings, tool policy, status, and run history. The detailed judgment process lives in the corresponding agent skill and its file-based state.^\[13\]^[^data:188]

## User-facing journey and current status

An unfinished business-model working draft gives a coarser four-stage journey before the daily rhythm begins:^\[14\]^[^data:63]

1. **Define** — a conversational Foundation session extracts the seven fields and builds a plan for the user and a mind for Pam.
2. **Confirm** — the user reads the plan, pushes back if it does not resonate, and Pam edits it.
3. **Reality setup** — Pam connects the calendar and allocates the project into the user's actual week.
4. **Daily rhythm** — the morning brief gives three tasks from the plan and calendar, chosen by Pam rather than the user.^\[15\]^[^data:63]

The draft treats Planning as likely folded into Define and Confirm at that level of detail.^\[16\]^[^data:63] The current implementation documentation treats Foundation and Planning as separate workflows, so the coarser journey should not replace the more precise operating model.^\[17\]^[^data:187]

The product-philosophy index records that Foundation, Planning, and operating rituals were documented from current implementation and a fresh walkthrough on 2026-08-27; no future data model has been selected.^\[18\]^[^data:189] The mechanics are now documented, but whether “Full coverage of the workflow” returns as a named product-value claim, and how collaboration or document generation fit that promise, remains a direct product-owner decision.^\[19\]^[^data:189]

The rituals currently depend on the agent joining structured project state with unstructured context at runtime. Whether those joins should remain agent-driven, become more explicitly mapped, or move into a future ontology is not decided.^\[20\]^[^data:188]

The broader user-facing product surface is covered on [Product](../page.md). Storage, retrieval, and service architecture belong with [Systems](../../systems/page.md), while testing and evidence capture are covered on [Product Testing](../product-testing/page.md).

[^data:188]: [domains/product/philosophy/product-rituals.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/product/philosophy/product-rituals.md)
[^data:65]: [domains/product/philosophy/product-values.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/product/philosophy/product-values.md)
[^data:37]: [domains/content/journey/founding-story.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/content/journey/founding-story.md)
[^data:187]: [domains/product/philosophy/foundation-and-planning.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/product/philosophy/foundation-and-planning.md)
[^data:63]: [domains/product/philosophy/business-model.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/product/philosophy/business-model.md)
[^data:189]: [domains/product/philosophy/version-history-and-open-questions.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/product/philosophy/version-history-and-open-questions.md)
