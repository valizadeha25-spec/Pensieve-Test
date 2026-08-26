# Content Library

Content Library is the persistent home for outside social inspiration that can be analyzed, indexed, tagged, and retrieved for later content ideation.^\[1\]^ (`data:31`) It is intended to be a browsable, persistent, tagged corpus that agents can search and synthesise against, rather than a report generated and then lost.^\[2\]^ (`data:45`)

## Lifecycle

1. **Capture.** An iOS shortcut sends an Instagram URL to a Supabase queue with one tap.^\[3\]^ (`data:35`)
2. **Analyze and ingest.** A Codex routine wakes every 6 hours, downloads the media, reads it frame by frame, transcribes the audio, analyzes it deeply, ingests it to the wiki, indexes and tags it for search, and files it in the library.^\[4\]^ (`data:35`)
3. **Retrieve and ideate.** Amir opens the library, picks items onto a board, and brainstorms against a format already proven on social.^\[5\]^ (`data:35`)

## Indexing and retrieval

The content taxonomy distinguishes three layers: the platform vessel, the content style or format, and the internal structure used to pace retention.^\[6\]^ (`data:77`) A single piece can combine all three—for example, a reel shot as greenscreen using an expert-debunk structure.^\[7\]^ (`data:77`)

The format taxonomy offers a reference catalog of about 28 named styles, but it is an open-ended starting vocabulary: new formats should be added as they are observed rather than spun into new pages.^\[8\]^ (`data:77`) It also proposes five format-selection metadata axes—effort, frequency, speed of result, planning, and niche fit—rather than treating those properties as formats themselves.^\[9\]^ (`data:77`) The mapping of those terms to the internal vocabulary and whether the tradeoff axes should become structured metadata in a real library store remain open questions.^\[10\]^ (`data:77`)

The Instagram craft references map hooks, story-flow structures, retention mechanics, and visuals to `hook_structure`, `storyline`, `retention_devices`, and `visual_type`. Ingested reels are tagged on those axes, and `board-ideation` surfaces the resulting moves as a parts-bin ranked by proven reach.^\[11\]^ (`data:27`)

## Operating principle

The system began as an empty directory; each step was added on demand as friction appeared rather than designed up front.^\[12\]^ (`data:31`) The resulting infrastructure evolved and adapted to Amir’s workflow, holding in the environment thinking that otherwise had to be repeated.^\[13\]^ (`data:35`) The operating discipline is to build each road only after feeling the friction by hand, because growth is not free: every system needs maintenance, cleanup, and mental and token cost.^\[14\]^ (`data:35`)

## Relationship to channel research

The Content Library requirement arose in LinkedIn research because `linkedin-scout` was assessed as “really badly configured, not that much helpful”; the requested replacement was the persistent corpus described above, not a disposable report.^\[15\]^ (`data:45`) As of 2026-08-25, the LinkedIn execution cycle is deliberately parked pending a separate research round.^\[16\]^ (`data:45`)

For deeper reading, see [Product](../../../product/page.md) for the user-facing product surface and workflows, [Content & Brand](../../../content-brand/page.md) for editorial identity and publishing operations, [AI Practice](../../../ai-practice/page.md) for principles governing AI-enabled work, [Systems](../../page.md) for work-context storage, AI routing, integrations, and service dependencies, and [Privacy & Data Protection](../../../privacy-data-protection/page.md) for personal-data governance.

## Sources
- [domains/content/journey/concepts/_spine.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/content/journey/concepts/_spine.md) (`data:31`)
- [domains/content/linkedin/strategy.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/content/linkedin/strategy.md) (`data:45`)
- [domains/content/journey/log.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/content/journey/log.md) (`data:35`)
- [wiki/pages/formats/content-format-taxonomy.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/wiki/pages/formats/content-format-taxonomy.md) (`data:77`)
- [domains/content/instagram/playbook/README.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/content/instagram/playbook/README.md) (`data:27`)
