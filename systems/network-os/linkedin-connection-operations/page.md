# LinkedIn Connection Operations

Pam’s LinkedIn connection operations are a controlled execution workflow for Amir’s account.^\[1\]^ (`data:55`) They run from target verification and stop-signal checks to proof-gated recording and batch reconciliation.^\[2\]^ (`data:53`) Audience selection and relationship reasoning belong in [Network Strategy](../../../go-to-market/network-strategy/page.md).

## Account boundaries and stop rules

Use Amir’s normal Chrome profile, device, and IP with visible sequential interaction.^\[3\]^ (`data:55`) The ceiling is 10 ordinary no-note requests per Istanbul day. High-value profiles are queued for Amir, within five personalized notes per month. Codex may inspect inboxes and replies but never sends a LinkedIn message.^\[4\]^ (`data:55`)

Pause on CAPTCHA, verification, account warning, invitation-limit UI, unexpected login, Chrome failure, or any other unusual friction. Track acceptance rate, pending buildup, and warnings.^\[5\]^ (`data:55`) Owner approval does not make unauthorized automation compliant; account risk remains nonzero under LinkedIn’s policy.^\[6\]^ (`data:55`)

## Targeting and request execution

1. Reuse one Chrome tab and navigate directly to stored profile URLs. Take one snapshot after navigation for locator ground truth. Use exact string locators from that snapshot, scoped to the target profile header, and confirm the locator count is exactly one before clicking.^\[7\]^ (`data:53`)
2. Prefer the target profile’s More menu. Verify that the menu item names the target and that the invitation dialog names the same target; stop when unique scoping is unavailable. Positional selection is not evidence of identity.^\[8\]^ (`data:53`) On Amir’s current Chrome surface, a physical click on a LinkedIn More-menu item may only focus it; Enter performs the selected action.^\[9\]^ (`data:53`)
3. After clicking, check only the candidate-named dialog, success alert, or Pending state. The authoritative send proof is an `Invitation sent to <name>` alert or the target profile’s `Pending` action; record the database activity only after one of these appears.^\[10\]^ (`data:53`) If the first post-click check is inconclusive, inspect the existing alert or Pending state and never click Connect again.^\[11\]^ (`data:53`)

## Recording and reconciliation

Before every request, read the database counter. After every proven send, record it immediately. Account warnings and stop signals belong in the database immediately.^\[12\]^ (`data:53`) After the batch, perform one sent-manager reconciliation rather than reopening it after every candidate.^\[13\]^ (`data:53`) The sent-invitations total may rise by fewer rows than the database send count when a request is accepted immediately.^\[14\]^ (`data:53`)

## Identity failure learning

A page-wide `Invite .* to connect` lookup is unsafe because profile pages include recommendation cards with unrelated Connect buttons.^\[15\]^ (`data:53`) One documented failure sent a request to Rashid ElTinay while Gastón Zelarayan’s profile was open.^\[16\]^ (`data:53`) Future actions therefore require profile-header scoping and candidate-name verification, with a stop when unique scoping is unavailable; positional selection is not evidence of identity.^\[17\]^ (`data:53`)

## Sources
- [domains/network/linkedin/README.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/network/linkedin/README.md) (`data:55`)
- [domains/network/learnings/browser-operations.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/domains/network/learnings/browser-operations.md) (`data:53`)
