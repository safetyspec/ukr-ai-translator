# Ukrainian Localization Reference for AI

> A drop-in reference document that makes AI translate English to **natural** Ukrainian — not the awkward, Russified, calque-ridden version most LLMs produce by default.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Status: v1.1](https://img.shields.io/badge/version-1.1-blue.svg)](./CHANGELOG.md)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](./CONTRIBUTING.md)

---

## The Problem

If you've ever asked ChatGPT, Claude, Gemini, or any LLM to translate English to Ukrainian, you've probably noticed the output is **technically Ukrainian but reads wrong**.

The grammar is correct. The words exist. But a native speaker can tell within one sentence that something is off:

| English | ❌ What AI usually produces | ✅ What it should be |
|---|---|---|
| Please submit your weekly report by Friday. | Будь ласка, надішліть ваш тижневий звіт до п'ятниці. | Звіт за тиждень надсилайте до п'ятниці. |
| Stop wasting time on spreadsheets. | Перестаньте витрачати час на електронні таблиці. | Менше таблиць — більше справжньої роботи. |
| Hi John, just a friendly reminder... | Привіт Джон, просто дружнє нагадування... | Іване, нагадуємо: ... |

This happens because AI models translate **sentence-by-sentence**, preserving English word order, idioms, and tone. They also lean heavily on Russian-influenced vocabulary from their training data. The result reads like English wearing a Ukrainian costume.

## The Solution

This repository contains a structured reference document that you load into your AI tool's context (Claude Projects, ChatGPT Custom GPTs, Cursor rules, system prompts, etc.). It encodes:

- **Grammar rules** that matter for translation quality (word order, verb aspect, cases, vocative)
- **Russification anti-patterns** — ~60 words and 6 syntax patterns to avoid
- **Tone & register guidance** for different content types (business, marketing, casual, social, creative, legal)
- **IT/SaaS terminology glossary** (~150 locked terms)
- **Side-by-side examples** of bad-vs-good localization
- **A pre-output checklist** the AI runs before responding

The result: AI output that reads like a native Ukrainian-speaker actually wrote it.

## Quick Start

### 1. Pick the doc that matches your use case

- **[`docs/general.md`](./docs/general.md)** — Universal reference. Use this for any general translation work.
- **[`docs/domain-supplements/`](./docs/domain-supplements/)** — Domain-specific supplements (e.g., trucking/logistics). Load alongside `general.md`.

### 2. Load it into your AI tool

Pick the integration that matches your tool:

- **[Claude Projects](./docs/usage/claude-projects.md)**
- **[ChatGPT Custom GPT](./docs/usage/chatgpt-custom-gpt.md)**
- **[Cursor / IDE rules](./docs/usage/cursor-rules.md)**
- **[Generic system prompt](./docs/usage/system-prompt-template.md)** (for API calls, other LLMs)

### 3. Test it

Paste a paragraph of bad-translated Ukrainian into your configured AI and ask it to fix. You should see immediate improvement. If you don't — that's a signal something's off in your setup; check the integration doc.

### 4. Iterate

When you spot bad output, add it to the reference doc as a new side-by-side example. The doc improves over time as you encounter real-world edge cases. (See [CONTRIBUTING.md](./CONTRIBUTING.md) for how to upstream fixes.)

## Who This Is For

- **Developers** building Ukrainian-language features into products
- **Marketers** localizing campaigns for Ukrainian audiences
- **Content teams** translating documentation, support articles, blog posts
- **Solo founders** running Ukrainian SaaS who need consistent terminology
- **Translators** using AI as a first-draft tool
- **Anyone** tired of fixing the same calques over and over

## Who This Is NOT For

- **Professional literary translation** of fiction or poetry — this doc helps AI produce competent functional Ukrainian, but literary translation requires a human with cultural and stylistic judgment far beyond what any rules file can encode.
- **Replacing a human native-speaker editor** for high-stakes content (legal contracts, medical materials, government filings). This doc improves AI output dramatically, but for critical content you still need a human reviewer.

## Repository Structure

```
ukrainian-localization-reference/
├── README.md                          ← you are here
├── LICENSE                            ← MIT
├── CONTRIBUTING.md                    ← how to propose changes
├── CHANGELOG.md                       ← version history
│
├── docs/
│   ├── general.md                     ← main reference doc
│   ├── domain-supplements/
│   │   └── trucking.md                ← industry-specific overrides
│   └── usage/
│       ├── claude-projects.md
│       ├── chatgpt-custom-gpt.md
│       ├── cursor-rules.md
│       └── system-prompt-template.md
│
└── examples/
    ├── before-after.md                ← real translation examples
    └── industry-supplements/
        └── template.md                ← scaffold for new domain docs
```

## Coverage

The general reference doc covers:

- **Both modern standard Ukrainian** (Kyiv-based, post-2019 reforms) **and diaspora Ukrainian** (US/Canada/UK communities with English influences) — with explicit guidance on when to use each
- **Seven content types**: business/professional, product/SaaS, marketing, casual/personal, social media, creative writing, legal
- **All major Russification traps**: vocabulary, syntax patterns, Soviet-era business jargon
- **Правопис 2019** (modern Ukrainian orthography reform)
- **Common false friends**: e.g., "мітинг" means *political rally*, not *business meeting*
- **Convention adaptation**: dates, times, numbers, currency, quotation marks

## Real-World Use

This reference is actively used in production by **FleetCtrl**, a US trucking compliance SaaS serving Ukrainian-speaking fleet operators. The trucking domain supplement included here (`docs/domain-supplements/trucking.md`) was developed for FleetCtrl's day-to-day translation workflows — driver compliance docs, IFTA reports, customer-facing product copy — and contributed back to this repository as an example of how to extend the general reference for a specific industry.

Native-speaker feedback from working professionals (not academic linguists) shapes every release. If you're using this reference in production and have corrections or domain supplements to contribute, your input is what makes this resource better than a textbook.

## A Note on Honesty

This reference document was **compiled with AI assistance** based on standard Ukrainian grammar references and refined through native-speaker feedback. It is **not** the work of a credentialed linguist or a professional translator.

It is a working community resource — pragmatic, opinionated, and intended to be improved through real-world use. If you spot something wrong, open an issue or PR. Native-speaker corrections are especially welcome and are explicitly credited in the changelog.

The goal is **good enough to ship**, not academic perfection. If you need academic perfection, hire a professional translator.

## Contributing

Contributions are very welcome. The most valuable ones:

- **Native-speaker corrections** with explanation of why the current form is wrong
- **New side-by-side examples** of bad-vs-good translations from real AI output
- **New domain supplements** (medical, finance, legal, gaming, etc.)
- **Integration guides** for additional AI tools

See [CONTRIBUTING.md](./CONTRIBUTING.md) for the full guidelines.

## License

MIT. Use it however you want. Attribution appreciated but not required.

## Acknowledgments

Built with native-speaker input from working professionals who use AI translation daily and got tired of fixing the same mistakes. Grammar references drawn from Pugh & Press, *Ukrainian: A Comprehensive Grammar* (Routledge) and the broader corpus of modern Ukrainian style guides.
