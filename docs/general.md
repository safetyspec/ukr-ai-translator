# Ukrainian Localization Reference (General Purpose)

**Version:** 1.1
**Purpose:** Canonical reference for any AI system performing English-to-Ukrainian translation, regardless of industry or use case. Designed to be read by an AI before producing any Ukrainian output.

**Scope:** Universal. Covers business/professional, casual/personal, creative writing, social media, and legal content. Covers both modern standard Ukrainian and diaspora-flavored Ukrainian with guidance on when to use each.

**How to use this doc:** Drop it into your Claude Project's knowledge. In the system prompt, instruct Claude to consult it before producing Ukrainian. Update over time as you spot issues.

**Note to the AI reading this:** You are not translating. You are localizing. If your output reads like a translation, you have failed. Read this document fully before producing Ukrainian. When in doubt, run the Section 10 checklist before responding.

---

## 1. Core Operating Principles

### 1.1 The Single Most Important Rule

**Do not translate sentence-by-sentence. Localize meaning-by-meaning.**

English and Ukrainian have fundamentally different sentence architectures. Preserving English word order in Ukrainian is the #1 source of "translated" feeling. A native Ukrainian speaker can detect a calque translation in under one second.

**Bad (translation):** *Будь ласка, надішліть ваші коментарі до п'ятниці.*
**Good (localization):** *Коментарі надсилайте до п'ятниці.*

The second version drops the unnecessary "please/your" filler that English requires for politeness but Ukrainian doesn't, uses topic-first word order natural to Ukrainian, and uses an imperative form a real person would actually write.

### 1.2 The Native Speaker Test

Before outputting any Ukrainian sentence, mentally ask:

> "Would a native Ukrainian-speaker who has never seen the English original write this sentence this way?"

If the answer is "probably no, they'd say it differently" — rewrite. Do not output text that fails this test.

### 1.3 Localize Idioms, Don't Translate Them

English idioms, phrasal verbs, and business clichés must never be translated word-for-word. Replace with Ukrainian equivalent or rewrite the underlying meaning.

| English | ❌ Wrong (calque) | ✅ Right (localized) |
|---|---|---|
| reach out | дотягнутися | зв'язатися, написати |
| follow up | слідувати за | нагадати, уточнити, повернутися до |
| moving forward | рухаючись вперед | надалі, у подальшому |
| at the end of the day | в кінці дня | зрештою, врешті-решт |
| touch base | торкнутися бази | зв'язатися |
| circle back | кружляти назад | повернутися до питання |
| game changer | змінювач гри | переломний момент, прорив |
| low-hanging fruit | низько висячі фрукти | легко досяжні цілі |
| heads up | голови вгору | до відома, попередження |
| think outside the box | думати поза коробкою | нестандартно мислити |
| ballpark figure | фігура з бейсбольного поля | приблизна цифра |
| break the ice | зламати лід | познайомитися ближче, розрядити обстановку |
| on the same page | на тій самій сторінці | дійти спільної думки, домовитися |
| hit the ground running | бігти по землі | одразу взятися до роботи |
| under the weather | під погодою | нездужати, погано почуватися |
| piece of cake | шматок торта | дрібниця, легка справа |
| once in a blue moon | раз у блакитний місяць | дуже рідко, раз на сто років |
| cost an arm and a leg | коштувати руки й ноги | коштувати дуже дорого, коштувати шалених грошей |

### 1.4 Default to Brevity

Ukrainian written communication is **more concise** than English. English padding words usually disappear in good Ukrainian. Cut, don't add.

- "Please be advised that..." → ❌ *Просимо взяти до відома, що...* → ✅ Just state the fact, or use *Зверніть увагу:*
- "We would like to inform you..." → ❌ *Ми хотіли б повідомити вас...* → ✅ *Повідомляємо:*
- "In order to..." → ❌ *Для того щоб...* → ✅ *Щоб...*
- "I just wanted to say..." → ❌ *Я просто хотів сказати...* → ✅ Just say it. Often drop entirely.
- "I hope this email finds you well" → ❌ *Сподіваюся, цей лист застане вас у доброму здоров'ї* → ✅ Drop entirely; Ukrainian business email opens with the point.

### 1.5 Localization Is Not Just Words — It's Conventions

When localizing, also adapt:
- **Date formats:** US "MM/DD/YYYY" → Ukrainian "DD.MM.YYYY" (e.g., "03/15/2026" → "15.03.2026"). Unless content is for a US-based Ukrainian audience that uses US formats.
- **Time:** US "3:00 PM" → Ukrainian "15:00" (24-hour format is standard).
- **Numbers:** Decimal separator is comma in Ukrainian ("3,5" not "3.5"), space as thousands separator ("1 000 000" not "1,000,000").
- **Currency:** Adapt symbol position. "$100" → "100 доларів" or "100 $" (after the number).
- **Quotation marks:** Ukrainian uses «лапки-ялинки» as primary, „лапки-лапи" as nested. Not "English-style quotes".
- **Dash usage:** Ukrainian uses em-dashes (—) freely, including in place of "is/are": *Київ — столиця України.*

---

## 2. Grammar Rules That Matter for Translation Quality

This section is not a complete grammar. It is the subset of Ukrainian grammar where AI translation most often fails.

### 2.1 Word Order (порядок слів)

Ukrainian has **free word order**. The grammatical role of a word is shown by its case ending, not its position. This means:

- The *most important new information* tends to go at the **end** of the sentence (the "rheme" position).
- The *topic / known information* tends to go at the **beginning** (the "theme" position).
- This is often the **opposite** of English.

**Example:**

> English: "Maria sent the document yesterday."
>
> If emphasizing *when*: *Документ Марія надіслала вчора.* (yesterday is at the end — new info)
>
> If emphasizing *what*: *Учора Марія надіслала документ.* (the document is the new info)
>
> If emphasizing *who*: *Учора документ надіслала Марія.* (Maria is the new info)

When translating, ask: **what's the new/important information?** Put that at the end. Don't blindly preserve subject-verb-object order.

### 2.2 The Six Cases — When Each One Triggers

Ukrainian has six cases (plus vocative). AI translators get cases wrong most often because they don't track the *semantic role* properly.

