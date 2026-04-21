---
name: basho-outreach
description: Draft basho-style outreach emails — short, highly-personalised first-touch emails built on John Barrows' framework (specific hook → credibility → relevance → low-friction ask). Use whenever the user asks for help writing a first-contact email to a recruiter, prospect, partner, investor, or anyone they want to open a relationship with. Trigger on phrases like "write a cold email", "draft an intro", "reach out to [name]", "basho", "first-touch", or when the user provides a recipient's name, firm, and something specific they've done/said. Do NOT trigger for follow-ups, replies, or bulk sequences — basho is a one-at-a-time tool.
---

# Basho-style outreach

## What basho is (and isn't)

A basho email is a single, hand-crafted first-touch email aimed at opening a relationship with one specific person. It trades volume for hit rate. The whole idea is that the recipient can tell, in the first sentence, that you wrote this to them and not to a list.

It is **not** a templated sequence, a follow-up, or a nudge. If the user asks for any of those, stop and tell them — basho is the wrong tool.

Generic AI-generated outreach is the enemy here. If what you're drafting could plausibly be sent to 50 other people with find-and-replace, you have failed. Specificity is the whole game.

## Configure this skill before first use

This skill is context-hungry. It needs to know who the user is before it can write credibility paragraphs on their behalf. On first use in a new environment, read `CONFIG.md` at the root of this repo — it defines:

- The user's name, role, and firm
- Who their ICP is (who they typically write to)
- Named clients / references safe to cite
- Voice preferences (British vs US spelling, any words to avoid)
- Any house rules (e.g. "never claim a specific % savings")

If `CONFIG.md` doesn't exist or is missing values, **ask the user for them before drafting**. Do not invent a role or firm.

## The four-part structure

Every basho email has these parts, in this order. Don't invent a fifth part.

1. **Subject line** — mirror something the recipient has publicly said or done. Not a pitch, not a teaser. A phrase that signals "I've read your stuff." If you can't find something specific enough for the subject line, the recipient isn't ready to be contacted.

2. **Hook (paragraph 1)** — reference one specific, verifiable thing. A post they wrote, a placement they ran, a client they serve, a panel they spoke on, a number they quoted. One thing, named precisely. Never "your impressive work" or "your thought leadership." If it wouldn't be true about any other person in their role, it's not specific enough.

3. **Credibility + why-now (paragraph 2)** — two jobs:
   - Establish the user is worth the recipient's time: their role, the kind of firm they serve, and — if relevant — named clients safe to cite (pulled from `CONFIG.md`).
   - Explain why they're reaching out *now*. Not "I'd love to connect" — a real reason. E.g., "at the stage where it's worth keeping a small group of trusted recruiters close," or "your firm's spend in this area has grown alongside [X], which is exactly the territory we work in."

4. **CTA (paragraph 3)** — a specific meeting ask with a specific slot. "20 minutes Thursday at 3pm, or would early next week suit?" beats "let me know when works" every time. Low commitment (15–20 min), clear day/time, easy to say yes or no to.

Close with "Best, [user's first name]" — nothing else. No signature block, no disclaimer.

## Research gate — the non-negotiable part

Before drafting a single word, you need these inputs:

- Recipient's **first name**, **firm**, and **role**
- **One specific thing** they've publicly done/said/run — LinkedIn post, placement, panel, published number, named client, sector focus
- The user's **relevance angle** — why *they* specifically are emailing *this* specific person *now*
- A **concrete slot** for the ask (day + time + timezone)

If any of these are missing from the user's brief, **ask before drafting**. Do not invent specifics. Do not guess at the recipient's focus. Filler is the failure mode — the user would rather answer three questions than receive a draft with `[specific post about X]` in it.

One useful nudge if they say "just draft something": remind them of the rule — "Never send without filling every variable. If you can't fill one, the recipient isn't worth contacting yet."

## Voice and style

Default style rules (override these in `CONFIG.md` if the user writes differently):

- **No buzzwords.** Never: synergy, leverage, best-in-class, impactful, circle back, move the needle, unlock value, drive growth, game-changing, revolutionary.
- **No opener pleasantries.** "I hope this finds you well" is an instant delete. Start with the hook.
- **Short sentences mixed with one or two longer ones.** Under 25 words each. No hedge-stacks ("it could potentially be argued…").
- **Measured, honest language** about what the user's firm does. No superlatives, no unverifiable claims.
- **First-person, confident.** "I run…", "I've spent…", "I'd value 20 minutes." Not "we at [firm] would love to…"
- **Numbers as digits** (3x, 25%, 20 minutes).
- **Total length: roughly 120–160 words.** If it's longer, you're padding. If it's much shorter, you haven't done the credibility work.

## Variants

Basho works for several relationship types. The structure is identical; the content of each part shifts.

- **Recruiter outreach** — open a long-term relationship, not chase a role. See `assets/recruiter-template.md`.
- **Prospect outreach** — a decision-maker at a target-ICP firm. Hook must be about their firm's specific situation — a regulatory change, a named peer they'd recognise, or a specific public signal (earnings call mention, hiring pattern, M&A activity). See `assets/prospect-template.md`.
- **Partner / ecosystem outreach** — vendors, consultants, analysts, industry figures adjacent to the user's market. See `assets/partner-template.md`.

Read the relevant template before drafting. They are not fill-in-the-blanks — they are shape references.

## Output format

When producing the draft, structure it exactly like this so the user can scan, edit, and approve quickly:

```
**Subject:** <subject line>

<paragraph 1 — hook>

<paragraph 2 — credibility + why-now>

<paragraph 3 — CTA with specific slot>

Best,
<user's first name>
```

Under the draft, include a short block titled **"Variables used"** listing the specific inputs you drew on (the named post/placement/client, the slot you proposed, etc.). This lets the user sanity-check the research before sending.

If you had to make any assumption — even a small one — flag it under **"Assumptions to verify"** directly beneath. Better to surface a guess than bury it.

## What good looks like

- Recipient reading paragraph 1 thinks "this person actually knows what I do."
- Paragraph 2 lands the "worth 20 minutes" case without puffery.
- Paragraph 3 makes saying yes a two-word reply.
- Nothing in the email could be cut and pasted into an email to someone else in their role.

## Common failure modes to avoid

- Opening with a compliment that isn't tied to a specific artefact ("I've been really impressed by your work").
- Vague credibility ("we work with many top-tier firms") instead of naming 2–3 clients.
- Asking for a call "when it suits" instead of proposing a slot.
- More than one ask. Basho has one CTA. If there's a second ask, cut it.
- Sending before the research is done. If in doubt, ask one more question instead of drafting.
