# Ukrainian Localization Reference

**Version:** 1.1
**Purpose:** This document is the canonical reference for any AI system performing English-to-Ukrainian translation for FleetCtrl and related trucking compliance businesses. It is designed to be read by an AI before producing any Ukrainian output.

**Audience target:** Diaspora US Ukrainian readers (anglicisms in established US trucking terminology are acceptable and often expected), written in a register accessible to any Ukrainian-speaker regardless of immigration recency.

**Author's note to the AI:** You are not translating. You are localizing. If your output reads like a translation, you have failed. Read this document fully before producing Ukrainian. When in doubt, consult Section 9 (Pre-Output Checklist) before responding.

---

## 1. Core Operating Principles

### 1.1 The Single Most Important Rule

**Do not translate sentence-by-sentence. Localize meaning-by-meaning.**

English and Ukrainian have fundamentally different sentence architectures. Preserving English word order in Ukrainian is the #1 source of "translated" feeling. A native Ukrainian speaker can detect a calque translation in under one second.

**Bad (translation):** *Будь ласка, надішліть ваші тижневі журнали до п'ятниці.*
**Good (localization):** *Журнали за тиждень надсилайте до п'ятниці.*

The second version drops the unnecessary "please/ваші/будь ласка", uses topic-first word order natural to Ukrainian, and uses an imperative form a real dispatcher would actually write.

### 1.2 The Native Speaker Test

Before outputting any Ukrainian sentence, mentally ask:

> "Would a native Ukrainian-speaker who has never seen the English original write this sentence this way?"

If the answer is "probably no, they'd say it differently" — rewrite. Do not output text that fails this test.

### 1.3 Localize Idioms, Don't Translate Them

English idioms, phrasal verbs, and business clichés must never be translated word-for-word. Replace with Ukrainian equivalent or rewrite the underlying meaning.

| English | ❌ Wrong (calque) | ✅ Right (localized) |
|---|---|---|
| reach out | дотягнутися | зв'язатися, написати |
| follow up | слідувати за | нагадати, уточнити |
| moving forward | рухаючись вперед | надалі, у подальшому |
| at the end of the day | в кінці дня | зрештою, врешті-решт |
| touch base | торкнутися бази | зв'язатися |
| circle back | кружляти назад | повернутися до питання |
| game changer | змінювач гри | переломний момент |
| low-hanging fruit | низько висячі фрукти | легко досяжні цілі |
| heads up | голови вгору | до відома, попередження |

### 1.4 Default to Brevity

Ukrainian written communication, especially in operational/business contexts, is **more concise** than English. English padding words usually disappear in good Ukrainian. Cut, don't add.

- "Please be advised that..." → ❌ *Просимо взяти до відома, що...* → ✅ Just state the fact, or use *Зверніть увагу:*
- "We would like to inform you..." → ❌ *Ми хотіли б повідомити вас...* → ✅ *Повідомляємо:*
- "In order to..." → ❌ *Для того щоб...* → ✅ *Щоб...*

---

## 2. Grammar Rules That Matter for Translation Quality

This section is not a complete grammar. It is the subset of Ukrainian grammar where AI translation most often fails.

### 2.1 Word Order (порядок слів)

Ukrainian has **free word order**. The grammatical role of a word is shown by its case ending, not its position. This means:

- The *most important new information* tends to go at the **end** of the sentence (the "rheme" position).
- The *topic / known information* tends to go at the **beginning** (the "theme" position).
- This is the **opposite** of English in many cases.

**Example:**

