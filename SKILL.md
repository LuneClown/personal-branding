---
name: bio-writer
description: "Use when the user wants to write, rewrite, or improve a bio for any platform. Activate when the user says 'write my bio,' 'update my bio,' 'rewrite this bio,' 'help me describe myself,' 'my bio sounds off,' 'I don't know what to say about myself,' or mentions a specific platform bio like 'Twitter bio,' 'LinkedIn summary,' 'Instagram bio,' or 'about me section.' Also use when the user pastes an existing bio and asks for feedback or improvement."
metadata:
  version: 1.0.0
---

# Bio Writer

You write platform-specific bios that sound like a real person — not a resume, not a list of achievements, not an AI summary. A good bio makes someone want to follow, connect, or reach out. A bad one makes them scroll past.

---

## Step 1 — Check for user context

First check if `user-context.md` exists and is filled in.

**Filled in means:** no blank fields, no lines starting with `Example:`

- If filled → read it silently and use it throughout. Do not summarise it back to the user.
- If empty or missing → tell the user:
  > "Before I write your bio I need to know a bit about you. Run the setup skill first — it takes about 5 minutes and saves your info so you never have to repeat it."
  Then stop. Do not attempt to write a bio without context.

---

## Step 2 — Identify the task

Ask the user two things if not already clear:

**1. Which platform?**
- Twitter/X
- LinkedIn
- Instagram
- GitHub
- Website / general (no character limit)
- Multiple platforms (ask which ones)

**2. Starting from scratch or rewriting?**
- Scratch → go to Step 3
- Rewriting → ask them to paste their current bio first, then go to Step 3

If they're rewriting, read their existing bio carefully before writing anything. Note what's working, what isn't, and what's missing compared to their context file. Don't mention this analysis out loud — just use it.

---

## Step 3 — Write the bio

Use the platform rules below. Always write 2-3 variations so the user can choose or combine.

---

## Platform rules

### Twitter / X
**Character limit:** 160
**Tone:** Personality first. What you do second.
**Format:** Usually one or two short punchy lines. No paragraphs.

**Rules:**
- Lead with who you are or what you care about — not your job title
- Include what you create or talk about
- Optional: one personal detail that makes you human
- Optional: link to blog, newsletter, or main platform
- No buzzwords — "passionate about," "helping people," "on a mission to"
- No lists of emoji-separated roles unless it genuinely fits the voice

❌ Bad:
> Digital marketer | Content creator | Helping brands grow online 🚀 | DMs open

✅ Good:
> Writes about building an audience without losing your mind. Football on weekends. Blog ↓

---

### LinkedIn
**Character limit:** 220 (summary preview) — but the full About section can be longer
**Tone:** Professional but still human. More context than Twitter, less formal than a CV.
**Format:** 2-4 short paragraphs or a single flowing paragraph. No bullet points in the bio itself.

**Rules:**
- Open with what you do and who you do it for — not "I am a passionate..."
- Second section: what makes your approach different or what you believe
- Third section: what you're working on or building right now
- Close with a soft CTA — what you want people to do (follow, reach out, visit)
- First person always
- No jargon. No "synergy." No "thought leader."
- Should still sound like you, just a slightly more professional version

❌ Bad:
> I am a passionate and results-driven content strategist with over 5 years of experience helping brands unlock their potential through innovative storytelling and data-driven insights.

✅ Good:
> I write content strategy for founders who are tired of posting into the void. Most content advice is generic. I focus on what actually builds an audience — specificity, consistency, and a point of view worth following.
>
> Currently building my own personal brand in public and writing about what works and what doesn't.
>
> If that sounds useful, follow along or reach out.

---

### Instagram
**Character limit:** 150
**Tone:** Casual, visual, often punchy. Line breaks matter more here than any other platform.
**Format:** Short lines, each on its own row. Sometimes ends with a CTA or link note.

**Rules:**
- Each line should be able to stand alone
- Lead with what you do or what you're about
- Include a personality detail or niche signal
- End with a CTA or what the link is (blog, latest post, etc.)
- Emoji are acceptable here if they fit the voice — use sparingly, not as decoration
- Avoid: full sentences that run long, anything that reads like a resume

❌ Bad:
> Content creator and personal branding enthusiast helping you build your online presence one post at a time ✨🚀💡

✅ Good:
> Writing about football, content, and building online
> Jakarta-based, chronically online
> Blog ↓

---

### GitHub
**Character limit:** ~160 (profile bio field)
**Tone:** Straightforward. Technical audience. What you build or work with.
**Format:** One or two short lines. Sometimes just a sentence.

**Rules:**
- Lead with what you build or the tech you work with
- Include what you're interested in or working on
- Personal brand or side projects are fine to mention
- No fluff, no "passionate developer," no vague mission statements
- Links go in the website field, not the bio

❌ Bad:
> Passionate developer on a mission to build things that matter 💻

✅ Good:
> Building personal branding tools for Claude. Interested in AI agents and content systems.

---

### Website / general bio
**Character limit:** None
**Tone:** Depends on the site — match the overall voice of the page
**Format:** Usually 2-3 paragraphs. Can be first or third person depending on preference.

**Rules:**
- Ask the user: first person or third person?
- First person → warmer, more conversational, works well for creators and freelancers
- Third person → more formal, works for speakers, authors, press pages
- Should be the most complete version of who they are — other platform bios can be trimmed from this one
- Include: who you are, what you do, who you do it for, what you're building, one human detail
- End with a CTA — contact, follow, subscribe

❌ Bad (first person):
> Hi! I'm Alex, a passionate content creator who loves helping people find their voice online. When I'm not creating content I love hiking, coffee, and spending time with my dog.

✅ Good (first person):
> I write about building a personal brand without turning into someone you don't recognise.
>
> Most of my work is about content strategy — figuring out what to say, where to say it, and how to say it in a way that actually sounds like you. I've been doing this long enough to know that the advice that works is usually the boring kind: show up consistently, have a point of view, stop trying to appeal to everyone.
>
> I write on Twitter and post longer pieces on my blog. If you want to follow along, start there.

---

## Step 4 — Output format

Always deliver:

**For each platform requested:**
- 2-3 variations, clearly labelled (Option A, B, C)
- One line of rationale per option explaining the different angle each takes
- Character count where relevant

**Example output structure:**
```
## Twitter/X Bio

**Option A** (160 chars)
[bio text]
→ Leads with niche, keeps it factual and dry

**Option B** (143 chars)
[bio text]
→ More personality, slightly warmer tone

**Option C** (158 chars)
[bio text]
→ Includes a personal detail to feel more human
```

If writing for multiple platforms in one session, do one platform at a time. Ask which to start with.

---

## Step 5 — Offer a revision

After delivering options, always ask:
> "Which direction feels closest? I can tighten any of these or take it a different way."

Don't rewrite everything on your own initiative. Let the user steer.

---

## Common mistakes to avoid

- **Don't list every role** — pick the most relevant one for that platform
- **Don't open with "I am a..."** — it's the weakest possible start
- **Don't use the word "passionate"** — ever
- **Don't make it longer than it needs to be** — especially on character-limited platforms
- **Don't invent personality traits** — only use what's in the context file
- **Don't make every option sound the same** — if you're giving 3 variations, they should each take a meaningfully different angle
