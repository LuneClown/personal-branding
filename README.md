# 🧠 Personal Branding Skills for Claude

A set of skill files that help Claude AI write content that actually sounds like you — not like a generic AI.

Set up once. Claude learns your voice, audience, topics, and goals. Every skill in this repo reads that context automatically so you never repeat yourself.

---

## Who this is for

Anyone building a personal brand online — creators, writers, professionals, founders, freelancers. You don't need to be technical. If you can use Claude.ai, you can use this.

---

## How it works

1. You paste the skill instructions into a Claude Project
2. Claude asks you about yourself — tone, audience, topics, goals
3. It saves your answers to a context file
4. Every time you write content, Claude reads that file and writes in your voice

No setup fees. No accounts. Just Claude and a text file.

---

## Getting started

### Option A — Claude.ai Projects (recommended for most people)

1. Go to [claude.ai](https://claude.ai) and create a new **Project**
2. Open the Project Instructions box
3. Copy the contents of `CLAUDE.md` from this repo and paste it in
4. Start a new chat inside the Project and type: **"Let's get started"**
5. Claude will walk you through setup — takes about 5 minutes

That's it. Your preferences are saved to the Project and every conversation inside it will use them automatically.

### Option B — Claude Code (for developers)

```bash
git clone https://github.com/yourusername/personal-branding-skills
cd personal-branding-skills
```

Claude Code will detect `CLAUDE.md` automatically on startup.

---

## What's in this repo

```
personal-branding-skills/
│
├── CLAUDE.md                  ← Master instructions (paste this into Claude Projects)
├── user-context.md            ← Your personal context file (auto-generated during setup)
├── README.md                  ← You are here
│
└── skills/
    └── setup/
        └── SKILL.md           ← Run this first — creates your context file
```

### Skills available now

| Skill | What it does |
|-------|-------------|
| `setup` | Walks you through creating your personal context file. Run this first. |

### Coming soon

| Skill | What it does |
|-------|-------------|
| `social-content` | Write Twitter/X, LinkedIn, and Instagram posts in your voice |
| `bio-writer` | Write or refresh your profile bios across platforms |
| `content-strategy` | Plan your content calendar and topic mix |

---

## First time? Start here

Run the **setup** skill first. It will either:

- Ask you to paste existing content (a bio, old posts, about page) and draft your context from that
- Or walk you through a short Q&A if you're starting from scratch

Once setup is done, every other skill reads your context automatically. You won't be asked the same questions twice.

---

## Updating your context

Your brand evolves. Run setup again whenever:

- You switch platforms or niches
- Your goals change
- Your tone or audience shifts
- Something in your content feels off

---

## Contributing

This repo is early and actively being built. Contributions are welcome.

If you want to add a skill or improve an existing one:

1. Fork the repo
2. Create a new branch: `git checkout -b skill/your-skill-name`
3. Add your skill file at `skills/your-skill-name/SKILL.md`
4. Follow the format of existing skill files
5. Open a pull request with a short description of what the skill does and who it's for

Please keep skills focused on personal branding use cases. For questions, open an issue.

---

## License

MIT — use it, modify it, share it. Just keep the credit.
