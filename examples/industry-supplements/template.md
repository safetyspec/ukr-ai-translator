# [Industry Name] Localization Supplement

**Version:** 1.0
**Status:** Template — fill in for your domain
**Parent doc:** Loads alongside `docs/general.md`

This is a scaffold for creating a new industry-specific supplement. Replace placeholder text with your domain's content.

---

## Purpose

This supplement adds [INDUSTRY] specific overrides and additions to the general Ukrainian localization reference. Load both `docs/general.md` and this file into your AI tool for the best results in [INDUSTRY] content.

## Scope

**This supplement covers:**
- [list content types specific to your industry: e.g., customer support tickets, technical documentation, regulatory filings, marketing to industry audiences]

**This supplement does NOT cover:**
- [list things outside scope]
- Universal grammar, Russifications, and tone rules — those are in `general.md`

## Audience

[Describe the typical reader of [INDUSTRY] content in Ukrainian. Are they native speakers in Ukraine? Diaspora? Bilingual professionals? Working class? Etc. This shapes register and vocabulary choices.]

---

## 1. The Formal vs Operational Register Hierarchy

[Most industries have a tension between casual "how people actually talk" language and formal "what regulators/legal require" language. Document yours here.]

| Concept | Operational default | Formal default |
|---|---|---|
| [Term 1] | [Casual UA term] | [Formal UA term] |
| [Term 2] | [Casual UA term] | [Formal UA term] |
| ... | | |

**When to use which:**
- Operational: [list contexts — internal emails, marketing, customer chat, etc.]
- Formal: [list contexts — contracts, government filings, insurance, etc.]

## 2. Forbidden Words

Words that are wrong in this domain regardless of context. These are not stylistic preferences — they're errors.

- ❌ "[wrong term]" — [reason it's wrong]. Use **[correct term]** instead.
- ❌ "[wrong term]" — [reason]. Use **[correct term]**.

## 3. Industry Glossary

Locked terminology. Same English term → same Ukrainian term every time.

### 3.1 [Subdomain — e.g., "People & Roles"]

| English | Ukrainian | Notes |
|---|---|---|
| [Term] | [Translation] | [Context, alternates, formal/casual notes] |
| [Term] | [Translation] | |

### 3.2 [Subdomain — e.g., "Equipment / Products"]

| English | Ukrainian | Notes |
|---|---|---|
| | | |

### 3.3 [Subdomain — e.g., "Processes / Workflows"]

| English | Ukrainian | Notes |
|---|---|---|
| | | |

### 3.4 [Subdomain — e.g., "Regulatory / Compliance"]

| English | Ukrainian | Notes |
|---|---|---|
| | | |

[Add more subdomain glossaries as needed]

## 4. Industry-Specific Anglicisms

[If your industry uses many English borrowings — common in tech, finance, gaming, etc. — document which ones are accepted and which are not.]

### 4.1 Acceptable / Expected Anglicisms

| Anglicism (UA transliteration) | English origin | Notes |
|---|---|---|
| | | |

### 4.2 Anglicisms to AVOID

| ❌ Don't use | ✅ Use instead | English |
|---|---|---|
| | | |

## 5. Side-by-Side Examples

[Provide 3-5 real-world examples of bad-vs-good translations specific to your domain. These teach the AI faster than abstract rules.]

### Example 1: [Content type — e.g., "Customer Support Reply"]

**English source:**
> [English text]

**❌ Bad (typical AI output):**
> [What an AI without the supplement would produce]

**Problems:** [Specific issues — calques, wrong terminology, wrong register]

**✅ Good (localized):**
> [Correct version]

**Why it works:** [Explain the localization choices]

---

### Example 2: [Different content type]

[Same structure]

---

### Example 3: [Different content type]

[Same structure]

## 6. Tone Rules by Sub-Content-Type

[If your industry has multiple distinct content types — e.g., customer-facing marketing vs internal training docs vs regulatory filings — document tone rules for each.]

### 6.1 [Content type 1]
- [Rule]
- [Rule]

### 6.2 [Content type 2]
- [Rule]
- [Rule]

## 7. Domain-Specific Pre-Output Checks

[List 5-10 quick checks specific to your industry that the AI should run before outputting.]

1. ☐ [Check]
2. ☐ [Check]
3. ☐ [Check]

## 8. Version History

| Version | Date | Changes |
|---|---|---|
| 1.0 | [YYYY-MM] | Initial release. Covers [scope summary]. |

---

## Notes for the Maintainer

When updating this supplement:
1. Add new glossary terms as they come up in real work
2. Add new side-by-side examples when you catch the AI making the same mistake repeatedly
3. Document why a rule exists — future-you will forget
4. Get native-speaker review when possible
5. Don't duplicate rules already in `general.md` — only override or extend
