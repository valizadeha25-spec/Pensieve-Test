# LinkedIn

Pam's LinkedIn presence is a shared working space with distinct account lanes for the company and personal accounts.^\[1\]^ (`data:39`)

The execution cycle is deliberately parked as of 2026-08-25.^\[2\]^ (`data:45`) June's platform write-up explicitly labels its later observations "historical sample observations, not current algorithm rules."^\[3\]^ (`data:138`)

## Account roles and voices

The Pam company account uses a calm, direct, editorial brand voice.^\[4\]^ (`data:39`)

Amir is the primary LinkedIn content voice. LinkedIn is for community and brand—not leads, investors, or launch announcements—and for building an audience of founders and operators who feel the problem PAM solves before PAM is named.^\[5\]^ (`data:15`)

His four LinkedIn pillars are building in public, AI-engineering education, honest signal on AI, and personal story; the stated audience is not engineers.^\[6\]^ (`data:38`) His tone is direct, founder-led, technically credible, and free of corporate speak.^\[7\]^ (`data:38`) Posts should open with the hook, use short paragraphs, avoid listicles unless the structure serves the point, and end with a specific point or question rather than generic engagement bait.^\[8\]^ (`data:38`)

Niyayesh owns content creation and execution across LinkedIn, Instagram, Twitter, and YouTube Shorts.^\[9\]^ (`data:19`) The PAM LinkedIn lane is an editorial brand voice with a documented 1–3 posts/week rhythm rotating across The Problem, The POV, and The Proof.^\[10\]^ (`data:19`)

Negin's personal LinkedIn is a professional product-side presence broader than Pam: she is a product designer and lead showing how she thinks, with Pam as evidence rather than the subject.^\[11\]^ (`data:40`) Her topics are product design method and judgment, defensible contrarian product takes, positioning/category arguments, and design rationale; her voice is essayistic and argument-led rather than hook-tension-reveal or listicle.^\[12\]^ (`data:40`)

An earlier profile described Negin's voice guide as an empty shell as of 2026-07-04, pending review of published posts.^\[13\]^ (`data:16`) The later foundation was built directly with her on 2026-07-17 through a structured interview, not a review of existing posts, and says to revisit it once real posts and feedback exist.^\[14\]^ (`data:40`) The documented target was a first post live by 2026-08-04, locked on 2026-07-17.^\[15\]^ (`data:40`) Her planned drafting rule matches Amir's—she writes and the brain helps her write better—but it was not yet tested in real drafting sessions.^\[16\]^ (`data:16`)

## Drafting, storage, and approval

Each LinkedIn post is one row in the Supabase `posts` table, holding state and content.^\[17\]^ (`data:22`) The scratch file in `work/drafts/` is ephemeral and deleted on approval.^\[18\]^ (`data:39`)

Keep `posts.content` and `posts.content_brief` current as the source of truth.^\[19\]^ (`data:22`) Ideas enter from sessions, the journey material well, or the wiki; promoted posts carry `idea_ref` back to their wiki page.^\[20\]^ (`data:22`)

The author's words are the post, and drafting loads the author's voice, the channel playbook, and the wiki before writing.^\[21\]^ (`data:39`) For Amir, the rule is assistive rather than substitutive: brainstorm or research on request, shape his draft or transcript, and make minimal refinements; never write from scratch, restructure, replace his voice, or invent his facts, experiences, or opinions.^\[22\]^ (`data:15`)

## Channel decisions and open execution questions

The cross-channel plan places Instagram first and LinkedIn second, with LinkedIn's cycle not yet designed.^\[23\]^ (`data:46`) The LinkedIn decision sets a 2/week floor and 4/week target, requires separate rather than repurposed posts, shares one weekly lead magnet with Instagram, and gives LinkedIn its own streak.^\[24\]^ (`data:45`)

Post days are unset, the writing block is unresolved, and candidate material sources are the journey, the week's work, the scraped archive, and the wiki.^\[25\]^ (`data:45`) Amir's account guide records the same 2/week floor and 4/week target and leaves post days and the execution cycle parked pending a research round.^\[26\]^ (`data:38`)

One unadopted design observation separates text-only posts, which have no production dependency, from posts needing video, graphics, or screen recordings, which are production-constrained like reels.^\[27\]^ (`data:45`)

The research tool is itself an open dependency: `linkedin-scout` is assessed as badly configured, while the desired shape is a persistent, searchable, tagged Content Library for agents rather than a report that is generated and lost.^\[28\]^ (`data:45`)

Research coverage also has known failure modes. The June 16 report records zero posts from `scarletapi` across all five clusters and seven consecutive zero-yield runs, calling for a replacement actor evaluation.^\[29\]^ (`data:140`) The June 17 report records both actors timing out after about 16 minutes on the Building with AI cluster for a second consecutive zero-yield run, treating the failure as infrastructure rather than a topic signal.^\[30\]^ (`data:141`)

## Working format and playbook

Until a formal execution cycle is designed, the strongest working default for founder/operator posts is native text in the 200–500-word range, structured as Problem → Insight → Implication. Keep backstory below half of the post, use 0–1 emoji, treat external links as a mixed signal with no link as the safe default unless the post is authority-building, and treat carousels as an experiment rather than a performance default.^\[31\]^ (`data:138`)

