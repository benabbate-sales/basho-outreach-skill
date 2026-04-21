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

## Credit

Built by Ben. The underlying framework is John Barrows' [basho approach](https://www.jbarrows.com/).

## License

MIT — see [LICENSE](LICENSE). Fork it, adapt it, ship it. If you make it better, a link back is appreciated but not required.
