# Using This Reference with Cursor / IDE AI

If you're a developer building Ukrainian-language features (UI strings, error messages, marketing copy, documentation), you can configure your AI coding assistant to apply localization rules whenever it generates Ukrainian text.

## Cursor (`.cursorrules`)

Cursor reads a file called `.cursorrules` in your project root and applies it to every AI interaction in that project.

### Setup

1. In your project root, create a file named `.cursorrules` (note the leading dot)
2. Paste the content below
3. Commit it to your repo so the whole team benefits

### `.cursorrules` content

```
# Ukrainian Localization Rules

When generating, translating, or modifying ANY Ukrainian text in this
codebase, follow these rules. These apply to: UI strings, error messages,
marketing copy, user-facing content, documentation, comments in Ukrainian,
and any English→Ukrainian translation.

## Core principle
LOCALIZE, don't translate. Restructure sentences for natural Ukrainian flow,
not English word order. New/important information goes at the END of the
sentence (rheme position).

## Grammar rules
- Use vocative case for direct address: "Іване" not "Іван", "клієнте" not "клієнт"
- Drop unnecessary possessives ("ваш/мій/свій") and personal pronouns —
  Ukrainian uses far fewer than English
- Pick the right verb aspect: perfective for completed (Зберегти, Видалити),
  imperfective for ongoing/habitual, imperfective for negative imperatives
  (Не натискайте, not Не натисніть)
- Numbers govern cases: 1 → nom sing, 2-4 → nom plur, 5+ → gen plur

## Avoid Russifications
- "відповідно до" not "у відповідності з"
- "протягом" not "на протязі"
- "брати участь" not "приймати участь"
- "є" or em-dash, not "являється"
- "скасувати" not "відмінити"
- "оновити" not "обновити"
- "наступний" not "слідуючий"
- "наразі" / "зараз" not "у даний момент"
- "наступного тижня" not "у наступному тижні"
- Avoid "по + dative" — use "про/щодо/з/за"
- Avoid active participles in -чий/-щий — use relative clauses with "який/що"

## Avoid English calques
- "reach out" → "зв'язатися", not "дотягнутися"
- "follow up" → "нагадати", not "слідувати за"
- "moving forward" → "надалі", not "рухаючись вперед"
- "at the end of the day" → "зрештою", not "в кінці дня"

## False friends — DO NOT confuse
- "мітинг" = political rally, NOT business meeting. Use "зустріч" or "нарада"
- "магазин" = shop, NOT magazine. For magazine use "журнал"
- "фабрика" = factory, NOT manufacturer

## Modern spelling (Правопис 2019)
- "проєкт" not "проект"
- Apostrophes mandatory: "об'єкт", "п'ять", "ім'я"

## Tech/SaaS terminology defaults
- Header → Хедер (NOT "шапка" or "заголовок" for site header)
- Footer → Футер (NOT "підвал" or "нижній колонтитул")
- Account → Акаунт (informal) or Обліковий запис (formal)
- Settings → Налаштування
- Update → Оновити (NOT "обновити")
- Cancel → Скасувати (NOT "відмінити")
- Save → Зберегти
- Delete → Видалити
- Notification → Сповіщення (NOT "нотифікація")
- App → Додаток or Застосунок
- Project → Проєкт
- Meeting → Зустріч or Нарада (NEVER "мітинг")

## UI copy specifics
- Buttons: 1-3 words, imperative perfective (Зберегти, Скасувати, Надіслати)
- Section headers: noun phrases (Налаштування, Профіль)
- Error messages: blameless, clear, actionable. Use impersonal:
  "Не вдалося зберегти" not "Ми не змогли зберегти"
- Required field: "Обов'язкове поле"
- Loading: "Завантаження..."

## Register
- Default to formal "Ви" (capitalize in formal correspondence)
- Use lowercase "ви" in marketing/general broad-audience content
- Use "ти" only in casual/youth-oriented contexts

## Conventions
- Dates: DD.MM.YYYY
- Time: 24-hour format (15:00, not 3:00 PM)
- Decimal separator: comma (3,5 not 3.5)
- Thousands separator: space (1 000 000)
- Quotation marks: «лапки-ялинки» for primary, „лапки" for nested
- Em-dashes liberally for rhythm

## Final check before outputting any Ukrainian text
Ask: "Would a native Ukrainian-speaker who has never seen the English
original write this sentence this way?" If no, rewrite.

For the full reference doc with extended grammar rules, complete
Russification list, side-by-side examples, and IT/SaaS glossary, see:
https://github.com/safetyspec/ukr-ai-translator/blob/main/docs/general.md
```

### Test it

In a project with this `.cursorrules` file, ask Cursor to translate something:

> Translate this to Ukrainian: "Please save your changes before leaving this page."

Expected output: *"Збережіть зміни перед виходом зі сторінки."*

Not: *"Будь ласка, збережіть ваші зміни перед тим, як покинути цю сторінку."*

---

## Other AI coding tools

### GitHub Copilot Chat (with Copilot Workspace or custom prompts)

GitHub Copilot doesn't support a project-level rules file the same way Cursor does, but you can:

1. Add the rules to a `COPILOT.md` or `AI_GUIDELINES.md` file in your repo
2. Reference it explicitly in prompts: "Following AI_GUIDELINES.md, translate..."
3. Some workspaces support `.github/copilot-instructions.md` — check current Copilot docs

### Continue.dev

Continue supports custom system prompts per-model. Paste the compressed rules into the system prompt for your translation workflows.

### Aider

Aider supports a `.aider.conf.yml` with a `prompt` section. Paste the rules there.

### Cline / Roo Code (VS Code extensions)

These respect `.cursorrules` or have their own equivalent. Check current docs.

---

## Tips for codebases with localization files

If you have `i18n` JSON/YAML files with English keys and Ukrainian translations, you can:

1. Ask the AI to **audit** existing translations against the rules
2. Use the rules to **generate new strings** consistently
3. Use the rules to **review PRs** that touch translation files

Example prompt:

> Audit the Ukrainian translations in `src/i18n/uk.json` against the rules
> in `.cursorrules`. Identify any:
> - Russifications
> - Calques from English
> - Inconsistent terminology (same English word translated differently)
> - Missing vocative cases in user-facing strings
> - Wrong verb aspects in button labels
>
> Output a table of issues to fix.

This is one of the highest-leverage uses of this reference: cleaning up existing localization debt in a real codebase.
