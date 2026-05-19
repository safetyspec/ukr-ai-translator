# Real Before/After Examples

A growing collection of bad AI translations from the wild, with corrected versions and explanations of what went wrong.

These are useful as:
- Test cases when evaluating new prompt/reference versions
- Teaching material for understanding common AI failure modes
- Quick reference for "have I seen this pattern before?"

To contribute new examples, see [CONTRIBUTING.md](../CONTRIBUTING.md).

---

## Format

Each example follows this structure:

- **Source**: The English original
- **❌ Bad**: What AI produced (specify which AI if known)
- **Issues**: What's specifically wrong
- **✅ Good**: The corrected version
- **Rules applied**: Which section(s) of `general.md` apply
- **Date / context**: When this was caught, what tool

---

## Examples by Content Type

### Customer Support / Service

#### Example: Account Closure Confirmation

**Source:**
> "We're sorry to see you go! Your account has been successfully closed. If you change your mind, you can reactivate within 30 days by logging back in. Thank you for being part of our community."

**❌ Bad:**
> "Нам шкода бачити, як ви йдете! Ваш акаунт був успішно закритий. Якщо ви передумаєте, ви можете реактивувати його протягом 30 днів, увійшовши назад. Дякуємо за те, що були частиною нашої спільноти."

**Issues:**
- "Нам шкода бачити, як ви йдете" — direct calque of "we're sorry to see you go"; not natural Ukrainian
- "Ваш акаунт був успішно закритий" — passive construction + unnecessary "ваш"
- "Реактивувати" — anglicism where "поновити/відновити" reads better
- "Увійшовши назад" — calque of "logging back in"
- "Бути частиною нашої спільноти" — Soviet-era community jargon-ish

**✅ Good:**
> "Шкода, що йдете. Акаунт закрито. Якщо передумаєте — увійдіть протягом 30 днів, і ми його відновимо. Дякуємо, що були з нами."

