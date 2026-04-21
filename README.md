# Basho Outreach — a Claude skill for first-touch emails

A [Claude skill](https://support.claude.com/en/articles/12111783-using-skills-in-claude-ai) that helps you draft **basho-style** first-touch emails — short, hand-crafted, highly-personalised messages built on John Barrows' framework.

Basho trades volume for hit rate. The whole idea is that the recipient can tell, in the first sentence, that you wrote this to them and not to a list.

## Who this is for

Anyone who has to open cold relationships by email and is tired of generic AI slop:

- Enterprise AEs writing to prospects.
- Founders writing to investors, partners, design partners.
- Candidates opening relationships with recruiters.
- Anyone sending a real email to one real person.

It is **not** for: bulk sequences, follow-ups, replies, or anything where the same email could be sent to 50 people with find-and-replace.

## Why this exists

Most AI-generated outreach is the thing that killed cold email for everyone.

This skill forces the opposite discipline:

- **Research gate.** Claude won't draft until you've named one specific, verifiable thing the recipient has publicly said or done. No "your impressive work." No `[specific post about X]` placeholders.
- **Fixed four-part structure.** Subject → hook → credibility + why-now → specific-slot CTA. Nothing else.
- **120–160 words, no buzzwords.** If it sounds like a template, it's been rejected.
- **One-at-a-time only.** If you ask for a sequence, a follow-up, or a bulk draft, the skill will stop and tell you basho is the wrong tool.

If the recipient isn't specific enough to write a real subject line about, the skill's answer is: they're not ready to be contacted yet.

## Quickstart

1. **Clone or download** this repo.
2. **Fill in [`CONFIG.md`](CONFIG.md)** — your name, role, firm, ICP, named clients, voice rules. The skill reads this to write credibility paragraphs in your voice. There's a filled-in example at the bottom of that file.
3. **Drop the `skills/basho-outreach/` folder** into your Claude skills directory (Cowork, Claude Code, or the Claude desktop app's skills settings).
4. **In any chat**, ask Claude something like *"draft a basho email to Jane Doe at Acme — she just posted about vendor consolidation"* — the skill will trigger automatically and walk you through the research gate.

Full instructions for installing Claude skills: [Anthropic's skills docs](https://docs.claude.com/en/docs/build-with-claude/skills).

## Skills in this repo

| Skill | What it does |
|-------|--------------|
| [basho-outreach](skills/basho-outreach/SKILL.md) | Drafts a single basho-style first-touch email after a research gate. Variants for recruiters, prospects, and partners. |

## Example trigger phrases

- "Write a cold email to Jane Doe at Acme."
- "Draft an intro to that recruiter at Heidrick."
- "Basho to the CFO at [firm]."
- "Reach out to [name] — they just posted about X."

It will **not** trigger on: follow-ups, replies, sequences, bulk outreach. Those are different problems.

## What a good basho email looks like

The recipient reads paragraph 1 and thinks *"this person actually knows what I do."* Paragraph 2 lands the "worth 20 minutes" case without puffery. Paragraph 3 makes saying yes a two-word reply. Nothing in the email could be cut-and-pasted to anyone else in their role.

See [`skills/basho-outreach/assets/`](skills/basho-outreach/assets/) for shape references — recruiter, prospect, and partner variants. They are not fill-in-the-blanks. They are examples of the right skeleton.

## Example output

Here's the kind of email this skill produces — a recruiter-variant basho, drafted from the filled-in `CONFIG.md` example at the bottom of that file.

<details>
<summary>Click to expand example email</summary>

> **Subject:** Your placements in vertical-SaaS sales leadership
>
> Hi Alex,
>
> I read your piece last month on the collapse of pure-hunter roles at growth-stage vertical SaaS firms — specifically your point about PLG motions pushing the AE archetype toward embedded land-and-expand. It maps closely to the shift I've been navigating on the other side of the table.
>
> I'm Head of Revenue at Northline Labs — we help 200–2000-person B2B SaaS firms consolidate data-vendor contracts. Before this, I led commercial teams at Acme Cloud and Redwood Systems through exactly the transition you described. I'm not actively looking, but I'm at the stage where it's worth keeping a small group of trusted recruiters close — people who genuinely know the market.
>
> Would 20 minutes on Thursday at 3pm EST work, or is early next week better?
>
> Best,
> Dana

**What to notice:**

- Subject mirrors a specific piece the recipient wrote — not a pitch.
- Paragraph 1 references one verifiable thing (the piece + a precise point from it). No "your impressive work."
- Paragraph 2 uses named clients (Acme Cloud, Redwood Systems) and a real "why now" — not "I'd love to connect."
- CTA proposes a specific slot with timezone. Easy yes/no.
- 138 words total. No buzzwords. First-person, measured.

</details>

## Credit

Built by [Ben Abbate](https://github.com/benabbate-sales). The underlying framework is John Barrows' [basho approach](https://www.jbarrows.com/).

## License

MIT — see [LICENSE](LICENSE). Fork it, adapt it, ship it. If you make it better, a link back is appreciated but not required.
