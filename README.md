# CLAUDE.md

The master context file for working with Claude. Drop it in your project root and Claude reads it on every session.

This is one of a family of five templates that customise AI for the way you actually work.

| Template | What it covers | When to do it |
|----------|----------------|---------------|
| **[CLAUDE.md](https://github.com/catrinmdonnelly/CLAUDE.md)** (this repo) | Who you are, how you work, what's on your desk | First. Even if you do nothing else, this gets you 70% of the value |
| **[COPY.md](https://github.com/catrinmdonnelly/COPY.md)** | How things should sound. Voice + banned phrases | Second. Voice is the most-violated AI default |
| **[DESIGN.md](https://github.com/catrinmdonnelly/DESIGN.md)** | How things should look. Design tokens + banned aesthetics | Third. Only if you make visual things (websites, slides, social posts) |
| **[CONTEXT.md](https://github.com/catrinmdonnelly/CONTEXT.md)** | What each project is and where it's going | Per project, when you start working in a specific folder |
| **[NORTH-STAR.md](https://github.com/catrinmdonnelly/NORTH-STAR.md)** | Career-level direction. The why behind the projects | Last, and only if you have multiple businesses or want to think strategically |

You don't have to do all five. The minimum useful set is **CLAUDE.md + COPY.md**. Add the others as you need them.

They reference each other. Your CLAUDE.md tells AI to read the others when the relevant work comes up, so you do not have to think about which file is needed when.

## Why this exists

Without a CLAUDE.md, Claude has to guess who you are. Guessing is where the generic, hedged, slightly American responses come from. Three or four lines of real context, and you get a different assistant.

Most people either don't have a CLAUDE.md, or they have a 500-line one that Claude ignores past line 200. This template is the middle.

## Built on the work of others

This template isn't original. It's a synthesis of ideas from people who have thought hard about working well with AI. If anything in here is good, the credit goes to:

- **[Andrej Karpathy](https://github.com/forrestchang/andrej-karpathy-skills)** for the viral 65-line behavioural rules file (17K+ stars). The "tight is the goal" philosophy is his.
- **[Anthropic](https://code.claude.com/docs/en/best-practices)** for the official guidance, the "under 100 lines" finding, and the test: *"For each line, ask, would removing this cause Claude to make mistakes? If not, cut it."*
- **[HumanLayer](https://www.humanlayer.dev/blog/writing-a-good-claude-md)** for the WHAT/WHY/HOW frame and the warning that past 200 instructions, compliance drops fast.
- **[Garry Tan / gstack](https://github.com/garrytan/gstack)** for the production-grade example showing what strict writing style and commit standards look like.

What's mine is the synthesis: the HTML-comment guided pattern, the conversational walk-through, and the explicit pairing with DESIGN.md, COPY.md, CONTEXT.md, and NORTH-STAR.md as a coherent family.

## Who it's for

- **Solo founders** running a small business with AI as a real teammate
- **Consultants** who want their assistant to behave the same way across client projects
- **Small teams** sharing a single context file via git
- **Developers** who want behavioural rules separated from project context

## What's in this repo

| File | What |
|------|------|
| `CLAUDE.md` | The template. Walk through it with Claude (paste it into a chat) or fill it in by hand. |
| `README.md` | This file. |
| `LICENSE` | MIT. |

## How to use

There are two ways to use this template:

### Conversational (the easy way, for non-technical users)
1. Open `CLAUDE.md` in this repo, copy the whole file
2. Paste it into a Claude chat (claude.ai works fine)
3. Claude reads the meta-instruction at the top and walks you through it section by section
4. At the end, Claude gives you a clean version (comments stripped) ready to save as `CLAUDE.md` in your project folder

### Manual (for people comfortable with markdown)
1. Copy `CLAUDE.md` to your project folder
2. Open in any text editor
3. Read the HTML comments to understand each section, fill in the bracketed bits, delete the comments
4. Save

Either way: if you're using Claude Code, the file is loaded automatically from the project root. If you're using the desktop app or claude.ai, paste it into the project's "instructions" or "memory" field.

## The rules I learned from research

1. **Keep it under 100 lines** if you can, 300 absolute max. Past that, Claude starts ignoring sections.
2. **Cover what Claude can't infer from your code.** Skip anything readable from the codebase.
3. **Use IMPORTANT and YOU MUST** for the rules that actually matter. Anthropic explicitly endorses this.
4. **Bake in verification.** Tell Claude how to check its own work. "Run the tests" beats "make sure it works."
5. **Use progressive disclosure.** Reference sub-files (`@docs/testing.md`) so the main file stays lean.
6. **Treat it like code.** Review it when things go wrong. Update it when Claude makes a mistake.
7. **Hand-craft it.** Don't ship the raw `/init` output. It's a starting point, not a finished file.

## References

The best thinking I found while writing this:

- [Anthropic: Best Practices for Claude Code](https://code.claude.com/docs/en/best-practices): the official guidance
- [Anthropic: CLAUDE.md / memory](https://code.claude.com/docs/en/memory): file location hierarchy and progressive disclosure
- [Karpathy's CLAUDE.md](https://github.com/forrestchang/andrej-karpathy-skills/blob/main/CLAUDE.md): the 65-line behavioural file (17K+ stars)
- [HumanLayer: Writing a good CLAUDE.md](https://www.humanlayer.dev/blog/writing-a-good-claude-md): the WHAT/WHY/HOW frame and the 150-200 instruction ceiling
- [josix/awesome-claude-md](https://github.com/josix/awesome-claude-md): curated real-world examples
- [gstack's CLAUDE.md](https://github.com/garrytan/gstack/blob/main/CLAUDE.md): production example with strict writing style and commit standards
- [What Karpathy's CLAUDE.md Misses](https://www.masteringproducthq.com/p/what-karpathys-claudemd-misses-and): useful counterpoint for non-technical use cases

## Pair this with

- [CONTEXT.md](https://github.com/catrinmdonnelly/CONTEXT.md): per-project context file (one per project folder)
- [NORTH-STAR.md](https://github.com/catrinmdonnelly/NORTH-STAR.md): career-level direction (only if you have multiple projects)
- [DESIGN.md](https://github.com/catrinmdonnelly/DESIGN.md): design system in a single markdown file
- [COPY.md](https://github.com/catrinmdonnelly/COPY.md): brand voice and banned phrases

## License

MIT.

Made by Catrin Donnelly.
