---
name: Bad Translation Detected
about: Report bad AI Ukrainian output and propose a fix
title: "[BAD TRANSLATION] "
labels: bad-translation
assignees: ''
---

## English source

> [paste the exact English text the AI was asked to translate]

## AI output

> [paste the exact Ukrainian output the AI produced]

**AI tool / model:** [e.g., Claude Opus 4.7 / GPT-4o / Cursor with Sonnet 3.5 / etc.]

**Reference doc version used (if any):** [v1.0 / v1.1 / no reference doc / unsure]

## What's wrong

[Describe the specific issues. Be concrete — point to specific words, structures, or rules.]

Examples of useful descriptions:
- "Uses 'являється' instead of 'є' (Russification — see Section 3.2 Pattern 3)"
- "Doesn't use vocative case for direct address — should be 'Іване' not 'Іван'"
- "Wrong verb aspect — uses imperfective where perfective is needed for a one-time action"
- "Calque of 'reach out' as 'дотягнутися' — should be 'зв'язатися'"

## Corrected version

> [paste the version you think is correct]

## Why your version is better

[Explain the localization choices. This is the most valuable part of the issue — it teaches the reference doc.]

## Rule references

Which sections of `docs/general.md` (or domain supplement) apply? If this is a new pattern not yet covered, say so.

## Would you accept this becoming a new side-by-side example?

- [ ] Yes, add to `examples/before-after.md` (with credit to me)
- [ ] Yes, but anonymously
- [ ] No, just fix the rule
