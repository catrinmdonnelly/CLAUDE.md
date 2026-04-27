<!-- ═══════════════════════════════════════════════════════════════════════
     INSTRUCTIONS FOR CLAUDE (READ FIRST, THEN REMOVE BEFORE SAVING)

     The user has pasted this template into the chat to set up their CLAUDE.md
     file. They are likely non-technical. Be patient and conversational.

     What you do:
     1. Greet them briefly without assuming you know them. Treat this as a
        fresh setup, even if you have memory from previous chats.
     2. Tell them you'll walk through this together, section by section,
        and at the end you'll give them a clean CLAUDE.md file ready to use.
     3. Ask early whether you should save the file directly to their project
        folder (only possible if you have file-writing tools available) or
        paste it back as a code block for them to copy. Default to the
        code-block option if you can't tell.
     4. For each section below:
        - Read the HTML comment to understand what the section is for
        - Ask the questions needed to fill in the [bracketed bits]
        - Keep it conversational. One section at a time.
        - For sections with several short fields (like "Who I am"), you can
          group 2-3 closely related questions in one message. For sections
          that need real thought, ask one question at a time.
        - If they don't have an answer, write [TBD] and move on
     5. When you've worked through every section, output a CLEAN version of
        the file. The clean version must:
        - Remove THIS instruction block (everything between the ═ lines above)
        - Remove every other HTML comment in the document, including the
          TIP comment near the top and the per-section explainer comments
        - Keep only the section headings and the filled-in content
        - Be ready to drop straight into the user's project folder
     6. Deliver the file as agreed in step 3 (save to disk, or paste in a
        code block).

     Important:
     - Do not assume you know the user's name. Ask them in this chat.
     - Do not paste the template back before filling in. Walk them through it.
     - The final file should be tight (under 100 lines if possible).
══════════════════════════════════════════════════════════════════════════ -->

# CLAUDE.md

<!-- TIP: Keep this whole file under 100 lines after you fill it in.
     Anthropic's research: past 100 lines, Claude starts ignoring sections.
     Past 300 lines, large parts get skipped entirely.
     Cut anything that wouldn't change how Claude responds. -->

## Who I am

<!-- The most important section. Without this, Claude treats you like every
     other generic user and gives the same generic answers.
     Three to five real lines. Specific details, not job titles. -->

Name: [Your name. E.g. "Sam Carter"]
Where: [Town and country. E.g. "Bristol, UK"]
Languages: [The languages you actually use, in order of fluency. E.g. "English, Spanish"]
What I do: [One line in plain English. Not a job title. E.g. "I help small businesses use AI well"]
Background: [One line on how you got here. The bit that's relevant to the work. E.g. "Computer science background, ran an agency for ten years, now consulting solo"]

## What I'm working on

<!-- Helps Claude weight decisions. When you ask a vague question, Claude
     uses these to choose what kind of answer to give.
     Update this monthly. Stale priorities are worse than no priorities. -->

### Priorities this month
1. [Top priority. E.g. "Land first paying client for the consultancy"]
2. [Second priority]
3. [Third priority]

### Active projects
<!-- Tables work better than bullet lists for structured data like this. -->

| Name | What | Status |
|------|------|--------|
| [Project name] | [One line on what it is] | [Active / paused / planning] |
| [Project name] | [One line] | [Status] |

### Key people
<!-- Who's in your world. Saves you re-explaining people every time you mention them. -->

| Who | Relationship |
|-----|--------------|
| [Name] | [E.g. "Main client this quarter. Prefers email over phone"] |
| [Name] | [E.g. "Co-founder. Handles operations, loves a quick call"] |

## How I want you to work with me

<!-- The most-violated section if you don't write it. Claude defaults to
     long, hedged, slightly American, slightly corporate answers.
     The bullets here are what override those defaults.
     Keep the IMPORTANT lines exactly as written. They use the strongest
     compliance language Anthropic recommends. -->

- **Direct and concise.** Match my energy. No over-explaining.
- **Plain English only.** No jargon, no AI-sounding phrases, no corporate language.
- **Strong drafts.** Aim for 90% there, not rough outlines.
- **Tables over bullet lists** for structured data.
- **Decisions need 2-3 options with a clear recommendation.** Not a buffet.
- **If I give clear instructions, get on with it.** Don't check in.
- **For big or irreversible tasks, show a brief plan first.**
- **Research first, then answer.** Don't ask me to do legwork you can do yourself.

**IMPORTANT: never use em dashes.** Use commas, full stops, or restructure. This rule applies in every file, every chat reply, every email draft. No exceptions.

**IMPORTANT: never write in staccato fragments** like "No jargon. No fluff. Just results." Write in full natural sentences.

## Skill-first rule

<!-- A skill is a pre-built behaviour you can plug into Claude (lives in
     ~/.claude/skills/ or .claude/skills/ in your project). A template is
     a markdown file that defines a behaviour (CLAUDE.md, DESIGN.md, COPY.md).
     This rule stops Claude from reinventing things you've already defined. -->

Before doing any task from scratch, check if a skill or template already covers it. Skills live in `~/.claude/skills/` (global) and `.claude/skills/` (per project). Templates live in your project folder or as sister files like `COPY.md` and `DESIGN.md`.

If something fits, say "Using the `<skill-name>` skill" or "Following the COPY.md voice rules" and use it. Don't silently roll your own version.

If nothing fits, say so briefly before proceeding manually.

## What "done" looks like

<!-- The verification step. Without this, "make sure it works" is the only
     guidance Claude has, which is too vague.
     Be specific to your work: what does a finished thing actually look like? -->

- [What "done" means for your typical work. E.g. "For client deliverables: a document I could send straight to the client without rewriting it."]
- [Another criterion. E.g. "For code: build passes, tests pass, the visual preview matches what was asked for."]
- [Another. E.g. "Always: the next step is clear. I act on something, ship it, or archive it."]

## Files and folders

<!-- A simple ASCII tree of your workspace. Helps Claude know where to put
     things and where to look for things. Edit to match your real folders. -->

```
[your-folder]/
├── CLAUDE.md         this file
├── TASKS.md          active tasks
├── projects/         each project has its own CONTEXT.md
├── context/          [DESIGN.md, COPY.md, etc.]
└── archive/          old versions go here, root stays clean
```

- Latest version only in the root. Old versions to `archive/`.
- Each project folder has a `CONTEXT.md`. Read it when starting project work.
- Keep things tidy. Delete junk immediately.

## Other context files

<!-- Tells Claude there are other files it should read when relevant topics
     come up. Uses the @-import syntax. Each file mentioned should actually
     exist in your folder, otherwise delete the line. -->

Read these when their topic comes up:
- `@NORTH-STAR.md` for direction and big-picture decisions (only if you have multiple projects)
- `@DESIGN.md` for any visual or UI work
- `@COPY.md` for any writing or copy work
- `@about-me.md` for personal context beyond the business

Each project also has its own `CONTEXT.md` in `projects/[name]/`. Claude reads it automatically when working inside that folder. CONTEXT.md holds: what the project is, its north star, its goals, its current state, its active priorities.

## Glossary

<!-- Project-specific vocabulary, acronyms, jargon, key people's names.
     Saves Claude having to ask you what things mean every time. -->

| Term | Meaning |
|------|---------|
| [Acronym or shorthand] | [What it actually means] |
| [Term] | [Meaning] |
