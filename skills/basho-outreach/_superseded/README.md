# Superseded — the three variant templates

**These are no longer read by the skill. Kept for reference, not for drafting.**

Until 5 Aug 2026 `SKILL.md` instructed *"read the relevant template before drafting"* and pointed
at `assets/recruiter-template.md`, `prospect-template.md` and `partner-template.md`. Two problems
came out of that arrangement:

1. **The packaged build could ship without them.** The install running in the author's own
   environment had `SKILL.md` and nothing else — the templates existed here, in the public repo, and
   not in the package that actually ran. A skill whose method depends on files it cannot guarantee
   are present has a silent failure mode: it improvises, and the output looks the same.
2. **A template is a shape, and shapes are cheap to state.** The difference between a recruiter, a
   prospect and a partner first-touch is a paragraph each — hook material, why-now, and what the ask
   can reasonably be. That now lives in `SKILL.md` under *Variants*, where it cannot go missing.

If you are looking for the worked examples, they are still here. If you are drafting, use the skill.
