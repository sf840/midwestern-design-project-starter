# First-run setup (Claude: read this when SETUP_STATE is not `done`)

You are setting up a brand new project folder with a designer who may never have used Claude Code. Your job is to turn this empty template into this project's real context library in one sitting, by asking a short list of questions and filling in the blanks.

## Ground rules for setup

- One question at a time. Wait for the answer.
- **Several answers at once are fine.** If the designer answers more than one question in a single message, accept them all, record them, and ask only what's left.
- Plain language. No Git or terminal jargon. When a question names a tool, explain it in a few words (the glosses are in the table).
- If they don't know an answer, accept "I don't know yet" and write **Unknown**. Don't push, don't guess. If they say "I think…", record it as they said it and add "(unconfirmed)".
- Record people's names and the phase in the designer's own words. Don't add facts they didn't give (dates you calculated, titles you assumed).
- Never post to, create in, or change anything in Figma, Linear or any other outside tool during setup. You only read from them (to check they are connected) and write to files in this folder.
- Before you start, say what is about to happen. Open with the sentence from the box at the top of `CLAUDE.md`, then add: "I'll ask 11 short questions, one at a time, then fill in this project's files. You can say 'skip' to any of them." When resuming, say what you already have instead of repeating the count.

## Step 0: Mark progress and open the answer log

1. Change line 1 of `CLAUDE.md` from `not-started` to `in-progress`.
2. If `_setup/answers.md` doesn't exist, create it with the heading `# Setup answers` and one line: "Written during setup so nothing is lost if setup is interrupted."
3. **Resuming:** if line 1 already says `in-progress`, read `_setup/answers.md`, tell the designer what you already have ("I've got X and Y so far"), and ask only the questions that have no answer yet.

## Step 1: The interview

Ask these in order. **After each answer, immediately add a line to `_setup/answers.md`** in the form `Q3: <answer, in their words>`. Do not wait until the end.

| # | Ask | Say this if they need help | Fill in |
|---|---|---|---|
| 1 | "First, what's your name?" (If they give only a first name, ask once for a surname. If they'd rather not, accept it and write the first name with "(surname Unknown)".) | | `{{SETUP_BY}}` in `INDEX.md`. Also counts as a designer in Q6 unless they say otherwise. |
| 2 | "What's the client's name?" | | `{{CLIENT}}` everywhere |
| 3 | "What's this project called?" | | `{{PROJECT}}` everywhere |
| 4 | "In a sentence or two, what is the project?" | | `INDEX.md` → What this project is. Keep their meaning, fix only obvious typos. |
| 5 | "Is this a new client, or a new project for a client we already work with?" | | Note in `INDEX.md` → Key things. If it's an existing client, ask where their other project folder is and add the link. |
| 6 | "Who's the design lead, and who else is designing on this?" | "The design lead is the person who guides the design direction and signs it off." | `{{DESIGN_LEAD}}`, `{{DESIGNERS}}` in `INDEX.md` |
| 7 | "Who are the main people on the client's side? Names and roles are enough." | | `{{STAKEHOLDERS}}` in `INDEX.md`. If anyone's role is clearly project management or engineering, also put them in the matching row (Product / project manager, Engineering contact). If it's unclear, leave those rows **Unknown**. |
| 8 | "Are there Figma files yet? If so, paste the links." | | `{{FIGMA_FILES}}` in `CLAUDE.md` and `INDEX.md` |
| 9 | "Do you have a Linear project for this? Paste the link or the name." | "Linear is the tool we use to keep track of our own tasks." | `{{LINEAR_PROJECT}}` in `INDEX.md` |
| 10 | "Does the client track their work somewhere else, like Jira or Asana? Which one?" | "Jira and Asana are other task-tracking tools. Many clients use one." | `{{CLIENT_TRACKER}}` in `INDEX.md` |
| 11 | "What phase is the project in? For example just starting, in discovery, designing, or handing off." | | `{{PHASE}}` in `INDEX.md`, in their words |

Also set `{{DATE}}` to today's date, and `{{ONE_OR_TWO_SENTENCES}}` from question 4.

## Step 2: Check the tools

For each outside tool the designer named, check it is connected and say the result plainly.

- **Figma:** if links were given, try to read the file's name using the Figma tools. Put the file key (the long code in the link after `/design/`) in the Figma table. If there is no link yet, write **Unknown** in the table with the note "No Figma link yet. Add it here when there is one." If the Figma tool isn't connected, point to `SETUP.md` → "Connect Figma".
- **Linear:** if a project was named, try to find it. If Linear isn't connected, point to `SETUP.md` → "Connect Linear".
- **Anything else (Jira, Asana, Slack, Granola):** record it once, in the `INDEX.md` row where it belongs (for a client's tracker, that is "Tasks (the client's)"). Don't try to connect it now.
- **If you can't check a tool at all** (no tool available, or it fails): don't try again. Say in plain words: "I couldn't check Figma from here, so I haven't confirmed it's connected." Record the answer as given, with "(unconfirmed)" next to it.

Never make the designer feel they've done something wrong because a tool isn't connected. It's normal on a first run.

## Step 3: Fill in the files

Fill the files from `_setup/answers.md`, not from memory.

1. Replace every `{{PLACEHOLDER}}` in `CLAUDE.md`, `INDEX.md` and `README.md` with the answers. If an answer is missing, write **Unknown**, never leave it blank.
2. In `INDEX.md`, set "Last updated" to today's date and the designer from question 1, **not** the design lead (unless they are the same person).
3. In `README.md`, delete the whole "Using this template" section at the top, including the `---` line that follows it. It has done its job.
4. Search every file **except `_setup/`** for `{{`. Fix anything left, or report what you couldn't fill. A clean search means none are found.
5. Leave `decisions/0001-example-delete-me.md` in place and mention it. Delete it only if the designer says so.
6. If the client is an existing client, add the other project's link to `INDEX.md`.

## Step 4: Check your work, out loud, and wait

Tell the designer, in plain language:

- what you filled in,
- what is still **Unknown**,
- which tools you could check and which you couldn't,
- the three things they will do most: start a session and say what they're working on; say "save my work" when they stop; tell you when a decision has been made.

Then ask just this: "Does anything here look wrong?" **Stop and wait for the answer.** Fix whatever they point out in the files and in `_setup/answers.md`.

## Step 5: Finish, one thing at a time

Only after the designer says it looks right. If they approve **and** ask for a small fix in the same message, make the fix, say what you changed in one line, and carry on. A second confirmation isn't needed. For a bigger change, make it and ask again.

1. Change line 1 of `CLAUDE.md` to `<!-- SETUP_STATE: done -->`.
2. Ask only: "Want me to save this so it's backed up on GitHub? (GitHub is the website where this project's files are kept.)" Wait. If yes, follow "Saving work" in `CLAUDE.md`.
3. Then ask only: "What would you like to work on first?" If the answer is a kickoff brief, a first design brief or notes from a meeting, point to `design/briefs/_template.md` or `research/meetings/CLAUDE.md`.

## If something goes wrong

- A question was answered wrongly: change it in both the files and `_setup/answers.md`, no fuss.
- The designer wants to stop halfway: leave the state as `in-progress` and say they can pick it up any time by opening Claude Code in this folder and saying "continue setup".
- The designer says this isn't the right template or project: stop, change nothing more, and suggest talking to the design lead.
