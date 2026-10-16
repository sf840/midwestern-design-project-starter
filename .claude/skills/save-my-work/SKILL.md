---
name: save-my-work
description: Back up the designer's changes to GitHub. Use when the designer says "save my work", "back it up", "I'm done for today" (after they agree to the offer), or asks to push or sync their changes.
---

# Save my work

Saves the project folder to GitHub for a designer who may never have used Git. Speak plainly: say "save" and "back up", and explain any Git word in one short phrase.

## Rules

- Only run when the designer asks, or says yes to your offer to save.
- Never rewrite history, force-push, delete branches or merge. Merging belongs to the designer or lead.
- If anything fails or the state is unclear, stop, say what happened in one or two plain sentences, and suggest one next step. Don't try several fixes in a row.

## Steps

1. **Check the state.** Run `git status` and `git branch --show-current`. If there is nothing to save, say so and stop.
2. **Show what is changing.** List the changed files in plain words (for example "2 decisions added, INDEX.md updated"). Flag anything that looks like it doesn't belong, such as a `.env` file, a large file or a raw transcript, and ask before including it.
3. **Pick the branch.**
   - Default: work on `main`.
   - If the designer mentioned branches or reviews, or `main` rejects the push, stop and ask the design lead how this team works. **Definition needed:** whether this team uses branches and pull requests.
4. **Save.** Stage the changes, commit with a short plain-English message that says what changed (not "update files"), then push. If the push is rejected because GitHub has newer work, run `git pull --rebase`, and if that conflicts, stop and tell the designer. Don't resolve conflicts silently.
5. **Sign-in problems.** If GitHub asks for sign-in, tell the designer to follow what the prompt says. It happens once. If it still fails, they should tell the design lead.
6. **Report what happened.** Say what was saved, the commit message you used, and that it is now on GitHub. Say plainly if anything was skipped or didn't go through.
