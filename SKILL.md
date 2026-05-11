---
name: setup
description: "Use this skill first before any other skill in this repo. Activate when the user says 'set up my profile,' 'get started,' 'create my context,' 'update my brand info,' 'I'm new here,' or when no user-context.md file exists yet. This skill creates or updates the user-context.md file that all other skills depend on. Run this once at the start, and again whenever your brand, goals, or platforms change."
metadata:
  version: 1.0.0
---

# Setup — Personal Brand Context

You help users create and maintain their personal branding context file. This captures who they are, their tone, audience, topics, and goals — so every other skill in this repo can produce content that actually sounds like them, without asking the same questions over and over.

The context is stored at `user-context.md`.

---

## Step 1 — Check for existing context

First, check if `user-context.md` exists.

**If the file exists:**
Scan it for two things:
1. Are any fields blank (nothing written after the label)?
2. Does the word `Example:` still appear anywhere in the file?

If either is true, the file is **not fully filled in**. Tell the user:
> "I found your context file but some sections look incomplete. Want to fill in the gaps, or do a full refresh?"

Then go to Step 2.

If the file looks complete (no blank fields, no `Example:` lines remaining):
- Read it and summarize what you know about them in 3-4 sentences
- Ask: "Anything here that's changed or needs updating?"
- If yes — go to Step 2 for only the sections they want to update
- If no — skip to Step 4 and confirm everything is good

**If the file does not exist:**
Go to Step 2.

---

## Step 2 — Choose setup mode

Offer the user two options:

**Option A — Auto-draft (recommended)**
> "Paste in anything you already have — a bio, an about page, old social posts, a LinkedIn summary, anything. I'll read it and draft your context file from that. You just review and correct."

**Option B — Start from scratch**
> "No existing content? No problem. I'll ask you a few questions one section at a time. Takes about 5 minutes."

Most users who have been online for a while will have *something* — even a Twitter bio counts. Nudge them toward Option A if they're unsure.

---

## Step 3 — Gather information

### If auto-drafting (Option A)

1. Ask the user to paste their existing content
2. Read everything they share — bio, posts, about page, whatever they give you
3. Draft all sections of the context file based on what you find
4. Present the draft and say: "Here's what I put together. What needs correcting? What's missing or wrong?"
5. Iterate until they're happy
6. Go to Step 4

When auto-drafting, be conservative — only write what you can actually infer. Don't invent a tone or opinion that isn't supported by what they shared. Where you're unsure, leave the field blank and flag it:
> "I couldn't infer your strongest opinion from what you shared — what's a take you have that others might push back on?"

---

### If starting from scratch (Option B)

Walk through each section below one at a time. Don't ask everything at once — it feels like a form. Ask one section, get the answer, confirm it, move on.

For each section:
- Briefly explain what you're capturing and why it matters
- Ask the question
- When they answer, rephrase it back to confirm
- Then move to the next section

**Section order:**

#### 1. Who you are
- What do you want to be called publicly? (name, handle, or pen name)
- Finish this sentence: "I am a ___" — what's your one-line description?
- What's your niche? What space do you operate in?
- Which platforms are you actually active on right now?

#### 2. Your audience
- Who are you talking to? Describe your ideal reader or follower in plain terms.
- What can you assume they already know when they find you?
- Why do they follow you specifically — what do they come to you for?

#### 3. Your tone
- Ask them to pick words from this list that feel right, and delete the ones that don't:
  `casual / formal / conversational / authoritative / dry / warm / analytical / emotional / blunt / diplomatic / optimistic / skeptical / deadpan / enthusiastic / measured / provocative`
- What should your writing always feel like?
- What should it never feel like?
- Do you use humour? What kind?

#### 4. Your topics
- What are 3-5 topics you post about regularly?
- Any topics you want to stay away from?
- What's your strongest opinion in your niche — the thing you believe that others might push back on?

#### 5. Your goals
- What are you building toward with your personal brand?
- What does success look like 6 months from now?
- What do you want people to do after consuming your content?

#### 6. Content preferences
- How long do you like your social media posts?
- How often do you post?
- What formats do you like? What do you want to avoid?

#### 7. Things to always remember
- Any specific rules, phrases to avoid, brand terms, or quirks that don't fit anywhere else?

---

## Step 4 — Generate the context file

Once you have all the information, create `user-context.md` with this structure:

```markdown
# Personal Branding — User Context
*Last updated: [date]*

---

## Who you are

**Name:** [answer]

**One-line description:** [answer]

**Niche:** [answer]

**Current platforms:** [answer]

---

## Your audience

**Who you're talking to:** [answer]

**What they already know:** [answer]

**What they want from you:** [answer]

---

## Your tone

**Voice words:** [selected words]

**Always feel like:** [answer]

**Never feel like:** [answer]

**Humour:** [answer]

---

## Your topics

**Core topics:**
- [topic 1]
- [topic 2]
- [topic 3]

**Topics to avoid:** [answer]

**Strongest opinion:** [answer]

---

## Your goals

**Building toward:** [answer]

**Success in 6 months:** [answer]

**What you want people to do:** [answer]

---

## Content preferences

**Post length:** [answer]

**Posting frequency:** [answer]

**Formats you like:** [answer]

**Formats to avoid:** [answer]

---

## Things to always remember

- [rule or note 1]
- [rule or note 2]
```

---

## Step 5 — Confirm and save

Show the completed file to the user. Ask:
> "Does this feel like you? Anything that's off, missing, or needs rewording?"

Make any final adjustments. Then save to `user-context.md`.

After saving, tell the user:
> "You're all set. Every skill in this repo will now read this file automatically — you won't need to repeat any of this. If your brand, goals, or platforms change, just run setup again to update it."

Then list the skills that are now available to them:
- **social-content** — write Twitter/X, LinkedIn, and Instagram posts in your voice
- **bio-writer** — write or refresh your profile bios across platforms
- **content-strategy** — plan your content calendar and topic mix

---

## Tips for good output

- **Push for specifics** — "What's one post you wrote that really felt like you?" unlocks better tone data than asking about tone directly
- **Capture their actual words** — if they describe their audience in a specific phrase, use that exact phrase in the file
- **Don't over-polish** — the context file should sound like the user, not like a marketing document
- **Flag gaps honestly** — if a section is weak or vague, note it in the file so other skills know to ask for more detail
- **Skip what doesn't apply** — not everyone has a newsletter, a blog, or a strong opinion yet. Leave those blank rather than inventing something.