Specificity is load-bearing: named companies, people, numbers, and decisions are preferred to abstract AI-future takes.^\[32\]^ (`data:138`) Choose the response you want to earn: direct questions or challenges are associated with comment activity, concrete technical content with reshares, and emotional or aspirational content with reactions.^\[33\]^ (`data:138`)

Later sample observations favor first-person founder voice over advisor or consultant framing at equivalent topic and length; short teaser-with-link posts were near-zero, while heavy-emoji listicles could earn reach while suppressing comments. These are directional sample observations, not universal rules.^\[34\]^ (`data:141`)

The hook guide treats the opening as a job-specific mechanism—curiosity, challenge, proof, surprise, pain diagnosis, comparison, or compressed authority—and requires the first line or frame to establish stakes without greetings, with the body clearing the expectation it creates.^\[35\]^ (`data:206`) For audiences that already recognize a live subculture, a high-energy invitation can escalate through concrete shared behaviors in questions, then release into a self-aware turn; it is not a fit when the opening needs to carry proof or nuance.^\[36\]^ (`data:206`) For visual hooks, the caption must identify a specific shared tension before a repeated acted beat or borrowed reaction can read as the payoff.^\[37\]^ (`data:206`) The June scout identified counter-intuitive reframes, problem-first open questions, first-person narratives with concrete outcomes, vulnerability or friction, and evidence-first essays as recurring patterns.^\[38\]^ (`data:139`)

For product posts with native video, text should explain why the feature matters while the video proves that it exists and behaves specifically; the demonstration should remain understandable without audio.^\[39\]^ (`data:138`)

A reusable carousel reference uses a structured-document or file-tree aesthetic, clean white space, a two-column item-name/benefit hierarchy, and strong CTA buttons.^\[40\]^ (`data:66`) Its fit for non-technical audiences and the use of `.md` filenames remain open questions.^\[41\]^ (`data:66`) The two June scout datasets found no top-performing carousels, so this visual system is a template experiment rather than a settled default.^\[42\]^ (`data:138`)

The Joerg Storm benchmark is useful as a pattern reference, not a general rule: it records the easy/hard contrast, a high-polarity closing question, and apparent external-link tolerance tied to domain authority.^\[43\]^ (`data:84`)

Dissonance is not yet an adopted LinkedIn rule. Its source explicitly leaves open whether a framework developed around video persona applies to written LinkedIn posts, while identifying the text analogue as a contradiction hook that flips a dominant assumption in one opening line.^\[44\]^ (`data:106`)

## Topic fit and evidence discipline

The repeated June practitioner question was how to take what works in a demo and make it work when real users hit it.^\[45\]^ (`data:140`) The surrounding observations name production failure modes such as memory loss, concurrent state collapse, verification gates, and context constraints.^\[46\]^ (`data:138`) The first scout also tracked MCP as an infrastructure layer, enterprise knowledge management versus RAG, and the demo-to-production gap as emerging themes.^\[47\]^ (`data:139`)

AI-agent governance is a research lead rather than an adopted claim: one batch's governance post earned 1,475 reactions and 800 comments, but the same synthesis says Amir-specific credibility is not documented and a practitioner post would need a concrete deployment incident rather than borrowed enterprise framing.^\[48\]^ (`data:101`) Engagement filters must be paired with topic-relevance filters so off-topic emotional or aspirational posts do not become editorial evidence.^\[49\]^ (`data:138`)

## Sources
- [domains/content/linkedin/README.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/content/linkedin/README.md) (`data:39`)
- [domains/content/linkedin/strategy.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/content/linkedin/strategy.md) (`data:45`)
- [wiki/pages/platforms/linkedin.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/wiki/pages/platforms/linkedin.md) (`data:138`)
- [core/amir.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/core/amir.md) (`data:15`)
- [domains/content/linkedin/amir.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/content/linkedin/amir.md) (`data:38`)
- [core/niyayesh.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/core/niyayesh.md) (`data:19`)
- [domains/content/linkedin/negin.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/content/linkedin/negin.md) (`data:40`)
- [core/negin.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/core/negin.md) (`data:16`)
- [domains/content/README.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/content/README.md) (`data:22`)
- [domains/content/strategy.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/content/strategy.md) (`data:46`)
- [wiki/pages/syntheses/linkedin-scout-2026-06-16.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/wiki/pages/syntheses/linkedin-scout-2026-06-16.md) (`data:140`)
- [wiki/pages/syntheses/linkedin-scout-2026-06-17.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/wiki/pages/syntheses/linkedin-scout-2026-06-17.md) (`data:141`)
- [wiki/pages/formats/hooks.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/wiki/pages/formats/hooks.md) (`data:206`)
- [wiki/pages/syntheses/linkedin-scout-2026-06-13.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/wiki/pages/syntheses/linkedin-scout-2026-06-13.md) (`data:139`)
- [wiki/pages/formats/carousel-design.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/wiki/pages/formats/carousel-design.md) (`data:66`)
- [wiki/pages/people/joerg-storm.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/wiki/pages/people/joerg-storm.md) (`data:84`)
- [wiki/pages/themes/dissonance.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/wiki/pages/themes/dissonance.md) (`data:106`)
- [wiki/pages/syntheses/linkedin-scout-2026-06-15.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/wiki/pages/syntheses/linkedin-scout-2026-06-15.md) (`data:101`)
