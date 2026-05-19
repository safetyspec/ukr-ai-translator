# Using This Reference in Claude Projects

[Claude Projects](https://www.anthropic.com/news/projects) lets you attach reference documents and custom instructions that apply to every conversation within a project. This is the cleanest way to use this reference.

## Setup (5 minutes)

### Step 1: Create a Project

1. Open [claude.ai](https://claude.ai)
2. Click **Projects** in the sidebar
3. Click **Create Project**
4. Name it something like "Ukrainian Localization" or "UK Translation"

### Step 2: Upload the Reference Doc

1. In your new project, find the **Project knowledge** section
2. Click **Add content**
3. Upload [`docs/general.md`](../general.md)
4. If you work in a specific domain (trucking, medical, etc.), also upload the relevant supplement from [`docs/domain-supplements/`](../domain-supplements/)

### Step 3: Add the System Prompt

Click **Edit project instructions** and paste this:

```
You are a professional Ukrainian localizer. You localize English content
into natural Ukrainian — you never translate word-for-word.

Before producing Ukrainian output:
1. Determine the content type (business / product UI / marketing /
   casual / social / creative / legal).
2. Apply the corresponding tone rules from Section 4 of the reference doc
   (ukrainian-localization-reference-general.md).
3. Determine target audience flavor (modern standard vs diaspora).
   Default to modern standard if unspecified.
4. Use the locked glossary from Section 7 for tech/SaaS terms.
5. Avoid Russifications listed in Section 3.
6. Run the Section 10 checklist mentally before each output.

Default to formal Ви unless context calls for ти. Use Правопис 2019
spelling. Adapt date/time/number conventions to the audience.

Output only the Ukrainian text. No explanations unless asked.
```

### Step 4: Test It

In a new chat within the project, paste a paragraph of English content and ask for Ukrainian translation. The output should noticeably better than vanilla Claude.

Try this test prompt:

> Translate this email to Ukrainian:
>
> "Hi Maria, just a friendly reminder that your subscription will expire on March 15. Please renew before then to avoid any interruption to your service. If you have any questions, reach out anytime."

You should get something like:

> Маріє, нагадуємо: підписка закінчується 15 березня. Поновіть її, щоб уникнути перерви в обслуговуванні. Виникнуть питання — пишіть будь-коли.

**Not** something like:

> ❌ Привіт Марія, просто дружнє нагадування, що ваша підписка закінчиться 15 березня. Будь ласка, поновіть її до того часу, щоб уникнути будь-якого перебою у вашому сервісі. Якщо у вас є будь-які питання, дотягніться у будь-який час.

## Tips

### Loading multiple supplements

If you work across multiple domains, you can upload several supplement docs to the same Project. The AI will apply general rules from `general.md` and override with domain-specific rules where the supplement diverges.

If supplements conflict with each other (unlikely, but possible), be explicit in your prompt about which domain context applies.

### Adding your own corrections

When you spot bad output, edit the reference doc locally and re-upload. Claude Projects will use the latest version.

For corrections you want to share with the community, see [CONTRIBUTING.md](../../CONTRIBUTING.md) for how to submit a PR.

### When to use Claude vs other tools

Claude tends to follow long-form reference documents more consistently than some other LLMs because of its larger effective context window and explicit instruction-following training. For complex localization with many rules, Claude Projects is the path of least resistance.

For lightweight quick-translation needs, the [system prompt template](./system-prompt-template.md) approach with any LLM works too.

## Known Limitations

- **Project knowledge has size limits.** The general doc is ~7,000 words, the trucking supplement is ~6,000 words. Most projects can fit both plus more. If you hit limits, prioritize the general doc.
- **The AI still makes mistakes.** Especially on edge cases (verb aspect in complex tenses, vocative for rare names, regional vocabulary). Native-speaker review is still recommended for high-stakes content.
- **Memory across chats** within a project works, but the reference doc is the anchor — don't rely solely on conversation history.

## Troubleshooting

**"The output still has Russisms / sounds translated"**

- Check that the reference doc is actually loaded in Project knowledge.
- Verify the system prompt was saved.
- Try a fresh chat (sometimes older chats in the project don't pick up new instructions).
- Paste the bad output back to Claude and ask: "Following the reference doc in Project knowledge, what's wrong with this Ukrainian and how should it be fixed?" — this forces Claude to consult the doc explicitly.

**"It ignores my domain glossary"**

- Make sure the domain supplement is also uploaded.
- In your prompt, explicitly state the domain: "This is trucking compliance content..." or "This is medical content..."

**"It's too formal / too casual"**

- Specify the content type in your prompt: "Write this as a casual email to a friend" or "Write this as formal business correspondence." The reference doc has tone rules per type — but the AI needs to know which type applies.