**Rules applied:** §1.1 (localize don't translate), §1.4 (brevity), §2.4 (drop possessives), §3.2 Pattern 6 (passive voice overuse)

---

### Marketing / Landing Pages

#### Example: SaaS Hero Headline

**Source:**
> "Save hours every week by automating your busywork. Join 10,000+ teams already growing faster with us."

**❌ Bad:**
> "Заощаджуйте години щотижня, автоматизуючи вашу рутинну роботу. Приєднуйтесь до 10,000+ команд, які вже зростають швидше з нами."

**Issues:**
- "Заощаджуйте години щотижня, автоматизуючи..." — long, gerund-heavy; preserves English structure
- "Вашу рутинну роботу" — unnecessary "вашу"
- "10,000+" — wrong thousand separator (UA uses spaces: "10 000+")
- "Які вже зростають швидше з нами" — calque of "growing faster with us"

**✅ Good:**
> "Менше рутини — більше результату. Понад 10 000 команд уже з нами."

**Rules applied:** §1.4 (brevity), §1.5 (number conventions), §4.3 (marketing tone), §2.4 (drop possessives)

---

### Product UI Strings

#### Example: Empty State Message

**Source:**
> "You don't have any projects yet. Create your first project to get started!"

**❌ Bad:**
> "У вас ще немає жодних проектів. Створіть ваш перший проект, щоб почати!"

**Issues:**
- "У вас ще немає жодних проектів" — wordy
- "Ваш перший проект" — unnecessary "ваш"
- "Проектів" — pre-2019 spelling; should be "проєктів"
- "Щоб почати" — passable but flat

**✅ Good:**
> "Проєктів ще немає. Створіть перший — і починайте."

**Rules applied:** §2.4 (drop possessives), §5.4 (Правопис 2019), §4.2 (product UI brevity)

---

### Error Messages

#### Example: Form Validation Error

**Source:**
> "Please enter a valid email address."

**❌ Bad:**
> "Будь ласка, введіть дійсну електронну адресу."

**Issues:**
- "Будь ласка" — unnecessary in error message
- "Дійсну" — translation of "valid" but reads stiff; "правильну" is more natural
- "Електронну адресу" — formal; in UI, "емейл" is more common

**✅ Good:**
> "Введіть правильний емейл."

Or for formal context:

> "Введіть правильну електронну адресу."

**Rules applied:** §1.4 (brevity), §4.2 (UI: blameless and short)

---

### Casual / Personal

#### Example: Birthday Text

**Source:**
> "Happy birthday! Hope you have an amazing day filled with everything you love."

**❌ Bad:**
> "З днем народження! Сподіваюся, у вас буде дивовижний день, наповнений усім, що ви любите."

**Issues:**
- Sounds like a formal greeting card, not a personal text
- "Дивовижний день, наповнений усім, що ви любите" — heavy calque
- "Ви" register is wrong for casual birthday message

**✅ Good:**
> "З днем народження! Хай цей день буде наповнений усім, що ти любиш."

Or more casual:

> "З Днюхою! Бажаю, щоб день був як ти заслуговуєш — найкращим."

**Rules applied:** §2.5 (Ви/ти choice), §4.4 (casual tone), §1.1 (localize idioms)

---

### Legal / Formal

#### Example: Privacy Policy Snippet

**Source:**
> "By using this service, you agree to our Privacy Policy and Terms of Service. You may withdraw your consent at any time by contacting our support team."

**❌ Bad:**
> "Використовуючи цей сервіс, ви погоджуєтеся з нашою Політикою Конфіденційності та Умовами Обслуговування. Ви можете відкликати ваш дозвіл у будь-який час, зв'язавшись з нашою командою підтримки."

**Issues:**
- "Використовуючи цей сервіс" — active participle (-чи form) starting the sentence is fine, but "цей сервіс" + later "нашою" overcomplicates
- "Нашою Політикою Конфіденційності" — calque of English title case; UA doesn't capitalize this way
- "Ваш дозвіл" — unnecessary "ваш"
- "Зв'язавшись з нашою командою підтримки" — calque

**✅ Good:**
> "Використання сервісу означає згоду з Політикою конфіденційності та Умовами користування. Згоду можна відкликати в будь-який момент, написавши в службу підтримки."

**Rules applied:** §4.7 (legal tone), §2.4 (drop possessives), §3 (avoid English-style title case)

---

### Common Idioms / Phrases

#### Example: "Looking forward to hearing from you"

**Source:**
> "Looking forward to hearing from you."

**❌ Bad:**
> "З нетерпінням чекаю почути від вас."

**Issues:**
- "Почути від вас" — direct calque of "hear from you"
- "З нетерпінням чекаю" — overly emotional; calque of "looking forward"

**✅ Good:**
> "Чекаю Вашої відповіді."

Or in casual:

> "Чекаю!"

**Rules applied:** §1.3 (localize idioms), §9.3 (email phrases)

---

#### Example: "Thank you for your patience"

**Source:**
> "Thank you for your patience."

**❌ Bad:**
> "Дякую за вашу терплячість."

**Issues:**
- "Вашу терплячість" — calque + unnecessary "вашу"
- The whole phrase sounds translated

**✅ Good:**
> "Дякую за розуміння."

**Rules applied:** §1.3 (localize idioms)

The Ukrainian equivalent shifts from "patience" to "understanding" — that's the natural collocation. Word-for-word doesn't work.

---

## Contributing New Examples

When you encounter bad AI output in your work, capture it:

1. Save the **exact English source**
2. Save the **exact AI output** with the AI name/version if known
3. Identify **what's wrong** (consult `general.md` Section 3 for the rule catalog)
4. Write the **corrected version**
5. Submit a PR adding it to this file under the appropriate category

The most useful examples are ones where multiple AIs make the same mistake — those become important test cases.
