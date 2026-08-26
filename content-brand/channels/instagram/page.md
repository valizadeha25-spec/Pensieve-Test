# Instagram

Instagram is PamAI’s primary content channel. The 2026-08-21 channel decision sets the opening vessel scope to Reels only; Stories and carousels are deliberately out until Reels have been consistent for a few weeks.^\[1\]^ (`data:23`)

Account-level operating detail is maintained in [Pam Account](./pam-account/page.md), [Amir's Account](./amir-s-account/page.md), and [Emma Narrative Account](./emma-narrative-account/page.md). Shared Instagram-specific production doctrine is maintained in [Production Craft](./production-craft/page.md).

The Pam account strategy is explicitly the May 2026 Instagram Content Strategy, filed 2026-06-13.^\[2\]^ (`data:26`) It lists Carousels as secondary for ideas needing more than one frame^\[3\]^ (`data:26`) and Stories as always-on informal content.^\[4\]^ (`data:26`) Those entries are historical account guidance; the later channel decision records Reels-only as the opening scope.^\[5\]^ (`data:23`)

## Account portfolio

[Pam Account](./pam-account/page.md) is Pam’s brand account for reach and recognition. It participates in platform culture through trends, humour, visual storytelling, and relatable moments rather than performing.^\[6\]^ (`data:26`) Trend pieces remix trending audio, formats, or meme structures around founder experience, work chaos, and the gap between plans and reality.^\[7\]^ (`data:26`) Founder-reality pieces capture what it actually feels like to build from a brand perspective, while product teases show a decision, workflow, or problem in context rather than making an advertisement.^\[8\]^ (`data:26`)^\[9\]^ (`data:26`) Its voice is dry, funny, and self-aware: relatable first, brand second.^\[10\]^ (`data:26`)^\[11\]^ (`data:26`)

[Amir's Account](./amir-s-account/page.md) is the personal lane for personal brand, thought leadership, and raw, in-the-moment build-in-public documentation; it is Amir talking rather than a brand account.^\[12\]^ (`data:25`) It speaks to ambitious people without a traditional computer-science background who want to build with AI and to business owners, freelancers, managers, and employees who want practical AI productivity; it is explicitly not positioned for engineers.^\[13\]^ (`data:25`)^\[14\]^ (`data:25`)^\[15\]^ (`data:25`) Its editorial focus spans building in public, AI-engineering education, honest signal on AI, and personal story.^\[16\]^ (`data:25`) The guardrail is receipts: show the specific thing, what it actually took, and what did not work, rather than making a generic promise about AI.^\[17\]^ (`data:25`)

[Emma Narrative Account](./emma-narrative-account/page.md) is a separate, unbranded account that is not publicly connected to Pam, Negin, or PamAI, and is not a marketing vehicle for Pam.^\[18\]^ (`data:24`) Its format is three approximately one-minute episodes per week, each tied to one real week, one real task, and one real result, paced as hook, attempt, and reveal.^\[19\]^ (`data:24`) Negin supplies what actually happened; Claude plots and checks the episode but does not invent plot events.^\[20\]^ (`data:24`)

The lanes have different documented rhythms: Amir’s plan calls for five Reels per week on Monday, Tuesday, Thursday, Friday, and Sunday; Emma’s series calls for three approximately one-minute episodes per week; and Pam coordinates with Amir on the same shoot days while producing different content.^\[21\]^ (`data:46`)^\[22\]^ (`data:24`)^\[23\]^ (`data:26`) Pam and Amir post freely and frequently, complementing one another without coordinating post-by-post.^\[24\]^ (`data:23`)

## Editorial and production system

Each piece has three separate axes: vessel, the platform container; format, the content style; and structure, the internal retention pacing.^\[25\]^ (`data:23`) Planning is format first and topic second; starting with the topic causes shoot-day paralysis.^\[26\]^ (`data:23`) Every idea is fully specified before shooting, with six fields: format, main insight, hook, storyline, retention, and visual plan.^\[27\]^ (`data:23`)

The default route from inspiration to a fully specified idea is `board-ideation`.^\[28\]^ (`data:23`) Saved reels are shelved on a [Content Library](../../../systems/company-brain/content-library/page.md) board with a line of intent; Claude decomposes them into measured craft moves, grounds them against journey and positioning, recombines them into content briefs, and graduates keepers into the pipeline with provenance.^\[29\]^ (`data:23`) Manual per-video prep is the fallback when there is no board.^\[30\]^ (`data:23`)

Build-in-public source material stays in `journey/` as cross-channel material, while Instagram is where the pieces get made.^\[31\]^ (`data:23`) The publishing model treats a post as one row in the Supabase `posts` table, with `posts.content` and `posts.content_brief` kept current as the source of truth.^\[32\]^ (`data:22`)^\[33\]^ (`data:22`) Instagram video production lives locally under `pam-video/` and binds back to the row through `project.md`.^\[34\]^ (`data:22`)

## Ownership and quality bar

Niyayesh synthesizes the weekly content-idea list from research, journey, and brainstorming, selects formats, plans visuals, schedules each piece, and posts to the PAM professional Instagram account.^\[35\]^ (`data:19`) Amir supplies the journey and build-in-public raw material—the what, why, and lesson—writes the one-sentence main insight for each chosen idea, and leads the storyline pass.^\[36\]^ (`data:15`) He posts to his personal account while Niyayesh posts to the PAM professional account.^\[37\]^ (`data:15`)

The shared [Production Craft](./production-craft/page.md) layer is a durable, human-readable reference for why short-form moves work, not a workflow to walk manually.^\[38\]^ (`data:27`) Before the camera rolls, the prep card must lock the visual type, exactly what appears and when, the physical setup required, and whether the visual eliminates the need for cuts; if any item is undecided, the prep card is incomplete.^\[39\]^ (`data:28`) Its governing question is what the viewer needs to see to believe the claim, and overlay text is never proof by itself.^\[40\]^ (`data:28`)^\[41\]^ (`data:28`)

Review separates attention winners, trust winners, conversion winners, and format failures, changing one major variable at a time.^\[42\]^ (`data:94`) AI handles aggregation and pattern detection while humans retain approval for consequential actions.^\[43\]^ (`data:102`)

## Sources
- [domains/content/instagram/README.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/content/instagram/README.md) (`data:23`)
- [domains/content/instagram/pam.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/content/instagram/pam.md) (`data:26`)
- [domains/content/instagram/amir.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/content/instagram/amir.md) (`data:25`)
- [domains/content/instagram/emma.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/content/instagram/emma.md) (`data:24`)
- [domains/content/strategy.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/content/strategy.md) (`data:46`)
- [domains/content/README.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/content/README.md) (`data:22`)
- [core/niyayesh.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/core/niyayesh.md) (`data:19`)
- [core/amir.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/core/amir.md) (`data:15`)
- [domains/content/instagram/playbook/README.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/content/instagram/playbook/README.md) (`data:27`)
- [domains/content/instagram/playbook/visuals.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/content/instagram/playbook/visuals.md) (`data:28`)
- [wiki/pages/syntheses/instagram-content-operating-system.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/wiki/pages/syntheses/instagram-content-operating-system.md) (`data:94`)
- [wiki/pages/themes/ai-marketing-workflows.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/wiki/pages/themes/ai-marketing-workflows.md) (`data:102`)
