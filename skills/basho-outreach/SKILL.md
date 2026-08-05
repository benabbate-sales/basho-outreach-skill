---
name: basho-outreach
description: >-
  Draft a basho-style first-touch email — one hand-crafted message to one named person, built on
  the hook, credibility, why-now, low-friction-ask structure. Use whenever someone wants to open
  a relationship with a recruiter, a prospect, a partner, an investor or anyone else: write a
  cold email, draft an intro, reach out to this person, first touch, basho. Reads an operator
  profile at run time — a CONFIG file, or the canon of the repo it is installed in — for who the
  sender is, what they may claim and whose names they may use; where neither exists it asks
  rather than inventing. Do NOT use for follow-ups, replies, nudges or bulk sequences: basho is
  one at a time. Where those skills are installed, use job-application-push to apply for a role,
  interview-prep for a booked call, linkedin-discoverability for profile work, and
  gtm-content-engine for marketing copy.
---

# Basho-style outreach

**Build:** `basho-outreach · 2026-08-05 · canon-optional-rebuild`

One hand-crafted first-touch email to one specific person. It trades volume for hit rate: the
recipient can tell from the first sentence that it was written to them and not to a list.

It is **not** a sequence, a follow-up, or a nudge. If that is what is wanted, say so and stop —
basho is the wrong tool for it.

## Two layers — the framework, and the operator

This skill runs standalone or inside someone's own repo, so it is explicit about which half is
which:

- **The framework is here.** The four parts, the length band, the one-CTA rule, the research gate,
  the failure modes. These are properties of the method, they are the same for every sender, and
  the skill must work with nothing but this file.
- **The operator is not here.** Who is sending, what they are allowed to claim, whose names may
  appear, house voice rules — **never hard-code any of it into this file.** It is read at run time
  from the operator profile below. A skill that remembers an employer, a client name or a metric
  will still be repeating it a year after it stopped being true, in a first email, to someone who
  can check.

## Load the operator profile — before drafting a word

In this order, and stop at the first that exists:

1. **The repo's own canon.** If this skill is installed inside a repo that defines the operator in
   its own files, read those. Repos that do this usually route them from a `CLAUDE.md` or equivalent
   at the root — **read that routing and follow it** rather than guessing filenames. Typical
   routing: who the operator is, what figures and claims are cleared, what is barred, and the voice
   files anything human-facing is written from.
2. **`CONFIG.md`** at the skill or repo root.
3. **Neither exists → interview the user.** Ask for the fields below and draft nothing until they
   are answered.

**Precedence: repo canon beats CONFIG beats anything remembered.** If this skill appears to
disagree with the operator's canon, canon wins and the skill is stale — say so in the output.

**What the profile has to supply:** the sender's name, role and firm · what the firm does, in the
sender's own words · who they typically write to · the proof points and figures they may cite, and
any that are barred · which names — clients, employers, references — may appear, and which may not
· voice preferences, including spelling convention and words to avoid · any house rules.

**Failure mode — stop, don't improvise.** If the profile cannot be read and the user cannot be
asked, **stop and say so. Never draft a credibility paragraph from memory or inference.** A first
email is the one artefact where being wrong is unrecoverable: it goes to a named stranger who can
check, over the sender's name, and it cannot be retracted. No profile, no draft.

## Naming names — the rule the credibility paragraph turns on

**Default to anonymising other people's business.** A client, customer or engagement is described
by shape — *a Series-B payments company*, *a Tier-1 bank's market-data function* — not by name.

**The sender's own employers, roles and record are the carve-out**: those are their positioning
proof and they are nameable, subject to whatever the profile clears.

**A third party's name goes in only where the profile explicitly says it may.** Silence is not
permission — if the profile does not clear a name, it is not cleared. Say so, and use the shape
instead. Where the profile bars a figure or a claim, it is barred here too; this skill never carries
its own list of what is safe to say.

## The research gate — non-negotiable

Before drafting, you need: the recipient's **first name, firm and role**; **one specific,
verifiable thing** they have done, said, published or run; the **sender's relevance angle** — why
this sender, to this person, now; and a **concrete slot** for the ask, with day, time and timezone.

**If any of these is missing, ask. Do not invent specifics and do not guess at the recipient's
focus.** Filler is the failure mode: the user would rather answer three questions than receive a
draft with `[specific post about X]` in it.

If the user says *"just draft something"*, hold the line: if a variable cannot be filled, the
recipient is not ready to be contacted yet.

## The four parts

**Subject.** Mirror something the recipient has publicly said or done. Not a pitch, not a teaser. If
nothing specific enough exists for the subject line, that is the research gate failing, not a
licence to generalise.

