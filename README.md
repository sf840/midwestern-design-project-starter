# Using this template

> **Delete this section after setup.** Claude does it for you in the last step.

This is a starter folder for a design project's written record: what the project is, what has been decided and why, what we've learned, and what's happening now. It's built to be read by Claude Code as much as by people. You open it in Claude Code, Claude asks you a few questions, and the folder becomes your project's.

**You don't need to know Git, GitHub or the terminal.** Claude handles those.

### Start in five steps

1. **Make your copy.** On this page, click the green **Use this template** button, then **Create a new repository**. Leave the owner as your own GitHub account. Name it after the client and project (for example `acme-checkout-redesign`). Choose **Private**. Click **Create repository**.
2. **Get it onto your computer.** Open Claude Code and say: *"Clone my new repository into my Documents folder. Here's the link:"* and paste the page's link.
3. **Open the folder.** In Claude Code, open the new folder (the one named after your project). It has to be this folder, not the one above it.
4. **Say "start".** Claude will ask a short list of questions about the project and fill everything in. It takes about 10 minutes. Answer "I don't know yet" whenever that's true.
5. **Say "save my work".** Claude backs it up to GitHub.

The longer guide, with what to do if a step doesn't work, is in [`SETUP.md`](SETUP.md).

### If "start" doesn't start the setup

Paste this into Claude Code:

> Read `CLAUDE.md` and `_setup/first-run.md` in this folder, then run the first-run setup with me. Ask me one question at a time, in plain language.

---

# {{CLIENT}}: {{PROJECT}}

{{ONE_OR_TWO_SENTENCES}}

This folder is the project's written record. Start Claude Code sessions from here, and Claude will read `CLAUDE.md` and `INDEX.md` first.

| Folder / file | What's in it |
|---|---|
| [`INDEX.md`](INDEX.md) | One-page status. Read this first. |
| [`CLAUDE.md`](CLAUDE.md) | Instructions for Claude: where things are and the standing rules |
| [`product/`](product/) | Glossary, PRDs and open questions |
| [`decisions/`](decisions/README.md) | One short file per decision, with the reason |
| [`design/`](design/) | Design rules, design briefs and specs |
| [`research/`](research/README.md) | What we've learned from outside the design: competitors, interviews, meetings |
| [`worklog/`](worklog/README.md) | Optional record of finished work |
| [`HANDOFF.md`](HANDOFF.md) | What to do when someone joins or leaves |

**Source of truth:** the live Figma files. If something here disagrees with Figma, Figma wins.
