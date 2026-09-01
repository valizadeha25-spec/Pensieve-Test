# Channels

PamAI’s content operation is organized channel-first: each platform is a self-contained world with its own accounts, playbook, and working space.^\[1\]^[^data:22] The platform-priority decision recorded on 2026-08-21[^decision:209] makes Instagram primary and LinkedIn second; Twitter/X and YouTube Shorts are parked.^\[2\]^[^data:46]

## Portfolio

[Instagram](./instagram/page.md) is the primary audience-building channel.^\[3\]^[^data:46] Its opening vessel scope is Reels only; Stories and carousels are deliberately out until Reels have been consistent for a few weeks.^\[4\]^[^data:23] Account-specific operating models sit in [Pam Account](./instagram/pam-account/page.md), [Amir's Account](./instagram/amir-s-account/page.md), and [Emma Narrative Account](./instagram/emma-narrative-account/page.md), with reusable short-form doctrine in [Production Craft](./instagram/production-craft/page.md).

[LinkedIn](./linkedin/page.md) is second to Instagram, with a 2-per-week floor and 4-per-week target.^\[5\]^[^data:45] Its intended approach is separate from Instagram rather than repurposed, with one weekly lead magnet shared with Instagram and a separate streak.^\[6\]^[^data:45] The execution cycle is deliberately parked as of 2026-08-25 pending a LinkedIn research round; post days and the writing schedule remain unset.^\[7\]^[^data:45]

[Twitter](./twitter/page.md) is parked as of 2026-08-25 and is not in the current plan.^\[8\]^[^data:48] Its documented presence is a single personal track for Amir, while Pam’s company account has not launched.^\[9\]^[^data:48] The retained Amir playbook’s cadence is suspended and is not a current commitment.^\[10\]^[^data:47]

## Shared publishing model

The content pipeline defines a post as one row in the Supabase `posts` table, with `posts.content` and `posts.content_brief` kept current as the source of truth.^\[11\]^[^data:22] Ideas come from sessions, the `journey/` material well, or the wiki; promoted posts carry an `idea_ref` back to their wiki page.^\[12\]^[^data:22] Empty playbook documents are not created speculatively; a channel grows a `hooks.md` when there is real hook craft to record.^\[13\]^[^data:22]

Craft doctrine also crosses channel boundaries: the Instagram playbook’s story-flow work has every piece — video and written alike — draw its emotional arc (tension rising, releasing, and building to an earned payoff) before a storyline is chosen or a single line drafted, and it states that this applies to all content, including LinkedIn, Twitter, and Instagram captions.^\[14\]^[^data:257]

Niyayesh’s role covers content creation and execution across LinkedIn, Instagram, Twitter, and YouTube Shorts.^\[15\]^[^data:19] Use the linked channel pages for each platform’s recurring publishing model and craft; this page keeps the cross-channel status, coordination points, shared pipeline, and craft principles visible in one place.

[^data:22]: [domains/content/README.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/content/README.md)
[^decision:209]: [decision recorded on 2026-08-21](https://app.pensieve.uk/dashboard/contexts/506/context/decisions/209)
[^data:46]: [domains/content/strategy.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/content/strategy.md)
[^data:23]: [domains/content/instagram/README.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/content/instagram/README.md)
[^data:45]: [domains/content/linkedin/strategy.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/content/linkedin/strategy.md)
[^data:48]: [domains/content/twitter/README.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/content/twitter/README.md)
[^data:47]: [domains/content/twitter/amir.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/content/twitter/amir.md)
[^data:257]: [domains/content/instagram/playbook/story-flow.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/content/instagram/playbook/story-flow.md)
[^data:19]: [core/niyayesh.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/core/niyayesh.md)