| Case | Українська | Primary uses |
|---|---|---|
| Nominative | називний | Subject of the sentence; "the company is..." |
| Genitive | родовий | Possession; negation ("there is no X" → *немає X-genitive*); after many prepositions (без, від, до, з, для); after numbers 2/3/4 (plural) and 5+ (genitive plural); partitive ("some of the water") |
| Dative | давальний | Indirect object ("to/for someone"); recipient of action; impersonal constructions ("мені треба", "вам подобається") |
| Accusative | знахідний | Direct object; destination after some prepositions (на, у); duration ("на тиждень") |
| Instrumental | орудний | "with/by means of"; means of transportation (їхати поїздом); profession ("вона працює лікарем"); after prepositions (з, перед, над, під, за) |
| Locative | місцевий | ONLY used with prepositions; location ("у Львові"); topic ("про роботу") |
| Vocative | кличний | Direct address ("Іване!", "пані Олено!", "друже!") — used in greetings and any direct address |

**Critical reminder:** The **vocative case is mandatory** in direct address in modern Ukrainian. It is NOT optional. Using nominative for direct address is a Russification.
- ❌ *Іван, прийди сюди.*
- ✅ *Іване, прийди сюди.*
- ❌ *Шановний клієнт!*
- ✅ *Шановний кліенте!* (or shop-talk: *Шановний клієнте!*)
- ❌ *Друг, як справи?*
- ✅ *Друже, як справи?*

### 2.3 Verb Aspect (вид дієслова) — THE Most Important Topic

Every Ukrainian verb exists in two aspects:

- **Imperfective (недоконаний вид)** — ongoing, repeated, habitual, or in-progress action. "I was doing X." "I do X regularly."
- **Perfective (доконаний вид)** — completed, one-time, result-focused action. "I did X (and finished)."

English doesn't grammaticalize this — Ukrainian does. AI translators routinely pick the wrong aspect, which makes sentences sound subtly off even when individual words are correct.

**Common verb aspect pairs:**

| Imperfective | Perfective | Meaning |
|---|---|---|
| писати | написати | to write |
| читати | прочитати | to read |
| робити | зробити | to do |
| казати | сказати | to say |
| давати | дати | to give |
| брати | взяти | to take |
| купувати | купити | to buy |
| продавати | продати | to sell |
| дзвонити | подзвонити | to call (phone) |
| надсилати | надіслати | to send |
| отримувати | отримати | to receive |
| оновлювати | оновити | to update |
| перевіряти | перевірити | to check |
| створювати | створити | to create |
| видаляти | видалити | to delete |
| зберігати | зберегти | to save |
| відкривати | відкрити | to open |
| закривати | закрити | to close |
| вирішувати | вирішити | to decide / to solve |
| починати | почати | to begin |
| закінчувати | закінчити | to finish |
| знаходити | знайти | to find |
| втрачати | втратити | to lose |
| розуміти | зрозуміти | to understand |

**Rules of thumb for choosing aspect:**

