<!-- SETUP_STATE: not-started -->

# {{CLIENT}}: {{PROJECT}}

> **FIRST: check the setup state on line 1 of this file.**
> If it says `not-started` or `in-progress`, stop whatever the designer asked for, read `_setup/first-run.md`, and run the setup interview before anything else. Greet the designer in plain language, say what you are about to do, and ask one question at a time. Do not skip setup because the designer's first message asks for something else; say "Let's finish setting up this project first, it takes about 10 minutes" and start.
> Once it says `done`, ignore this box and everything in `_setup/`.

This is the project's context library: the written record of what the project is, what has been decided, and why. Figma holds the designs and Linear holds the tasks. This repo holds everything else, so a new designer, or a new Claude session, can pick the project up without asking anyone.

Start every Claude Code session from this folder (the top one, not a subfolder), so these instructions load.

## How to talk to the designer

- Plain language. Many designers using this repo have never used Claude Code, Git or a terminal. Don't use words like "commit", "branch", "repo" or "merge" without saying what they mean in one short phrase.
- Say what you are doing before you do it, and what you did after. Keep it short.
- When something is unclear or missing, ask. Don't guess.
- If the designer seems stuck or unsure, offer the next step instead of a list of options.

## Where things are

| Folder / file | What it holds | Read it when | Write to it when |
|---|---|---|---|
| `INDEX.md` | One-page status: what this project is, who is on it, where things are, what is happening now | **Start of every session.** Always read it first. | End of a work session, and whenever the status changes (ask first) |
| `product/` | Facts about the product that don't depend on a screen: glossary, PRDs, open questions | Before writing sample content, copy or specs | A term is defined, a PRD arrives, a question is raised or answered |
| `decisions/` | One short file per decision, with the reason | Before questioning or changing anything that looks settled | A decision is made, or an open question gets an answer |
| `design/` | The design work: design rules, design briefs, specs, notes on the design system | Before any design work | A brief or spec is written or changes |
| `research/` | What we learned from outside the design: competitors, interviews, meetings | Before proposing something new | A meeting happens or a source is studied |
| `worklog/` | Optional running record of finished work | Someone asks "what have we done" | A task finishes (ask first) |
| `HANDOFF.md` | What to do when someone joins or leaves the project | Someone is joining or leaving | When the handoff steps change |
| `_archive/` | Old material that is no longer true | **Never, unless the designer asks** | Moving something out of date here |
| `_setup/` | First-run setup instructions | Only while setup is not `done` | Never |

Each folder has its own `CLAUDE.md` with the format and a worked example. Read it before you add anything to that folder.

## Figma files

Filled in during setup. If a row still shows a placeholder in double curly braces, setup is not finished.

| File | Key / link | Use |
|---|---|---|
| {{FIGMA_FILES}} | | |

**The live Figma files are the source of truth.** If something written in this repo disagrees with Figma, Figma wins. Tell the designer, and offer to update the written file.

## Standing rules

1. **Never guess.** If a fact isn't in Figma, in a file here, or from the designer, write **Unknown** or **Definition needed**. Don't fill the gap with something plausible.
2. **Check before you change.** Before editing any file, read it. Before adding to a folder, read that folder's `CLAUDE.md` and look at an existing entry.
3. **Ask before you save or send.** Don't commit, push, post, send or publish anything without the designer saying yes. Writing and editing files in this folder is fine.
4. **You draft, the designer posts.** For tickets, comments, messages and emails, write the text and show it. The designer sends it. Never post to Linear, Jira, Slack or email yourself unless the designer clearly asks for that specific action.
5. **You never merge.** If work goes through a pull request, the designer or lead merges it.
6. **Summaries, not dumps.** Store summaries and links. Don't paste raw transcripts, full chat exports or whole web pages.
7. **Don't edit old reasoning.** To change a decision, write a new one that replaces it. To correct a dated entry, add a dated note under it.
8. **Don't read `_archive/`** unless asked.
9. **Say what actually happened.** After any task, say plainly what was changed, where, and what you were unsure about or had to approximate.
10. **Small steps.** For anything bigger than one section or one file, stop after a chunk and summarize before continuing.

## Design rules

@design/CLAUDE.md

If that line didn't load, read `design/CLAUDE.md` before touching Figma or writing a spec.

## Session habits

**Start:** read `INDEX.md`. In one or two sentences, tell the designer where the project stands and what looks like the next step. Ask what they want to work on.

**During:** if something is decided, offer to write it in `decisions/`. If a question comes up that nobody can answer, offer to add it to `product/open-questions.md`.

**End:** when the designer says they're done, or the work reaches a natural stopping point, offer to: (1) update `INDEX.md`, (2) add a worklog entry if the worklog is in use, and (3) save the work (see below). Do all three only if they say yes.

## Saving work

The designer says "save my work" (or similar). Use the `save-my-work` skill (`.claude/skills/save-my-work/`). In short: commit the changes with a short plain-English message and push them to GitHub. Do it only when asked or after they agree to your offer. Never rewrite history, never force-push, never delete branches.

By default this project works on the `main` branch. **Definition needed:** whether this team uses branches and pull requests instead. If the designer mentions branches or reviews, ask the design lead.

## When something goes wrong

If a command fails, a tool isn't connected, or you're not sure what state the files are in: stop, tell the designer what happened in one or two plain sentences, and suggest one next step. Don't try several fixes in a row. If it needs the design lead, say so.