**Paragraph 1 — the hook.** One specific, verifiable thing, named precisely. A post, a placement, a
panel, a deal, a number they quoted. Never *your impressive work* or *your thought leadership*.
**The test: if it could be true of anyone else in their role, it is not specific enough.**

**Paragraph 2 — credibility and why-now.** Two jobs. Establish that the sender is worth the
recipient's time — role, the kind of firm they serve, and proof cleared by the profile, named
within the rules above. Then say why *now*, with a real reason rather than *I'd love to connect*.

**Paragraph 3 — the ask.** One CTA, low commitment, with a specific slot proposed. *Twenty minutes
Thursday at 3pm, or would early next week suit?* beats *let me know when works*. A second ask
halves the first one — if there are two, cut one.

Close with the sender's first name. No signature block, no disclaimer, no postscript.

**Length: roughly 120–160 words.** Longer means padding; much shorter means the credibility work
was skipped. This is a framework parameter, not an operator preference — but if the profile sets
its own, the profile wins.

## Variants — same structure, different content

- **Recruiter.** The goal is to open a long-term relationship, not to chase a role. The hook is
  their placements or their read of the market; the why-now is worth being explicit about — keeping
  a small group of trusted recruiters close, whether or not the sender is actively looking. Never
  ask about a specific vacancy in a first email.
- **Prospect.** A decision-maker at a target firm. The hook must be about *their firm's* situation
  — a regulatory change, a named peer they would recognise, an earnings-call remark, a hiring
  pattern, an acquisition. Their firm's public signals, not the sender's product.
- **Partner or ecosystem.** Vendors, consultants, analysts, adjacent operators. The hook is usually
  a shared audience or a shared problem, and the ask is a conversation between peers, not a pitch.
  Being useful before being interesting is the whole play.

## Voice — framework defaults, overridden by the profile

Where the operator profile sets a rule, it wins. Absent one:

- **No buzzwords.** Not: synergy, leverage, best-in-class, impactful, circle back, move the needle,
  unlock value, drive growth, game-changing, revolutionary.
- **No opener pleasantries.** *I hope this finds you well* is an instant delete. Open on the hook.
- **Short sentences, with one or two longer ones for rhythm.** No hedge-stacks.
- **Measured and honest.** No superlatives and no unverifiable claims — a first email is the worst
  possible place to be caught overstating.
- **First person and direct.** *I run…*, *I've spent…*, *I'd value twenty minutes* — not *we at
  [firm] would love to…*
- **Numbers as digits.**

## Output format

```
**Subject:** <subject line>

<paragraph 1 — hook>

<paragraph 2 — credibility + why-now>

<paragraph 3 — one ask, with a specific slot>

Best,
<sender's first name>
```

Then two blocks beneath it, always:

- **Variables used** — the specific inputs drawn on: the named post or placement, the proof points
  cited and where the profile cleared them, the slot proposed. This is what lets the sender check
  the research before sending.
- **Assumptions to verify** — anything inferred, however small. Better surfaced than buried. If
  there are none, say so rather than dropping the block.

**Draft only.** This skill does not send, schedule or queue anything. Where the operator's canon
gates outbound messages to a person, that gate applies here: show the exact text and wait.

## What good looks like

- Reading paragraph 1, the recipient thinks *this person actually knows what I do*.
- Paragraph 2 makes the twenty-minute case without puffery.
- Paragraph 3 can be answered with two words.
- **Nothing in the email could be pasted into an email to anyone else in the same role.** That is
  the whole test; if it fails, the draft is not finished.

## Failure modes seen in the wild

- A compliment not tied to a specific artefact — *I've been really impressed by your work*.
- Vague credibility — *we work with many top-tier firms* — where a shape or a cleared name belongs.
- Asking for a call *when it suits* instead of proposing a slot.
- More than one ask.
- Drafting before the research is done. When in doubt, ask one more question.
- **Reaching for a name, a figure or a claim the profile has not cleared.** Use the shape, and say
  which check it failed.

---
*Rebuilt 5 Aug 2026 to `NEW-SKILL-STANDARD.md` as a **canon-optional** build: one file that ships
byte-identical standalone and inside an operator's own repo, because two builds of the same method
is the drift this rebuild exists to remove. The prior build read a `CONFIG.md` that existed in no
copy of the repo, and told the reader to open three `assets/*-template.md` files that were never
packaged — so both of its dependencies were dangling and its only fallback was to improvise. The
variants are folded into this file for that reason. **This file greps clean for values**: the only
digits are the length band and the twenty-minute example, both framework parameters, both
overridable by the profile.*