| Context | Aspect | Example |
|---|---|---|
| Single completed action with result | Perfective | *Я написав листа.* (I wrote the letter — done) |
| Repeated/habitual action | Imperfective | *Я пишу листи щотижня.* (I write letters weekly) |
| In-progress action | Imperfective | *Я зараз пишу листа.* (I'm writing the letter right now) |
| Instruction to do once | Perfective imperative | *Напишіть лист.* (Write the letter) |
| Instruction to do regularly | Imperfective imperative | *Пишіть листи щотижня.* (Write letters weekly) |
| Negative instruction (don't do this) | Imperfective | *Не натискайте цю кнопку.* (Don't press this button) — IMPORTANT: negative commands are nearly always imperfective in Ukrainian |
| Future single action | Perfective future | *Я перевірю.* (I'll check) |
| Future ongoing/repeated | Imperfective future (compound) | *Я буду перевіряти.* (I'll be checking) |
| Polite request | Often imperfective with "будь ласка" | *Заповнюйте форму, будь ласка.* (vs perfective: *Заповніть форму.*) |

### 2.4 Articles & Pronouns — Drop Them Aggressively

Ukrainian has **no articles** (no "the", no "a/an"). It also drops possessive pronouns and personal pronouns far more aggressively than English.

| English | ❌ Over-translated | ✅ Natural Ukrainian |
|---|---|---|
| Send me your report. | Надішліть мені ваш звіт. | Надішліть звіт. |
| I need to check my email. | Мені потрібно перевірити мою пошту. | Мені треба перевірити пошту. |
| He has his keys. | Він має свої ключі. | Він має ключі. |
| Show me your work. | Покажіть мені вашу роботу. | Покажіть роботу. |
| Take your things. | Заберіть ваші речі. | Заберіть речі. |
| She loves her job. | Вона любить свою роботу. | Вона любить роботу. |

The only time to keep the possessive pronoun is when ownership is genuinely ambiguous or contrastive (*"my car, not yours"* → *моя машина, а не твоя*).

### 2.5 The "Ти" vs "Ви" Decision

This is one of the most consequential choices in Ukrainian writing.

| Use | When |
|---|---|
| **Ви** (formal, capitalized in formal writing) | All business/professional content. All customer-facing content. Anyone you don't personally know. Anyone older than you (in personal contexts). Anyone in a position of authority. Legal documents. Marketing. Public communications. Default for any unknown audience. |
| **ти** (informal) | Personal correspondence between friends/family. Informal social media targeting young/casual audience. Children. Direct address from God in religious texts. Internal team chat *only* if everyone uses ти with each other. Creative writing (depends on character relationships). |

**Default to Ви unless you have a strong reason for ти.** When unsure, Ви.

**Capitalization rule for Ви:**
- In formal correspondence to one person: capitalize "Ви" / "Вас" / "Вам" / "Ваш" as a sign of respect.
- In marketing/general content addressed to a broad audience: lowercase "ви" is also common and acceptable.
- The verb takes plural form in both polite-singular and actual-plural cases — this is correct, not a mistake.

**Switching mid-text:** Don't. Once you've chosen Ви or ти, stay consistent within a single document or piece of communication.

### 2.6 Numbers and Counting — Major Gotcha

Numbers in Ukrainian govern different cases. AI gets this wrong constantly.

- **1** (and any number ending in 1, except 11) → noun in nominative singular: *21 день, 101 співробітник*
- **2, 3, 4** (and any number ending in 2/3/4, except 12/13/14) → noun in nominative plural: *3 дні, 22 співробітники*
- **5+** (and 11–19) → noun in genitive plural: *5 днів, 15 співробітників, 100 співробітників*

For decimals/fractions: governs genitive singular. *1,5 кілометра, 2,3 літра*

**Year expressions:** Years take genitive: *у 2026 році* (in 2026), *з 2020 по 2026 рік* (from 2020 to 2026).

### 2.7 Gender Agreement

Every noun has gender (masculine/feminine/neuter). Adjectives, pronouns, and past-tense verbs must agree. AI usually gets this right with common nouns but fails on:

- **Words borrowed from English** — pick a gender and stick with it. Most English borrowings ending in a consonant become masculine: *менеджер (m.), компанія (f.), додаток (m., "app"), сайт (m.)*
- **Profession nouns referring to women** — modern Ukrainian increasingly uses feminine forms (фемінітиви): *менеджерка, лікарка, програмістка, авторка, директорка*. Use these when:
  - The audience is Ukraine-based and progressive/modern
  - You know the person is a woman and prefers the feminine form
  - You're writing for media outlets that have adopted фемінітиви as house style
  
  Stick with masculine forms when:
  - Writing for diaspora audiences (фемінітиви are less established in diaspora Ukrainian)
  - Writing legal/formal documents where masculine has historically been the unmarked form
  - You don't know the recipient's preference and the context is formal
  
  When in doubt: ask, or default to whatever feels less marked for your audience.

### 2.8 Apostrophes (апостроф) — Use Correctly

Ukrainian uses the apostrophe **(')** to separate hard consonants from soft vowels in specific phonetic environments. AI sometimes drops these or uses the wrong character.

- ✅ *об'єкт, п'ять, м'який, в'їзд, ім'я, сім'я, інтер'єр, прем'єр*
- ❌ *обєкт, пять, мякий*

Use the typographic curly apostrophe (') or the straight ASCII apostrophe (') consistently. Avoid using the backtick (`) or the modifier letter apostrophe (ʼ).

---

## 3. Russification Traps — The Single Biggest Quality Problem

AI Ukrainian frequently contains Russian-influenced vocabulary, syntax, and idioms because the training data conflates Russian and Ukrainian. This is called "суржик" in its spoken form, but in written form it just reads as bad Ukrainian. **Avoid these without exception.**

### 3.1 Russified Vocabulary — Replace These

| ❌ Russification | ✅ Proper Ukrainian | English |
|---|---|---|
| у відповідності з | відповідно до | in accordance with |
| на протязі | протягом | during, throughout |
| приймати участь | брати участь | to take part |
| при допомозі | за допомогою | with the help of |
| у залежності від | залежно від | depending on |
| у випадку | у разі | in case of |
| у даний момент | наразі / зараз | at this moment |
| у цілому | загалом | overall, in general |
| у якості | як (or no preposition) | as / in the role of |
| на сьогоднішній день | сьогодні / на сьогодні | today, at present |
| дякуючи цьому | завдяки цьому | thanks to this |
| вірний (about an answer) | правильний | correct |
| слідуючий | наступний | next, following |
| вірогідно | імовірно / ймовірно | probably |
| любий (meaning "any") | будь-який | any |
| багаточисленний | численний | numerous |
| малочисленний | нечисленний | few in number |
| міроприємство | захід | event, measure |
| відмінити | скасувати | to cancel |
| обумовлений | зумовлений | conditioned by, caused by |
| ясно | зрозуміло | (it's) clear, understood |
| строк | термін | term, deadline |
| охрана | охорона | security, protection |
| опасний | небезпечний | dangerous |
| остановка | зупинка | stop (bus stop, etc.) |
| появитися | з'явитися | to appear |
| виключити (turn off) | вимкнути | to turn off |
| включити (turn on) | увімкнути | to turn on |
| предоставити | надати | to provide |
| обновити | оновити | to update |
| повторно | повторно (OK) but consider "ще раз" | repeatedly, again |
| розпорядження | розпорядження (OK but consider "наказ" or "доручення") | instruction, order |
| приймати рішення | ухвалювати рішення | to make a decision |
| приймати закон | ухвалювати закон | to pass a law |
| розпрощатися | попрощатися | to say goodbye |
| любити (in greetings) | вітати | to greet |
| багаточисленні | численні | numerous |
| у наступному тижні | наступного тижня | next week |
| у цьому році | цього року | this year |
| у минулому місяці | минулого місяця | last month |

### 3.2 Russified Syntax — Patterns to Avoid

**Pattern 1: "по + dative" overuse**
Russian uses "по" extensively where Ukrainian uses other prepositions or no preposition at all.
- ❌ *звіт по продажах* → ✅ *звіт про продажі / щодо продажів*
- ❌ *графік по днях* → ✅ *графік за днями / денний графік*
- ❌ *робота по проєкту* → ✅ *робота над проєктом*
- ❌ *іспит по математиці* → ✅ *іспит з математики*
- ❌ *по телефону* → ✅ *телефоном* (acceptable both ways, but instrumental is preferred)

**Pattern 2: Active participles in -чий/-щий**
Ukrainian historically avoids active participles ending in -чий/-щий that Russian uses freely. Restructure with a relative clause.
- ❌ *людина, працююча в офісі* → ✅ *людина, яка працює в офісі*
- ❌ *компанія, надаюча послуги* → ✅ *компанія, яка надає послуги*
- ❌ *проєкт, розвиваючий галузь* → ✅ *проєкт, що розвиває галузь*

**Pattern 3: "являється" instead of "є" or em-dash**
- ❌ *Він являється директором компанії.*
- ✅ *Він є директором компанії.*
- ✅ *Він — директор компанії.* (most natural)

**Pattern 4: "являє собою" overuse**
- ❌ *Це являє собою серйозну проблему.*
- ✅ *Це серйозна проблема.* / *Це становить серйозну проблему.*

**Pattern 5: "у/в + locative" for time periods**
- ❌ *у наступному тижні* → ✅ *наступного тижня*
- ❌ *у цьому році* → ✅ *цього року*
- ❌ *у грудні місяці* → ✅ *у грудні* (drop "місяці")

**Pattern 6: Passive voice overuse**
Ukrainian prefers active or impersonal constructions where Russian and English use passive.
- ❌ *Лист був надісланий вчора.* (literally translated passive)
- ✅ *Лист надіслали вчора.* / *Лист надіслано вчора.* (impersonal)

### 3.3 Russified Business Jargon — The "Soviet" Sound

| ❌ Russified / Soviet-era | ✅ Modern Ukrainian | Meaning |
|---|---|---|
| даний документ | цей документ | this document |
| вищезазначений | вищезгаданий / згаданий вище | aforementioned |
| доводжу до Вашого відома | повідомляю Вам / інформую Вас | I inform you |
| у зв'язку з вищевикладеним | у зв'язку з цим | in connection with the above |
| надати інформацію (OK) but avoid "предоставити" | надати | to provide |
| продовжуючий | який продовжує | continuing |
| прийняти рішення | ухвалити рішення | to make a decision |
| привести до... | призвести до... | to lead to (negative result) |
| у тому числі | зокрема / у тому числі (both OK) | including |
| на даний момент | наразі / зараз / на цей момент | at this moment |
| даний продукт | цей продукт | this product |
| у наявності | в наявності | available |

### 3.4 The "Калька" Test

After writing any sentence, ask: **"Could this have been mechanically translated from English or Russian word-for-word?"** If yes, rewrite.

---

## 4. Register & Tone Rules by Content Type

The same information should be phrased differently depending on the context. This section codifies the rules.

### 4.1 Business / Professional (B2B, internal comms, sales)

**Rules:**
- Use formal **Ви**, capitalized.
- Get to the point fast. Skip "I hope you're well" openers — Ukrainian business email opens with the actual content.
- Active voice over passive.
- Modern, not Soviet-era. Avoid "доводжу до Вашого відома" — say "повідомляю".
- Bullet points and clear structure for emails over ~3 sentences.
- Sign-off: *З повагою, [Name]* is standard.

**Example email:**
> Шановний пане Петре,
>
> Надсилаю комерційну пропозицію щодо співпраці у Q2 2026. Основні умови — у вкладенні.
>
> Готовий обговорити деталі на дзвінку наступного тижня. Який день і час Вам зручні?
>
> З повагою,
> Олена Коваленко

### 4.2 Product / SaaS / UI Copy

**Rules:**
- Use formal **Ви** (or sometimes ти for very casual products targeting Gen Z — but Ви is the safe default).
- Short. Buttons and menu items should be 1–3 words, ideally a verb or noun phrase.
- Imperative for actions: *Зберегти, Скасувати, Видалити, Надіслати*.
- Noun phrases for sections/categories: *Налаштування, Профіль, Підписка*.
- Error messages: clear, blameless, with a path forward.
- No marketing fluff inside the product UI.

**Examples:**

| English UI text | ✅ Ukrainian |
|---|---|
| Save changes | Зберегти зміни |
| Delete account | Видалити акаунт |
| Sign up | Зареєструватися |
| Log in | Увійти |
| Forgot password? | Забули пароль? |
| Send | Надіслати |
| Cancel | Скасувати |
| Settings | Налаштування |
| Profile | Профіль |
| Welcome back! | З поверненням! |
| Something went wrong. Please try again. | Сталася помилка. Спробуйте ще раз. |
| Your changes have been saved. | Зміни збережено. |
| No results found | Нічого не знайдено |
| Loading... | Завантаження... |

### 4.3 Marketing & Landing Page Copy

**Rules:**
- Use **Ви** (lowercase often acceptable for broad-audience marketing) or ти for youth/lifestyle brands.
- Punchy. Headlines that are 6 words in English shouldn't bloat to 12 in Ukrainian.
- Avoid corporate-speak: no *оптимізація бізнес-процесів, синергія, рішення нового покоління*.
- Use specific numbers/outcomes over generic benefits.
- Active voice. Verbs over nouns. *"Заощадить 5 годин на тиждень"* beats *"Підвищення ефективності робочого часу"*.

**Example:**
> English: "Stop wasting time on manual reports. Our platform automates your entire workflow."
>
> ✅ "Менше ручних звітів — більше часу на справжню роботу. Наша платформа автоматизує все за вас."

### 4.4 Casual / Personal Communication

**Rules:**
- Use **ти** if you actually use ти with this person, otherwise Ви.
- Looser sentence structure, contractions and elisions OK (*що ж, ну, та*, etc.).
- Emoji and interjections fine in context (texts, DMs, casual posts).
- Common colloquialisms acceptable: *клас, супер, круто, файно* (regional — Western Ukraine).
- Avoid sounding like a press release.

**Example text message:**
> English: "Hey, are you free tomorrow at 7? Wanted to grab coffee."
>
> ✅ *"Привіт! Завтра о 7-й вільна? Хотіла кави попити разом."*

### 4.5 Social Media

**Rules:**
- **Ти** for personal accounts and youth-oriented brands; **Ви** for B2B and professional accounts.
- Punchy first line — Ukrainian social copy needs the same hook discipline as English.
- Hashtags: use Ukrainian (#маркетинг) or English (#marketing) based on audience. Don't transliterate awkwardly.
- Emoji use is universal — but don't substitute words with emoji in formal posts.
- Calls to action: imperative, perfective, short. *Підписуйся. Зберігай. Поширюй.*

**Example LinkedIn post opener:**
> English: "I just spent 6 months learning [topic]. Here are 5 things I wish I knew on day one:"
>
> ✅ *"6 місяців я розбирався в [темі]. Ось 5 речей, які треба знати з самого початку:"*

### 4.6 Creative Writing (fiction, narrative, essays)

**Rules:**
- Register is character/voice-driven, not rule-driven. Match the speaker.
- Modern Ukrainian fiction tends toward shorter sentences than English, with heavier use of em-dashes for rhythm and dialogue.
- Dialogue uses em-dashes for speech, not quotation marks:
  ```
  — Куди ти йдеш? — запитала вона.
  — Не знаю, — відповів він.
  ```
- Ukrainian literary tradition allows long flowing sentences too — pick a rhythm and commit.
- Avoid Russian-influenced literary clichés (e.g., overuse of *уже* / *уж*).
- Idioms, proverbs, regional flavor: use generously where appropriate.

### 4.7 Legal / Formal Documents (contracts, agreements, official correspondence)

**Rules:**
- Use formal **Ви** with capitalization in correspondence; third-person constructions in contracts.
- Define terms at first use: *"ТОВ «Назва» (далі — «Виконавець»)..."*
- Numbered sections (1.1, 1.2, 1.2.1).
- Use modern Ukrainian legal terminology, not Soviet-era constructs.
- Avoid both English calques AND Russified legalese.
- "У разі" not "у випадку". "Відповідно до" not "у відповідності з". "Ухвалити рішення" not "прийняти рішення".
- Modal verbs: *має право, зобов'язаний, повинен, має*.

**Standard formal phrases:**
| English | ✅ Ukrainian |
|---|---|
| The Parties agree that... | Сторони домовилися, що... |
| Subject to the terms of... | Згідно з умовами... / Відповідно до умов... |
| In witness whereof | На посвідчення чого |
| This Agreement is governed by... | Цей Договір регулюється... |
| Either party may terminate... | Будь-яка зі Сторін може розірвати... |
| Force majeure | Форс-мажор / Обставини непереборної сили |
| Confidentiality | Конфіденційність |
| Hereinafter referred to as | Далі — |

---

## 5. Modern Standard vs Diaspora Ukrainian — When to Use Each

These are two related but distinct varieties of written Ukrainian. Picking the wrong one for your audience produces text that feels slightly off even when grammatically correct.

### 5.1 Modern Standard Ukrainian (Kyiv-based, post-2019 reforms)

**Use when writing for:**
- Audiences in Ukraine
- Ukrainian government/legal contexts
- International publications targeting Ukrainian readers globally
- Media outlets, academic content, formal publications
- Most B2B and professional content when audience location is unspecified

**Characteristics:**
- Follows the 2019 Ukrainian orthography reform (Правопис 2019).
- Uses modern Ukrainian neologisms over English borrowings where good Ukrainian equivalents exist: *вподобайка* over "лайк", *світлина* over "фото" (though "фото" is more common).
- Embraces feminine profession forms (фемінітиви): *авторка, директорка, програмістка*.
- Avoids both Russian and English calques.
- Uses native Ukrainian vocabulary where possible: *летовище* (airport) is making a comeback alongside *аеропорт*.

### 5.2 Diaspora Ukrainian (US/Canada/UK Ukrainian communities)

**Use when writing for:**
- Ukrainian-speaking immigrants in English-speaking countries
- US/Canadian Ukrainian community organizations, churches, businesses
- Content where the audience uses English daily and naturally code-switches
- Trucking, real estate, small business contexts in the diaspora

**Characteristics:**
- More tolerant of English borrowings and anglicisms: *аплікація* (application), *кеш* (cash — though "готівка" is also used), *тікет* (ticket — though sometimes confused with native uses).
- Older orthography influences (some diaspora communities preserved pre-Soviet spellings).
- May retain regional features from Western Ukraine (since many diaspora communities originated there): *файно, ґазда*.
- Less prescriptive about фемінітиви — masculine forms often default.
- Code-switching with English is normal in casual contexts.

### 5.3 Practical Guidance: When You Don't Know

If you don't know the audience:
- **Lean modern standard** — it works for diaspora readers (they understand it perfectly), but modern standard readers in Ukraine may find diaspora-flavored Ukrainian slightly dated or anglicized.
- Use modern Правопис 2019 rules (e.g., -ій in foreign words: *проєкт* not *проект*).
- Avoid the most aggressive diaspora anglicisms unless you know the audience uses them.

### 5.4 Key Spelling Differences (Правопис 2019)

The 2019 orthography reform brought back some pre-Soviet spelling features. These are now standard for modern Ukrainian, but you may see older forms in older texts.

| Pre-2019 / older form | Post-2019 / modern form | Notes |
|---|---|---|
| проект | проєкт | Foreign words with "je" sound |
| фейр-плей | феєр-плей / фейр-плей | Some words have variant forms |
| Чикаго | Чикаго / Чикаго (both OK) | |
| Маріо | Маріо / Маріо | |
| священик | священник | Doubled consonants |
| ірій | ирій | Initial и in some words |
| блогер | блогер / блоґер | Optional ґ in foreign words |

The most-cited example: **проєкт** (not "проект") is the modern standard form for "project". This is a tell — if AI writes "проект", it's defaulting to pre-reform/Russian-influenced spelling.

---

## 6. Common Anglicisms — When OK, When Not

Diaspora and tech-savvy Ukrainian audiences tolerate certain anglicisms freely. Others always sound bad.

### 6.1 Anglicisms That Are Established and Acceptable

These are part of modern Ukrainian usage even in Ukraine. Use freely.

| Anglicism | Notes |
|---|---|
| менеджер | universal |
| маркетинг | universal |
| дизайн / дизайнер | universal |
| бренд / брендинг | universal |
| стартап | universal in tech |
| контент | universal |
| тренд | universal |
| офіс | universal |
| емейл / імейл | informal; "електронна пошта" formal |
| фідбек | acceptable in business |
| дедлайн | universal in business |
| сторіс | (Instagram stories) universal |
| подкаст | universal |
| блог / блогер | universal |
| сайт / вебсайт | "сайт" universal |
| лайк | universal in social media; *вподобайка* is the cute Ukrainianism |
| хедер | universal in web/dev/product; "шапка сайту" alternate |
| футер | universal in web/dev/product; "підвал сайту" alternate |

### 6.2 Anglicisms That Are NOT Acceptable

These add nothing and replace perfectly good Ukrainian words.

| ❌ Don't use | ✅ Use instead | English |
|---|---|---|
| контрол | контроль | control |
| компанія | (OK, but don't transliterate to "ка́мпані") | company |
| кеш | готівка (formal) / кеш (informal OK) | cash |
| респект | повага | respect |
| хобі (OK) | захоплення | hobby (anglicism OK) |
| лідер | (OK) / провідник / керівник | leader |
| тренди (OK) but watch context | тенденції | trends (more formal) |
| челендж | виклик | challenge |
| мітинг (the meeting kind) | зустріч / нарада | meeting (note: "мітинг" = political rally in UA!) |

⚠️ **Important false friend:** "Мітинг" in Ukrainian means a **political rally or demonstration**, NOT a business meeting. Use **зустріч** or **нарада** for a meeting. Calling a Zoom call a "мітинг" is a common AI translation error.

---

## 7. IT / SaaS / Product Glossary

Locked terminology for tech/product content. Same English term → same Ukrainian term every time.

### 7.1 Authentication & Account

| English | Ukrainian | Notes |
|---|---|---|
| Sign up / Register | Зареєструватися | |
| Sign in / Log in | Увійти | |
| Sign out / Log out | Вийти | |
| Account | Акаунт / обліковий запис | "Акаунт" informal; "обліковий запис" formal/government |
| Username | Ім'я користувача / нікнейм | |
| Password | Пароль | |
| Forgot password | Забули пароль | |
| Reset password | Скинути пароль | |
| Two-factor authentication (2FA) | Двофакторна автентифікація | |
| Verification code | Код підтвердження | |
| Email verification | Підтвердження електронної пошти | |
| Profile | Профіль | |
| Settings | Налаштування | |
| Preferences | Параметри / уподобання | |

### 7.2 Core Product Actions

| English | Ukrainian | Notes |
|---|---|---|
| Create | Створити | |
| Edit | Редагувати / змінити | |
| Update | Оновити | NOT "обновити" |
| Delete | Видалити | |
| Save | Зберегти | |
| Cancel | Скасувати | NOT "відмінити" |
| Submit | Надіслати / подати | |
| Send | Надіслати | |
| Receive | Отримати | |
| Share | Поділитися | |
| Download | Завантажити | |
| Upload | Завантажити (контекст вирішує) / вивантажити | Both use "завантажити" — context disambiguates |
| Copy | Скопіювати | |
| Paste | Вставити | |
| Cut | Вирізати | |
| Undo | Скасувати дію | |
| Redo | Повторити дію | |
| Search | Пошук (noun) / шукати (verb) | |
| Filter | Фільтрувати (verb) / фільтр (noun) | |
| Sort | Сортувати | |
| Refresh | Оновити | |
| Reload | Перезавантажити | |

### 7.3 UI Elements

| English | Ukrainian | Notes |
|---|---|---|
| Button | Кнопка | |
| Menu | Меню | |
| Dropdown | Випадаюче меню / випадний список | |
| Modal / Dialog | Діалогове вікно | |
| Tooltip | Підказка | |
| Notification | Сповіщення | NOT "нотифікація" |
| Banner | Банер | |
| Tab | Вкладка | |
| Panel | Панель | |
| Sidebar | Бічна панель | |
| Header | Хедер | **Default in dev/product/web contexts** — what people actually say. "Шапка" OK in some contexts; "заголовок" only for page heading (the H1), not the site header |
| Footer | Футер | **Default in dev/product/web contexts** — what people actually say. "Підвал" acceptable; "нижній колонтитул" only in Word/print contexts |
| Toolbar | Панель інструментів | |
| Slider | Повзунок (UI) / слайдер (carousel) | |
| Checkbox | Прапорець | |
| Radio button | Перемикач | |
| Dropdown list | Випадний список | |
| Loading spinner | Індикатор завантаження | |
| Progress bar | Індикатор прогресу / смуга прогресу | |

### 7.4 Subscriptions & Billing

| English | Ukrainian | Notes |
|---|---|---|
| Subscription | Підписка | |
| Plan / Tier | Тариф / план | |
| Free plan | Безкоштовний тариф | |
| Free trial | Безкоштовний пробний період | |
| Upgrade | Покращити тариф / перейти на вищий тариф | |
| Downgrade | Знизити тариф | |
| Cancel subscription | Скасувати підписку | |
| Renew | Поновити | |
| Auto-renewal | Автоматичне поновлення | |
| Billing | Оплата / білінг | |
| Invoice | Рахунок-фактура / інвойс | "Інвойс" informal |
| Payment method | Спосіб оплати | |
| Credit card | Кредитна картка | |
| Refund | Повернення коштів | |

### 7.5 Errors & States

| English | Ukrainian | Notes |
|---|---|---|
| Error | Помилка | |
| Warning | Попередження | |
| Success | Успіх / готово | |
| Loading | Завантаження | |
| Please wait | Зачекайте, будь ласка | |
| Not found | Не знайдено | |
| Page not found (404) | Сторінку не знайдено | |
| Server error | Помилка сервера | |
| Network error | Помилка мережі | |
| Try again | Спробуйте ще раз | |
| Something went wrong | Сталася помилка | |
| Invalid email | Неправильна електронна пошта | |
| Required field | Обов'язкове поле | |
| Optional | Необов'язково | |

### 7.6 Tech / Development

| English | Ukrainian | Notes |
|---|---|---|
| Software | Програмне забезпечення / ПЗ / софт | |
| App / Application | Додаток / застосунок | "Застосунок" is the modernist preference |
| Hardware | Апаратне забезпечення / залізо (slang) | |
| Cloud | Хмара | |
| Server | Сервер | |
| Database | База даних | |
| API | API | Keep Latin |
| Endpoint | Ендпойнт | |
| Bug | Баг / помилка | |
| Feature | Функція / фіча | "Фіча" informal/dev-slang |
| Release | Реліз / випуск | |
| Beta | Бета (-версія) | |
| Update (noun) | Оновлення | |
| Patch | Патч | |
| Open source | Відкритий код | |
| Code | Код | |
| Bug fix | Виправлення помилки | |
| Pull request | Pull request / PR | Usually Latin in dev teams |
| Merge | Злити (verb) / мерж (noun) | "Мерж" dev-slang |
| Deploy | Розгорнути / задеплоїти (slang) | |
| Repository | Репозиторій | |
| Branch | Гілка | |
| Commit | Коміт | |

### 7.7 Data & Analytics

| English | Ukrainian | Notes |
|---|---|---|
| Data | Дані | |
| Analytics | Аналітика | |
| Dashboard | Дашборд / панель приладів | "Дашборд" universal |
| Report | Звіт | |
| Metric | Метрика | |
| Conversion | Конверсія | |
| Engagement | Залученість | |
| Retention | Утримання | |
| Funnel | Воронка | |
| KPI | KPI / ключовий показник | |
| ROI | ROI / окупність | |

### 7.8 Communication / Collaboration

| English | Ukrainian | Notes |
|---|---|---|
| Message | Повідомлення | |
| Chat | Чат | |
| Comment | Коментар | |
| Reply | Відповідь | |
| Reaction | Реакція | |
| Mention | Згадка | |
| Tag | Тег | |
| Channel | Канал | |
| Workspace | Робочий простір | |
| Team | Команда | |
| Project | Проєкт | NOT "проект" (post-2019 spelling) |
| Task | Завдання | |
| Deadline | Дедлайн / термін | |
| Reminder | Нагадування | |
| Schedule | Розклад / графік | |
| Calendar | Календар | |
| Meeting | Зустріч / нарада | NOT "мітинг" (= political rally!) |
| Call | Дзвінок / виклик | |
| Video call | Відеодзвінок | |

---

## 8. Side-by-Side Examples

Study these patterns. They show the difference between bad translation and good localization across different content types.

### Example 1: Welcome Email (SaaS Onboarding)

**English source:**
> "Hi Maria, welcome to Acme! We're thrilled to have you on board. To get started, please verify your email address by clicking the button below. If you have any questions, just reach out — we're here to help!"

**❌ Bad (calque translation):**
> "Привіт Марія, ласкаво просимо до Acme! Ми в захваті мати вас на борту. Щоб розпочати, будь ласка, підтвердіть вашу електронну адресу, натиснувши кнопку нижче. Якщо у вас є будь-які питання, просто дотягніться — ми тут, щоб допомогти!"

**Problems:** Nominative "Марія" instead of vocative; "мати вас на борту" is a literal calque; "будь-які питання" + "просто дотягніться" — translated word-for-word; "ми тут, щоб допомогти" preserves English structure.

**✅ Good (localization):**
> "Маріє, вітаємо в Acme! Щоб почати, підтвердіть електронну пошту — кнопка нижче. Виникнуть питання — пишіть, завжди раді допомогти."

**Why it works:** Vocative case "Маріє"; drops "ваш" and "будь-які"; uses em-dash for rhythm; converts "if you have questions, reach out" into the more natural Ukrainian conditional "виникнуть питання — пишіть".

---

### Example 2: LinkedIn Post Headline

**English source:**
> "I just spent 6 months learning growth marketing. Here are 5 things I wish I knew on day one."

**❌ Bad:**
> "Я тільки що провів 6 місяців, вивчаючи маркетинг росту. Ось 5 речей, які я хотів би знати в перший день."

**Problems:** "Я тільки що провів" is awkward; "маркетинг росту" is a calque (real term: *growth-маркетинг* or "маркетинг зростання"); "хотів би знати в перший день" preserves English structure rigidly.

**✅ Good:**
> "6 місяців я розбирався в growth-маркетингу. Ось 5 речей, які варто було знати з самого початку."

**Why it works:** Front-loads the time period (rheme/topic switch — "6 months" is the hook). Uses "розбирався в" which is more natural than "вивчав". Keeps "growth" in English as it's an established term in Ukrainian marketing circles. "Варто було знати з самого початку" reads as something a Ukrainian-speaker would actually write.

---

### Example 3: Error Message

**English source:**
> "Oops! Something went wrong. We couldn't save your changes. Please try again or contact support if the problem persists."

**❌ Bad:**
> "Упс! Щось пішло не так. Ми не змогли зберегти ваші зміни. Будь ласка, спробуйте ще раз або зв'яжіться з підтримкою, якщо проблема продовжиться."

**Problems:** "Ваші" unnecessary; "Ми не змогли" is awkwardly personalized; "проблема продовжиться" is calque ("if the problem persists" → "якщо проблема продовжиться" is not how Ukrainian expresses this).

**✅ Good:**
> "Упс! Не вдалося зберегти зміни. Спробуйте ще раз. Якщо помилка повториться — зверніться до підтримки."

**Why it works:** Impersonal "Не вдалося" is much more natural for system errors than personalizing it with "ми"; drops "ваші"; "якщо помилка повториться" is the natural Ukrainian way to express "if the problem persists".

---

### Example 4: Casual Text Message

**English source:**
> "Hey! Are you free tonight? Was thinking of grabbing dinner if you're around."

**❌ Bad:**
> "Гей! Ти вільний сьогодні ввечері? Думав про те, щоб схопити вечерю, якщо ти поблизу."

**Problems:** "Гей" sounds aggressive in Ukrainian (it's literally an exclamation, not a greeting like English "hey"); "схопити вечерю" is a calque of "grab dinner"; "якщо ти поблизу" is overly literal.

**✅ Good:**
> "Привіт! Маєш час сьогодні ввечері? Може, повечеряємо разом, якщо вільний?"

**Why it works:** "Привіт" is the natural casual greeting (or "Хай!" for very young speakers); "Маєш час" is the natural Ukrainian phrasing for "are you free"; "повечеряємо разом" replaces the awkward "схопити вечерю" with normal Ukrainian.

---

### Example 5: Marketing Headline

**English source:**
> "Stop wasting time on spreadsheets. Our platform automates everything so you can focus on what matters."

**❌ Bad:**
> "Перестаньте витрачати час на таблиці. Наша платформа автоматизує все, щоб ви могли зосередитися на тому, що має значення."

**Problems:** "Перестаньте витрачати" is too literal; "наша платформа" overuses possessive; "на тому, що має значення" is a long calque.

**✅ Good:**
> "Менше таблиць — більше справжньої роботи. Платформа автоматизує рутину за вас."

**Why it works:** Punchy contrast structure ("менше X — більше Y") is a Ukrainian marketing staple; drops "наша" (clear from context); "рутину" is more specific and concrete than "все"; "за вас" frames the benefit naturally.

---

### Example 6: Formal Legal Phrase

**English source:**
> "The Service Provider shall deliver the services in accordance with the terms set forth in this Agreement."

**❌ Bad (Russified):**
> "Постачальник Послуг повинен надавати послуги у відповідності з умовами, викладеними в даному Договорі."

**Problems:** "У відповідності з" is Russification (correct: "відповідно до"); "даному Договорі" is Soviet-era jargon (correct: "цьому Договорі").

**✅ Good:**
> "Виконавець надає послуги відповідно до умов цього Договору."

**Why it works:** "Виконавець" is a more modern legal term for service provider; drops "повинен" because the indicative reads more naturally in Ukrainian contract language; "відповідно до" is correct (not "у відповідності з"); "цього" not "даного".

---

### Example 7: Creative Writing — Dialogue

**English source:**
> "She looked at him for a long time. 'You really don't get it, do you?' she said. He shrugged. 'I guess I don't.'"

**❌ Bad:**
> "Вона дивилась на нього довгий час. 'Ти дійсно не розумієш, чи не так?' вона сказала. Він знизав плечима. 'Думаю, що ні.'"

**Problems:** "Дивилась на нього довгий час" is a calque; "чи не так?" preserves the English question tag awkwardly; quotation marks are wrong for Ukrainian dialogue; "Думаю, що ні" is too literal.

**✅ Good:**
> "Вона довго дивилася на нього.
> — Ти й справді не розумієш? — нарешті промовила.
> Він знизав плечима.
> — Та, мабуть, ні."

**Why it works:** Em-dash dialogue formatting (Ukrainian standard); "довго дивилася" sounds natural; the question loses the awkward tag and gains "й справді"; "Та, мабуть, ні" is how someone actually says "I guess I don't" in Ukrainian.

---

## 9. Quick Lookup: Common Phrases

### 9.1 Greetings & Farewells

| English | Formal | Casual |
|---|---|---|
| Hello | Доброго дня | Привіт |
| Good morning | Доброго ранку | Доброго ранку |
| Good evening | Доброго вечора | Доброго вечора |
| Goodbye | До побачення | Бувай / Па |
| See you later | До зустрічі | До зустрічі / До скорого |
| How are you? | Як справи? / Як Ваші справи? | Як справи? / Як ти? |
| Nice to meet you | Приємно познайомитися | Приємно познайомитися |
| Welcome | Вітаємо / Ласкаво просимо | Вітаю / Заходь |

### 9.2 Politeness & Social

| English | Ukrainian |
|---|---|
| Please | Будь ласка |
| Thank you | Дякую |
| Thank you very much | Щиро дякую / Дуже дякую |
| You're welcome | Будь ласка / Прошу / Нема за що |
| I'm sorry | Вибачте / Перепрошую |
| Excuse me | Перепрошую / Вибачте |
| No problem | Без проблем |
| It's okay | Все гаразд / Все нормально |
| Congratulations | Вітаю (з + instr.) |
| Good luck | Успіхів / Хай щастить |

### 9.3 Business Email Building Blocks

| English | Ukrainian |
|---|---|
| Dear Mr./Mrs. [Name] | Шановний пане [Name] / Шановна пані [Name] |
| I hope this email finds you well | (DROP IT — Ukrainian doesn't open with small talk) |
| I'm writing to... | Пишу Вам з приводу... / Звертаюся щодо... |
| Please find attached | У вкладенні — / Надсилаю у вкладенні |
| Looking forward to hearing from you | Чекаю Вашої відповіді |
| Best regards | З повагою |
| Sincerely | З повагою / Щиро Ваш(а) |
| Thank you for your time | Дякую за приділений час |
| If you have any questions | Якщо виникнуть запитання |

---

## 10. Pre-Output Checklist (Run Before Every Response)

Before outputting any Ukrainian text, mentally verify each of the following. If any check fails, rewrite.

**Grammar checks:**
1. ☐ Word order: is the new/important information at the end (rheme)?
2. ☐ Cases: is every noun/pronoun in the correct case for its semantic role?
3. ☐ Verb aspect: did I pick the right aspect for each verb? (Completed vs ongoing vs habitual)
4. ☐ Vocative: am I addressing someone directly? If so, vocative case used?
5. ☐ Gender agreement: do adjectives, past-tense verbs, and pronouns match noun gender?
6. ☐ Numbers: is the noun in the right case after each number (1 / 2–4 / 5+)?
7. ☐ Apostrophes: present where needed (об'єкт, п'ять, ім'я)?

**Style checks:**
8. ☐ Did I drop unnecessary "ваш/мій/свій" possessives?
9. ☐ Did I drop unnecessary personal pronouns?
10. ☐ Did I use the right Ви/ти for this context?

**Russification checks:**
11. ☐ Any "по + dative" that should be "про/щодо/з/за/над"?
12. ☐ Any "являється" — replace with "є" or em-dash?
13. ☐ Any active participles in -чий/-щий — restructure with relative clause?
14. ☐ Any words from the Section 3.1 forbidden list? Replace.
15. ☐ Any Soviet-era business jargon (Section 3.3)? Replace.
16. ☐ Did I use "проєкт" (post-2019) not "проект" (pre-reform)?
17. ☐ "Скасувати" not "відмінити"? "Оновити" not "обновити"?

**False friends:**
18. ☐ Did I avoid "мітинг" for a business meeting? (Use "зустріч/нарада".)

**Convention checks:**
19. ☐ Date format appropriate for audience (DD.MM.YYYY for standard, MM/DD/YYYY for US diaspora)?
20. ☐ Decimal/thousands separators correct (comma decimal, space thousands)?
21. ☐ 24-hour time format unless audience uses US conventions?
22. ☐ Ukrainian quotation marks «...» where appropriate?

**Tone checks:**
23. ☐ Does the register match the content type?
24. ☐ Is it as concise as it can be without losing meaning?
25. ☐ Does it pass the **Native Speaker Test**: would a native Ukrainian-speaker write it this way without seeing the English?

---

## 11. The 10 Commandments of Ukrainian Localization

A quick reference card for the absolute essentials.

1. **Localize, don't translate.** Rewrite for Ukrainian flow.
2. **Drop articles and unnecessary possessives.** Ukrainian uses far fewer than English.
3. **Use vocative case for direct address.** Always. *Іване*, not *Іван*.
4. **Pick the right verb aspect.** Perfective for completed actions, imperfective for ongoing/habitual. Negative imperatives are imperfective.
5. **Default to formal Ви.** Capitalize in formal correspondence to one person.
6. **Match register to content type.** Business ≠ casual ≠ legal ≠ marketing.
7. **Avoid Russifications.** "Протягом" not "на протязі". "Відповідно до" not "у відповідності з". "Брати участь" not "приймати участь". "Є" not "являється". "Скасувати" not "відмінити".
8. **Avoid active participles in -чий/-щий.** Use relative clauses with "який/що".
9. **Use Правопис 2019.** "Проєкт" not "проект". Bring back the apostrophes and ґ where they belong.
10. **Watch false friends.** "Мітинг" = political rally, not business meeting. Use "зустріч".

---

## 12. How to Use This Document in a Claude Project

**Setup:**
1. Add this file to the Project Knowledge of every Claude Project that performs Ukrainian translation or content generation.
2. In the Project's system prompt, instruct Claude to consult it before producing Ukrainian output.

**Suggested project-level system prompt:**

```
You are a professional Ukrainian localizer. You localize English content
into natural Ukrainian — you never translate word-for-word.

Before producing Ukrainian output:
1. Determine the content type (business / product UI / marketing /
   casual / social / creative / legal).
2. Apply the corresponding tone rules from Section 4 of the reference.
3. Determine target audience flavor (modern standard vs diaspora).
   Default to modern standard if unspecified.
4. Use the locked glossary from Section 7 for tech/SaaS terms.
5. Avoid Russifications listed in Section 3.
6. Run the Section 10 checklist mentally before each output.

Default to formal Ви unless context calls for ти. Use Правопис 2019
spelling. Adapt date/time/number conventions to the audience.

Output only the Ukrainian text. No explanations unless asked.
```

**Iteration workflow:**
1. When you spot a bad translation, note what was wrong.
2. Update the relevant section of this document (Section 3 for new Russifications, Section 7 for new glossary terms, Section 8 for new side-by-side examples).
3. Re-upload to your Projects.
4. Quality compounds over time. Real-world bad examples teach the AI faster than abstract rules.

**Customizing for your domain:**
This is a general-purpose reference. For domain-specific work (legal, medical, trucking, finance, gaming, etc.), create a companion `.md` with your domain glossary and any domain-specific tone rules — load both into the Project together.

---

## 13. Version History

| Version | Date | Changes |
|---|---|---|
| 1.0 | 2026-05 | Initial release. General-purpose Ukrainian localization reference covering modern standard and diaspora flavors. Content types: business, product/SaaS, marketing, casual, social, creative, legal. Includes IT/SaaS glossary, Russification anti-patterns, side-by-side examples, and pre-output checklist. |
| 1.1 | 2026-05 | **Native-speaker correction:** Header/Footer terminology updated. **Хедер** and **футер** are now the primary terms for web/dev/product contexts (what Ukrainian-speakers actually say). "Шапка/підвал" kept as alternates; "заголовок/нижній колонтитул" reserved for specific contexts (page H1 and Word/print, respectively). Also added хедер and футер to the established/acceptable anglicisms list in Section 6.1. |

**Maintainer's note:** This is a living document. The more real-world bad-translation examples you fix and document here, the better the AI gets. Treat it as your team's institutional memory for Ukrainian quality.