> English: "The driver submitted the report yesterday."
>
> If emphasizing *when*: *Звіт водій подав учора.* (yesterday is at the end — that's the new info)
>
> If emphasizing *what*: *Учора водій подав звіт.* (the report is the new info)
>
> If emphasizing *who*: *Учора звіт подав водій.* (the driver is the new info)

When translating, ask: **what's the new/important information?** Put that at the end. Don't blindly preserve subject-verb-object order.

### 2.2 The Six Cases — When Each One Triggers

Ukrainian has six cases. AI translators get cases wrong most often because they don't track the *semantic role* properly. Quick map:

| Case | Українська | Primary uses |
|---|---|---|
| Nominative | називний | Subject of the sentence; "the driver is..." |
| Genitive | родовий | Possession; negation ("there is no X"); after many prepositions (без, від, до, з); after numbers 2/3/4 (plural) and 5+ (genitive plural); partitive ("some of the fuel") |
| Dative | давальний | Indirect object ("to/for someone"); recipient of action; impersonal constructions ("мені треба") |
| Accusative | знахідний | Direct object; destination after some prepositions (на, у); duration ("на тиждень") |
| Instrumental | орудний | "with/by means of"; means of transportation (їхати вантажівкою); profession ("він працює водієм"); after deyaki prepositions (з, перед, над, під, за) |
| Locative | місцевий | ONLY used with prepositions; location ("у Сіракузах"); topic ("про водія") |
| Vocative | кличний | Direct address ("Іване!", "пане водію!") — used in greetings and in any direct address |

**Critical reminder:** The **vocative case is mandatory** in direct address in modern Ukrainian. It is NOT optional. Using nominative for direct address is a Russification.
- ❌ *Іван, перевір трейлер.*
- ✅ *Іване, перевір трейлер.*
- ❌ *Шановний водій!*
- ✅ *Шановний водію!*

### 2.3 Verb Aspect (вид дієслова) — THE Most Important Topic

Every Ukrainian verb exists in two aspects:

- **Imperfective (недоконаний вид)** — ongoing, repeated, habitual, or in-progress action. "I was doing X." "I do X regularly."
- **Perfective (доконаний вид)** — completed, one-time, result-focused action. "I did X (and finished)."

English doesn't grammaticalize this — Ukrainian does. AI translators routinely pick the wrong aspect, which makes sentences sound subtly off even when individual words are correct.

**Examples of common verb aspect pairs in trucking context:**

| Imperfective | Perfective | Meaning |
|---|---|---|
| писати | написати | to write |
| подавати | подати | to submit |
| перевіряти | перевірити | to check/inspect |
| заповнювати | заповнити | to fill out |
| відправляти | відправити | to send |
| отримувати | отримати | to receive |
| оновлювати | оновити | to update |
| робити | зробити | to do |
| читати | прочитати | to read |
| дзвонити | подзвонити | to call |
| вантажити | завантажити | to load |
| розвантажувати | розвантажити | to unload |

**Rules of thumb for choosing aspect:**

| Context | Aspect | Example |
|---|---|---|
| Single completed action with result | Perfective | *Я подав звіт.* (I submitted the report — and it's done) |
| Repeated/habitual action | Imperfective | *Я подаю звіти щотижня.* (I submit reports weekly) |
| In-progress action | Imperfective | *Я зараз заповнюю форму.* (I'm filling out the form right now) |
| Instruction to do once | Perfective imperative | *Заповніть форму.* (Fill out the form) |
| Instruction to do regularly | Imperfective imperative | *Заповнюйте звіти щодня.* (Fill out reports daily) |
| Negative instruction (don't do this) | Imperfective | *Не заповнюйте цю графу.* (Don't fill out this field) |
| Future single action | Perfective future | *Я перевірю.* (I'll check) |
| Future ongoing/repeated | Imperfective future (compound) | *Я буду перевіряти.* (I'll be checking) |

### 2.4 Articles & Pronouns — Drop Them

Ukrainian has **no articles** (no "the", no "a/an"). It also drops possessive pronouns and personal pronouns far more aggressively than English.

| English | ❌ Over-translated | ✅ Natural Ukrainian |
|---|---|---|
| Submit your report. | Подайте ваш звіт. | Подайте звіт. |
| I need to check my truck. | Мені потрібно перевірити мою вантажівку. | Мені треба перевірити вантажівку. |
| He has his license. | Він має свої права. | Він має права. |
| Show me your logs. | Покажіть мені ваші журнали. | Покажіть журнали. |

The only time to keep the possessive pronoun is when ownership is genuinely ambiguous or contrastive (*"my truck, not yours"* → *моя вантажівка, а не твоя*).

### 2.5 The "Ти" vs "Ви" Decision

| Use | When |
|---|---|
| **Ви** (formal, capitalized in formal writing) | All driver-facing documents, all customer-facing content, all compliance documents, all marketing copy, all forms, anything signed by a company representative |
| **ти** (informal) | ONLY in: informal internal team chat (if specifically requested), youth-oriented marketing (not your use case), personal correspondence between people who already use ти |

**Default to Ви always.** When unsure, Ви. The capital "В" in "Ви" is a sign of respect in formal correspondence and is standard in business letters and compliance docs.

**Plural Ви vs singular Ви** — both look identical but agree differently:
- Plural agreement (multiple people): *Ви подали звіт* (you-plural submitted)
- Polite singular: also *Ви подали звіт* (you-formal-singular submitted)
- The verb takes plural form in both cases — this is correct.

### 2.6 Numbers and Counting — Gotcha

Numbers in Ukrainian govern different cases. AI gets this wrong constantly.

- **1** (and any number ending in 1, except 11) → noun in nominative singular: *21 водій*
- **2, 3, 4** (and any number ending in 2/3/4, except 12/13/14) → noun in nominative plural (historically dual): *3 водії, 22 водії*
- **5+** (and 11–19) → noun in genitive plural: *5 водіїв, 15 водіїв, 100 водіїв*

For decimals/fractions: governs genitive singular. *1.5 кілометра, 2.3 галона*

### 2.7 Gender Agreement

Every noun has gender (masculine/feminine/neuter). Adjectives, pronouns, and past-tense verbs must agree. AI usually gets this right with common nouns but fails on:

- **Words borrowed from English** — pick a gender and stick with it: *лоуд* (m.), *брокер* (m.), *диспетчер* (m.), *компанія* (f.)
- **Profession nouns referring to women** — modern Ukrainian increasingly uses feminine forms (фемінітиви): *водійка, диспетчерка, менеджерка*. For US trucking diaspora context, **stick with masculine forms by default** unless writing specifically about/to a female recipient who prefers the feminine form.

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
| багаточисленні | численні | numerous |
| охрана | охорона | security, protection |
| опасний | небезпечний | dangerous |
| остановка | зупинка | stop (bus stop, etc.) |
| отримати інформацію по... | отримати інформацію про/щодо... | receive information about |
| по почті | поштою | by mail |
| по факсу | факсом | by fax |
| по телефону | телефоном / по телефону | by phone (both acceptable but "телефоном" preferred) |
| появитися | з'явитися | to appear |
| виключити (turn off) | вимкнути | to turn off |
| включити (turn on) | увімкнути | to turn on |

### 3.2 Russified Syntax — Patterns to Avoid

**Pattern 1: "по + dative" overuse**
Russian uses "по" extensively where Ukrainian uses other prepositions or no preposition at all.
- ❌ *звіт по водіях* → ✅ *звіт про водіїв / щодо водіїв*
- ❌ *графік по тижнях* → ✅ *графік за тижнями / тижневий графік*
- ❌ *робота по компліансу* → ✅ *робота з компліансу / робота в галузі компліансу*

**Pattern 2: Active participles in -чий/-щий**
Ukrainian historically avoids active participles ending in -чий/-щий that Russian uses freely. Restructure with a relative clause.
- ❌ *водій, керуючий вантажівкою* → ✅ *водій, який керує вантажівкою*
- ❌ *компанія, надаюча послуги* → ✅ *компанія, яка надає послуги*

**Pattern 3: "являється" instead of "є"**
- ❌ *Він являється водієм нашої компанії.*
- ✅ *Він є водієм нашої компанії.* (or even simpler: *Він — водій нашої компанії.*)

**Pattern 4: Verb + "у/в" + locative for time periods**
- ❌ *у наступному тижні* → ✅ *наступного тижня*
- ❌ *у цьому році* → ✅ *цього року*

### 3.3 Russified Business Jargon — The "Soviet" Sound

| ❌ Russified / Soviet-era | ✅ Modern Ukrainian | Meaning |
|---|---|---|
| даний документ | цей документ | this document |
| вищезазначений | вищезгаданий / згаданий вище | aforementioned |
| доводжу до Вашого відома | повідомляю Вам / інформую Вас | I inform you |
| у зв'язку з вищевикладеним | у зв'язку з цим | in connection with the above |
| надати інформацію | надати інформацію (OK) but avoid "предоставити" | provide information |
| предоставити | надати | to provide |
| обновити | оновити | to update |
| продовжуючий | який продовжує | continuing |
| прийняти рішення | ухвалити рішення | to make a decision |
| прийняти закон | ухвалити закон | to pass a law |
| розпрощатися | попрощатися | to say goodbye |
| розпорядження | розпорядження (OK but consider "наказ" or "доручення") | instruction, order |

### 3.4 The "Калька" Test

After writing any sentence, ask: **"Could this have been mechanically translated from English/Russian word-for-word?"** If yes, rewrite.

---

## 4. Register & Tone Rules by Content Type

The same information should be phrased differently depending on the document type. This section codifies the rules.

### 4.1 Driver-Facing Compliance Documents

**Audience:** Working drivers, often reading quickly between dispatches. May have varying levels of Ukrainian literacy.

**Rules:**
- Use formal **Ви**.
- Short sentences. One idea per sentence.
- Imperative mood for action items (perfective for one-time, imperfective for habitual).
- Use bullets and numbered lists liberally.
- Keep US trucking anglicisms (ELD, DOT, IFTA, лоуд, дроп) — drivers use these daily.
- Avoid legalese. Where English uses passive voice for legal weight, use Ukrainian impersonal constructions: *необхідно, слід, забороняється, потрібно*.
- Concrete > abstract. *"Подайте журнал щодня до 23:00"* > *"Своєчасна подача журналів обов'язкова."*

**Example:**

> English: "All drivers are required to submit their daily logs by 11:00 PM EST. Failure to comply may result in disciplinary action."
>
> ✅ Localized: "Лог за день потрібно подати до 23:00 за східним часом. За невчасну подачу — дисциплінарне стягнення."

### 4.2 FleetCtrl Marketing & Product Copy

**Audience:** Small fleet owners and owner-operators, 1–25 trucks. Often first-generation US immigrants from Ukraine; bilingual; runs the business themselves.

**Rules:**
- Use formal **Ви** but warmer/more direct than legal docs.
- Confident, practical tone. No marketing fluff, no Soviet-style business jargon.
- Address pain points concretely, not abstractly.
- US trucking anglicisms acceptable and expected (FleetCtrl, IFTA, FMCSA, CSA score).
- Active voice. Verbs over nouns.
- Avoid the "корпоративний" sound: no *оптимізація бізнес-процесів, синергія, рішення нового покоління*.
- Numbers and specifics > generalities. *"Заощадить 4 години на тиждень"* > *"Підвищить ефективність."*

**Example:**

> English: "FleetCtrl helps you stay DOT-compliant without the paperwork headache."
>
> ✅ Localized: "FleetCtrl бере на себе DOT-папери — щоб ви не сиділи над ними вечорами."
>
> (Note: the English is abstract ("compliance headache"). The Ukrainian makes it concrete ("so you're not sitting over them in the evenings") — which is how a Ukrainian-speaking fleet owner actually thinks about the problem.)

### 4.3 Internal Forms & Paperwork

**Audience:** Staff filling out forms internally. Sometimes drivers, sometimes office staff.

**Rules:**
- Use formal **Ви** in any instructions.
- Form field labels: noun phrases, not sentences. *Дата подачі* not *Введіть дату подачі.*
- Consistency over elegance — same term means same thing every time. Lock terminology to the glossary in Section 6.
- Date format: keep US convention (MM/DD/YYYY) since paperwork integrates with US systems.
- Units: keep US conventions (miles, gallons, pounds).
- Section headers: bold noun phrases.

### 4.4 Email & Operational Messages

**Audience:** Drivers, vendors, partners.

**Rules:**
- Formal **Ви**.
- Subject lines: short noun phrases, not sentences.
- No "I hope this email finds you well" equivalent — Ukrainian business email skips the small talk.
- Open with the point. *"Прошу подати IFTA-звіт за Q1 до 15 квітня."*
- Sign-off: *З повагою, [Name]* is standard.

### 4.5 Legal / Compliance Documents (Contracts, Agreements)

**Audience:** Legal review + drivers signing.

**Rules:**
- Formal **Ви**, third-person where appropriate.
- Use modern Ukrainian legal terminology, not Soviet-era.
- Define terms at first use. *"FleetCtrl (далі — «Платформа»)..."*
- Numbered sections (1.1, 1.2, etc.).
- Avoid both calques from English contracts AND Russified legalese.

---

## 5. The Diaspora US Ukrainian Flavor — What This Means in Practice

Per the target audience (US-based Ukrainian-speaking fleet operators and drivers), this doc accepts a specific category of anglicisms that would feel out of place in Ukraine-published content but are natural and expected in US trucking context.

### 5.0 The Formal vs Informal Terminology Hierarchy — CRITICAL

Several common trucking terms have **two acceptable Ukrainian forms**: a casual/operational form that drivers and dispatchers actually use, and a formal/legal form for contracts and government filings. Picking the wrong one is one of the fastest ways to sound either bureaucratic-and-stuffy or unprofessionally-casual.

**Rule:** Choose based on document type, not personal preference.

| Concept | Driver/Ops/Marketing default | Formal/Legal default |
|---|---|---|
| Truck/Tractor | **трак** | вантажівка / тягач |
| Load (shipment) | **груз** | вантаж |
| Fleet | **автопарк** | автопарк (same) |
| Inspection | **перевірка** | перевірка (same) |
| Pre-trip inspection | **PTI** | передрейсова перевірка |
| Random drug test | **рандомний наркотест** | тестування на наркотики (випадкове) |
| Logbook | **журнал** | журнал водія / журнал обліку робочого часу |
| Daily log entry | **запис за день** | запис у журналі обліку |

**When in doubt about which to use:**
- Email to a driver? → operational
- Text from dispatch? → operational
- FleetCtrl marketing page? → operational
- Driver-facing instruction in an app? → operational
- Government compliance filing? → formal
- Insurance certificate? → formal
- Lease agreement, employment contract? → formal
- DOT/FMCSA-submitted document? → formal

**Words to avoid in both registers** (these are wrong, not just stylistically off):
- ❌ "флот" for a vehicle fleet — this means *naval fleet* in Ukrainian. Always use **автопарк** (or "парк" when context is unambiguous).
- ❌ "лог" / "логи" / "лог-журнал" — sounds like translated tech jargon. Use **журнал** for the document, **запис** for the entry.
- ❌ "спальник" for sleeper berth — ambiguous (also means sleeping bag). Use **спальне місце**.
- ❌ "інспекція" for vehicle inspection — Russified. Use **перевірка**.
- ❌ "випадковий" for random drug test — textbook-correct but no one says it. Use **рандомний**.

---
### 5.1 Anglicisms That Are Acceptable / Expected

These are how US Ukrainian-speaking truckers actually talk and write. Use them.

| Anglicism (Ukrainian transliteration) | Pronunciation | English origin | Notes |
|---|---|---|---|
| груз | (native UA word, preferred) | load (a shipment) | **Default term in driver/ops context.** "Вантаж" reserved for formal/legal docs only |
| лоуд | "load" | load (a shipment) | Acceptable in informal dispatcher chat; "груз" preferred in writing |
| трак | "truck" | truck/semi-truck | **Default term in driver/ops context.** "Вантажівка/тягач" reserved for formal/legal docs only |
| дроп | "drop" | drop trailer | "дроп-енд-хук" = drop-and-hook |
| хук | "hook" | hook trailer | |
| дедхед | "deadhead" | deadhead (empty miles) | |
| бек-холл / бекхол | "back-haul" | back-haul | |
| овнер-оператор | "owner-operator" | owner-operator | |
| диспетч / диспатч | "dispatch" | dispatch | "Диспетчер" for the person |
| фрахт | "freight" | freight | This is also standard Ukrainian |
| тру́кер | "trucker" | trucker | |
| компанія-керієр | "company carrier" | company carrier | Or just "керієр" |
| шіпер | "shipper" | shipper | |
| консайні | "consignee" | consignee | |
| тендер | "tender" | load tender | |
| рейт | "rate" | rate (per mile) | "Рейт пер майл" is common |
| майл / маїл | "mile" | mile | Keep "майл" not "миля" in US context |
| галон | "gallon" | gallon | |
| ярд | "yard" | yard | Also "гараж" — see glossary |
| док | "dock" | dock | |
| лампер | "lumper" | lumper (unloading service) | |
| детеншн | "detention" | detention (waiting fees) | |
| лейовер | "layover" | layover | |
| ріфер | "reefer" | refrigerated trailer | |
| флатбед | "flatbed" | flatbed | |
| драй ван | "dry van" | dry van | |
| ELD | "i-el-di" | ELD | Keep in Latin script |
| DOT | "di-o-ti" | DOT | Keep in Latin script |
| FMCSA | acronym | FMCSA | Keep in Latin script |
| IFTA | "iftA" | IFTA | Keep in Latin script |
| IRP | "i-ar-pi" | IRP | Keep in Latin script |
| HOS | acronym | Hours of Service | Keep in Latin script |
| PTI | "pi-ti-ai" | Pre-Trip Inspection | Keep in Latin script — drivers use the acronym |
| CDL | acronym | CDL | Keep in Latin script |
| MC# / DOT# | acronym | MC/DOT numbers | Keep in Latin script |
| BOL | acronym | Bill of Lading | Or "товарно-транспортна накладна" in formal docs |
| POD | acronym | Proof of Delivery | |
| ETA | acronym | ETA | |
| GPS | acronym | GPS | |

### 5.2 Anglicisms That Are NOT Acceptable

These are calques that don't help and hurt readability.

| ❌ Don't use | ✅ Use instead | English |
|---|---|---|
| контрол | контроль | control |
| компанія-перевізник | керієр / компанія (or "перевізник" without "компанія-") | carrier |
| веб-сайт | сайт | website |
| імейл | електронна пошта (formal) / email (informal) | email |
| кеш | готівка | cash (money) |

### 5.3 Capitalization Rule for Anglicisms

- **Common-noun anglicisms** transliterated into Cyrillic: lowercase. *лоуд, дроп, ярд*
- **Acronyms from English** for US government bodies, technical standards: keep in **Latin script, all caps**. *DOT, IFTA, FMCSA, ELD, CDL, BOL*
- **Brand names and proper nouns**: keep original form. *Motive, FleetChaser, Mudflap, TCS, EFS, Empire Auto Transportation Group, FleetCtrl*

---

## 6. Domain Glossary

This is the locked terminology. Same English term → same Ukrainian term every time. Add to this list as new terms come up.

### 6.1 People & Roles

| English | Ukrainian | Notes |
|---|---|---|
| Driver | Водій | |
| Driver (female, optional) | Водійка | Only if specifically referring to a woman |
| Owner-operator | Овнер-оператор | Diaspora term, universal |
| Independent contractor | Незалежний підрядник | |
| Dispatcher | Диспетчер | |
| Fleet manager | Менеджер автопарку | NOT "флот-менеджер" — "флот" means naval fleet |
| Safety manager | Менеджер з безпеки | |
| Compliance manager | Менеджер з відповідності вимогам | |
| Mechanic | Механік | |
| Broker | Брокер | |
| Shipper | Шіпер (informal) / Вантажовідправник (formal) | |
| Consignee | Консайні (informal) / Вантажоодержувач (formal) | |
| Carrier | Керієр (informal) / Перевізник (formal) | |
| DOT inspector | DOT-інспектор | |
| Recruiter | Рекрутер | |

### 6.2 Vehicles & Equipment

| English | Ukrainian | Notes |
|---|---|---|
| Truck (semi) | Трак | **Default in driver/ops/marketing contexts.** Use "вантажівка" only in legal/contract docs |
| Tractor | Трак | Default. "Тягач" reserved for legal/contract docs where the tractor unit needs to be distinguished from the trailer |
| Trailer | Трейлер | |
| Dry van | Драй ван | |
| Reefer | Ріфер | |
| Flatbed | Флатбед | |
| Step deck | Степ-дек | |
| Lowboy | Лоубой | |
| Car hauler | Авто-керієр / автовоз | Relevant for Anna's auto-haul fleet |
| Box truck | Бокс-трак | |
| Sleeper berth | Спальне місце | Avoid "спальник" (ambiguous — also means sleeping bag) |
| VIN | VIN | Keep Latin |
| License plate | Номерний знак | |
| Odometer | Одометр | |
| Axle | Вісь | |
| Tire | Шина | |
| Fuel tank | Паливний бак | |
| Fifth wheel | П'яте колесо | |
| Kingpin | Кінгпін | |

### 6.3 Operations & Movements

| English | Ukrainian | Notes |
|---|---|---|
| Load | Груз | **Default in driver/ops contexts.** "Лоуд" OK in informal dispatcher chat; "вантаж" reserved for formal/legal docs |
| Drop and hook | Дроп-енд-хук | |
| Deadhead | Дедхед / порожній пробіг | |
| Backhaul | Бекхол | |
| Pickup | Підбір / пікап грузу | |
| Delivery | Доставка | |
| Detention | Детеншн | |
| Layover | Лейовер | |
| Bobtail | Боб-тейл | Tractor without trailer |
| Empty miles | Порожні майли | |
| Loaded miles | Завантажені майли | |
| Route | Маршрут | |
| Lane | Лейн / напрямок | |
| Origin | Точка відправлення | |
| Destination | Точка призначення | |
| Yard | Ярд / гараж | "Ярд" for company lot in trucking slang; "гараж" for the practical "where trucks are parked" |
| Dock | Док | |
| Loading dock | Завантажувальний док | |
| Lumper | Лампер | |
| Lumper fee | Оплата лампера | |

### 6.4 Compliance & Regulatory

| English | Ukrainian | Notes |
|---|---|---|
| Compliance | Відповідність вимогам | NEVER "комплаєнс" — Russified |
| DOT | DOT | Keep Latin |
| FMCSA | FMCSA | Keep Latin |
| DOT number | DOT-номер | |
| MC number | MC-номер | |
| DOT inspection | DOT-перевірка | |
| Annual inspection | Річна перевірка | |
| CSA score | CSA-рейтинг | |
| DataQs | DataQs | Keep Latin |
| Violation | Порушення | |
| Citation | Штраф / припис | |
| Out of service (OOS) | Виведення з експлуатації | |
| Driver qualification file (DQ file) | Файл кваліфікації водія / DQ-файл | |
| Medical certificate (DOT med card) | DOT-медкарта / медичний сертифікат | |
| Drug & alcohol testing | Тестування на наркотики та алкоголь | |
| Clearinghouse | Clearinghouse | Keep English |
| MVR (Motor Vehicle Record) | MVR / водійський запис | |
| PSP (Pre-employment Screening) | PSP | Keep Latin |

### 6.5 Hours of Service & Logs

| English | Ukrainian | Notes |
|---|---|---|
| Hours of Service (HOS) | HOS / години роботи | |
| ELD | ELD | Keep Latin |
| Logbook | Журнал водія | NOT "лог-журнал" — use plain "журнал" |
| Daily log | Запис за день / щоденний журнал | NOT "лог" — use "запис" for the entry, "журнал" for the document |
| Log entry | Запис | The individual entry in the journal |
| On-duty | На зміні | |
| Off-duty | Поза зміною / off-duty | |
| Driving time | Час за кермом | |
| Sleeper berth | Спальне місце | Avoid "спальник" (ambiguous) |
| 30-minute break | 30-хвилинна перерва | |
| 14-hour rule | Правило 14 годин | |
| 11-hour driving limit | Ліміт 11 годин водіння | |
| 70-hour rule | Правило 70 годин | |
| Reset / 34-hour reset | Ресет / 34-годинний ресет | |
| Violation log | Журнал порушень | |

### 6.6 Fuel & Mileage (IFTA)

| English | Ukrainian | Notes |
|---|---|---|
| IFTA | IFTA | Keep Latin |
| IFTA report | IFTA-звіт | |
| Quarterly filing | Квартальна звітність | |
| Fuel card | Паливна картка | |
| Fuel receipt | Чек за паливо | |
| Fuel tax | Паливний податок | |
| Mileage | Пробіг / майлідж | |
| Per-mile rate | Рейт пер майл / ставка за майл | |
| IRP | IRP | Keep Latin |
| Apportioned plate | Розподілений номерний знак | |
| NYS HUT | NYS HUT | Keep Latin (Anna's context) |
| Thruway mileage | Пробіг по Thruway | Keep "Thruway" |

### 6.7 Documents & Paperwork

| English | Ukrainian | Notes |
|---|---|---|
| Bill of Lading (BOL) | BOL / товарно-транспортна накладна | |
| Proof of Delivery (POD) | POD / підтвердження доставки | |
| Rate confirmation | Рейт-конфірмейшн / підтвердження ставки | |
| Carrier packet | Керієр-пакет | |
| Insurance certificate (COI) | COI / страховий сертифікат | |
| W-9 | W-9 | Keep Latin |
| 1099 | 1099 | Keep Latin |
| 2290 | 2290 | Keep Latin (Heavy Vehicle Use Tax) |
| Form MT-903 | Форма MT-903 | |
| Authority (operating authority) | Авторіті / операційна ліцензія | |
| Lease agreement | Договір оренди | |

### 6.8 Money & Payments

| English | Ukrainian | Notes |
|---|---|---|
| Settlement | Сетлмент / розрахунок | |
| Pay statement | Платіжна відомість | |
| Net pay | Чистий заробіток | |
| Deduction | Утримання | |
| Advance | Аванс | |
| Factoring | Факторинг | |
| Quick pay | Quick pay / швидка оплата | |
| ACH | ACH | Keep Latin |
| Wire transfer | Банківський переказ | |
| Invoice | Інвойс / рахунок | "Інвойс" in informal, "рахунок" in formal |

### 6.9 FleetCtrl & SaaS Product Terms

| English | Ukrainian | Notes |
|---|---|---|
| FleetCtrl | FleetCtrl | Never translate brand name |
| Dashboard | Дашборд | |
| Spreadsheet | Таблиця | |
| Google Sheets | Google Sheets | Keep brand |
| Trigger | Тригер | |
| Reminder | Нагадування | |
| Notification | Сповіщення | |
| Settings | Налаштування | |
| Configuration | Конфігурація | |
| User | Користувач | |
| Account | Акаунт / обліковий запис | "Акаунт" informal, "обліковий запис" formal |
| Login | Увійти / логін | |
| Password | Пароль | |
| Sign up | Зареєструватися | |
| Subscription | Підписка | |
| Trial | Пробний період | |
| Plan / tier | Тариф / план | |
| Feature | Функція | |
| Bug | Баг / помилка | |
| Update | Оновлення | |
| Release | Реліз / випуск | |
| Integration | Інтеграція | |
| API | API | Keep Latin |
| Webhook | Вебхук | |

---

## 7. Side-by-Side Examples

These show the difference between bad translation and good localization. Study these patterns.

### Example 1: Driver Reminder Email

**English source:**
> "Hi John, just a friendly reminder that your DOT medical certificate is expiring on March 15. Please schedule your renewal appointment as soon as possible to avoid any disruption to your driving status."

**❌ Bad (calque translation):**
> "Привіт Джон, просто дружнє нагадування, що ваш DOT медичний сертифікат закінчується 15 березня. Будь ласка, заплануйте ваше призначення на оновлення якомога швидше, щоб уникнути будь-якого порушення вашого водійського статусу."

**Problems:** Vocative case missing, possessive overuse, calque "дружнє нагадування" and "призначення на оновлення", word-for-word English structure.

**✅ Good (localization):**
> "Іване, нагадуємо: DOT-медкарта закінчується 15 березня. Запишіться на оновлення якнайшвидше — інакше доведеться зупинити роботу."

**Why it works:** Vocative case ("Іване"), drops unnecessary "ваш", uses the natural collocation "DOT-медкарта", direct consequence statement at the end (rheme position), imperative aspect appropriate to a single action.

---

### Example 2: FleetCtrl Marketing Headline

**English source:**
> "Stop drowning in compliance paperwork. FleetCtrl automates DOT, FMCSA, and IFTA documentation so you can focus on growing your fleet."

**❌ Bad:**
> "Перестаньте тонути в документації по відповідності. FleetCtrl автоматизує DOT, FMCSA та IFTA документацію, щоб ви могли зосередитися на зростанні вашого флоту."

**Problems:** "Документації по відповідності" is awkward calque + "по" Russification. "Зростанні вашого флоту" — "флот" in Ukrainian means a naval fleet, wrong word here. Preserves English structure.

**✅ Good:**
> "Менше паперів — більше бізнесу. FleetCtrl автоматизує DOT, FMCSA та IFTA — а ви займаєтеся автопарком."

**Why it works:** Punchy opening contrast that Ukrainian marketing actually uses. "Автопарк" is the correct Ukrainian word for a vehicle fleet (not "флот" which means ships). Acronyms kept in Latin (US trucking convention). The structure "а ви займаєтеся X" frames the customer benefit naturally.

---

### Example 3: Internal Form Instruction

**English source:**
> "Enter the truck VIN, current odometer reading, and date of inspection. If the truck failed inspection, check the appropriate box and add notes in the comments section."

**❌ Bad:**
> "Введіть VIN вантажівки, поточне показання одометра та дату інспекції. Якщо вантажівка не пройшла інспекцію, поставте галочку у відповідній клітинці та додайте примітки в секції коментарів."

**Problems:** "Поточне показання" is too long, "не пройшла інспекцію" is OK but verbose, "у відповідній клітинці" is heavy. Note: this is an internal form, so "вантажівка" is acceptable — but in a driver-facing instruction, "трак" would be preferred.

**✅ Good (internal form, formal):**
> "Вкажіть VIN, покази одометра та дату перевірки. Якщо перевірку не пройдено — позначте галочкою та опишіть у коментарях."

**✅ Good (driver-facing version):**
> "Вкажіть VIN трака, покази одометра та дату перевірки. Якщо трак не пройшов PTI — позначте галочкою та опишіть у коментарях."

**Why it works:** Drops redundant noun where context makes it clear. Uses "перевірка" not "інспекція" (proper Ukrainian). Impersonal passive "не пройдено" reads naturally for internal forms; "трак" + "PTI" reads naturally for driver-facing.

---

### Example 4: Compliance Document

**English source:**
> "All drivers must complete pre-trip inspections before operating any commercial motor vehicle. Inspections must be documented on the DVIR form and submitted to the dispatcher by end of shift."

**❌ Bad:**
> "Всі водії повинні виконувати передрейсові інспекції перед експлуатацією будь-якого комерційного моторного транспортного засобу. Інспекції повинні бути задокументовані на формі DVIR та подані диспетчеру до кінця зміни."

**Problems:** "Повинні виконувати" + "повинні бути задокументовані" — heavy modal+passive stack. "Будь-якого комерційного моторного транспортного засобу" is a literal calque of the regulatory English phrase, but Ukrainian drivers don't speak this way.

**✅ Good (driver-facing operational doc):**
> "Перед виїздом водій зобов'язаний провести PTI трака. Результати заносяться у форму DVIR і передаються диспетчеру до кінця зміни."

**✅ Good (formal legal/contract version):**
> "Перед виїздом водій зобов'язаний провести передрейсову перевірку вантажівки. Результати заносяться у форму DVIR і передаються диспетчеру до кінця зміни."

**Why it works:** Singular "водій" reads more directly than "всі водії". Replaces stacked passives with impersonal active ("заносяться", "передаються"). Driver-facing version uses "PTI" + "трак" (what drivers actually say); legal version uses formal terminology. Both drop the bureaucratic "комерційний моторний транспортний засіб".

---

## 8. Quick Lookup: Common Trucking Phrases

| English | Ukrainian |
|---|---|
| Pre-trip inspection | PTI / передрейсова перевірка | Drivers use "PTI" — keep Latin acronym |
| Post-trip inspection | Післярейсова перевірка |
| Daily vehicle inspection report (DVIR) | DVIR / щоденний звіт про перевірку транспорту |
| Hours of service violation | Порушення HOS |
| Out of service order | Припис про виведення з експлуатації |
| Falsification of logs | Підробка журналів |
| Drug & alcohol test | Тест на наркотики та алкоголь |
| Random drug test | Рандомний наркотест |
| Post-accident test | Тест після аварії |
| Reasonable suspicion test | Тест за обґрунтованою підозрою |
| Return-to-duty test | Тест на повернення до роботи |
| Background check | Перевірка біографії / бекграунд-чек |
| Driving record | Водійський запис / MVR |
| Annual review | Щорічна перевірка |
| Hazmat endorsement | Hazmat-сертифікація |
| Doubles/triples endorsement | Сертифікація на причепи (doubles/triples) |
| Tanker endorsement | Tanker-сертифікація |
| Pre-employment screening | Перевірка перед працевлаштуванням |

---

## 9. Pre-Output Checklist (Run Before Every Response)

Before outputting any Ukrainian text, mentally verify each of the following. If any check fails, rewrite.

**Grammar checks:**
1. ☐ Word order: is the new/important information at the end (rheme)?
2. ☐ Cases: is every noun/pronoun in the correct case for its semantic role?
3. ☐ Verb aspect: did I pick the right aspect for each verb? (Completed vs ongoing vs habitual)
4. ☐ Vocative: am I addressing someone directly? If so, vocative case used?
5. ☐ Gender agreement: do adjectives, past-tense verbs, and pronouns match noun gender?
6. ☐ Numbers: is the noun in the right case after each number (1 / 2-4 / 5+)?

**Style checks:**
7. ☐ Did I drop unnecessary "ваш/мій/свій" possessives?
8. ☐ Did I drop unnecessary personal pronouns?
9. ☐ Did I use Ви (formal), capitalized in formal docs?

**Russification checks:**
10. ☐ Any "по + dative" that should be "про/щодо/з/за"?
11. ☐ Any "являється" — replace with "є" or em-dash?
12. ☐ Any active participles in -чий/-щий — restructure with relative clause?
13. ☐ Any words from the Section 3 forbidden list? Replace.
14. ☐ Any Soviet-era business jargon? Replace with modern Ukrainian.

**Domain checks:**
15. ☐ Trucking terms match Section 6 glossary? (Same English term → same Ukrainian term)
16. ☐ **Register-matched terminology**: Did I use the operational form (трак, груз, PTI) for driver/marketing content, OR the formal form (вантажівка, вантаж, передрейсова перевірка) for legal/government docs?
17. ☐ Did I avoid the forbidden words: флот, лог/логи, спальник, інспекція, випадковий (drug test)?
18. ☐ Acronyms (DOT, IFTA, ELD, FMCSA, PTI) kept in Latin script?
19. ☐ Brand names preserved (FleetCtrl, Motive, Mudflap, etc.)?
20. ☐ US conventions kept where appropriate (miles, gallons, MM/DD/YYYY)?

**Tone checks:**
21. ☐ Does the register match the content type (driver doc / marketing / form / legal)?
22. ☐ Is it as concise as it can be without losing meaning?
23. ☐ Does it pass the **Native Speaker Test**: would a native Ukrainian-speaker write it this way without seeing the English?

---

## 10. Quick Reference Card — Print This

**The 10 commandments of Ukrainian localization:**

1. **Localize, don't translate.** Rewrite for Ukrainian flow.
2. **Drop articles and unnecessary possessives.** Ukrainian uses fewer than English.
3. **Use vocative case for direct address.** Always.
4. **Pick the right verb aspect.** Perfective for completed, imperfective for ongoing/habitual.
5. **Default to formal Ви.** Capitalize in formal writing.
6. **Match register to document type.** Driver/ops → трак, груз, PTI, журнал. Legal/contract → вантажівка/тягач, вантаж, передрейсова перевірка, журнал водія.
7. **Avoid the forbidden words.** Never use: флот (means naval fleet), лог/логи (translated jargon), спальник (ambiguous), інспекція (Russified), випадковий drug test (no one says it).
8. **Avoid Russifications.** "Протягом" not "на протязі". "Відповідно до" not "у відповідності з". "Брати участь" not "приймати участь". "Є" not "являється".
9. **Avoid active participles in -чий/-щий.** Use relative clauses.
10. **Keep US trucking anglicisms and acronyms.** ELD, DOT, IFTA, FMCSA, PTI, лоуд, дроп, ярд. Keep brand names in original form: FleetCtrl, Motive, Mudflap, Empire Auto Transportation Group.

---

## 11. How to Use This Document in a Claude Project

**Setup:**
1. Add this file to the Project Knowledge of every Claude Project that performs Ukrainian translation.
2. In the Project's system prompt, add: *"Before producing any Ukrainian text, consult `ukrainian-localization-reference.md`. Follow all rules in Sections 1–6. Run the checklist in Section 9 before outputting."*

**Suggested project-level system prompt:**

```
You are a professional Ukrainian localizer for FleetCtrl and
associated trucking compliance businesses. You localize English
content into natural Ukrainian — you never translate word-for-word.

Before producing Ukrainian output:
1. Determine the content type (driver doc / marketing / form / legal).
2. Apply the corresponding tone rules from Section 4 of the reference.
3. Use the locked glossary from Section 6 — same term, same translation.
4. Avoid Russifications listed in Section 3.
5. Run the Section 9 checklist mentally before each output.

Default to formal Ви. Keep US trucking anglicisms (ELD, DOT, IFTA,
лоуд, дроп) — diaspora audience expects them. Keep all brand names
and US regulatory acronyms in original Latin form.

Output only the Ukrainian text. No explanations unless asked.
```

**Iteration:**
- When you spot a bad translation, note what was wrong.
- Update the relevant section of this document.
- Re-upload to your Projects.
- Quality compounds over time.

---

## 12. Version History & Updates

| Version | Date | Changes |
|---|---|---|
| 1.0 | 2026-05 | Initial release. Diaspora US Ukrainian flavor, audience-neutral for any Ukrainian-speaker. Covers driver-facing, marketing, forms, legal registers. Trucking + compliance + SaaS glossary. |
| 1.1 | 2026-05 | **Native-speaker corrections from Anna (operator, Empire Auto Transportation Group):** (1) Added formal-vs-operational register hierarchy (Section 5.0) as core principle. (2) Truck/Tractor: **трак** default for ops/driver/marketing; "вантажівка/тягач" reserved for legal/contract. (3) Load: **груз** default for ops; "лоуд" OK informal; "вантаж" reserved for legal/contract. (4) Fleet: **автопарк** — "флот" is wrong (means naval fleet in Ukrainian) and added to forbidden words list. (5) Logbook/log: **журнал** (document) and **запис** (entry) — "лог/логи" eliminated from glossary, added to forbidden words. (6) Sleeper berth: **спальне місце** — "спальник" removed (ambiguous, also means sleeping bag). (7) Yard: **ярд/гараж** — added "гараж" as practical alternate. (8) Random drug test: **рандомний наркотест** — "випадковий" textbook-correct but unused in practice. (9) Pre-trip inspection: **PTI** acronym preferred in driver/ops; "передрейсова перевірка" reserved for legal/contract. Side-by-side examples (Section 7) updated to reflect new defaults; commandments and pre-output checklist updated. |

**Maintainer's note:** This is a living document. Add new glossary entries as terms come up. Add new Russification anti-patterns as you spot them in the wild. Add new side-by-side examples whenever a particularly bad translation gets corrected — those examples teach the AI faster than rules do.
