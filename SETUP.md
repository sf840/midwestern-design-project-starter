# Setup guide

A step-by-step guide to starting a new project from this template. It assumes you have never used Claude Code, Git or the terminal. If a step doesn't work, find it in **If something goes wrong** at the bottom.

Time needed: about 20 minutes the first time, 10 for later projects.

## Before you start (one time only)

You need three things. If you already have them, skip ahead.

1. **A personal GitHub account.** It's free: github.com. There is no design organization yet, so projects live in your own account.
2. **Claude Code.** Use the Claude desktop app and open its **Code** tab. Sign in with your work account.
3. **A Figma account** with access to the project's Figma file, if one exists yet.

You don't need to install Git or anything else. If Claude says something is missing, it will tell you what to do.

## Step 1: Make your copy of the template

1. Open the template's GitHub page in your browser: https://github.com/sf840/midwestern-design-project-starter. Make sure you're signed in to GitHub.
2. Click the green **Use this template** button, then **Create a new repository**.
3. **Owner:** your own GitHub account.
4. **Name:** the client and project, in lowercase with dashes. For example `acme-checkout-redesign`.
5. **Visibility:** **Private**. Always private. These files hold client information.
6. Click **Create repository**.

You now have your own copy. The template itself is never changed.

## Step 2: Get it onto your computer

1. Open Claude Code.
2. Say: *Clone my new repository into my Documents folder.* Then paste the page's link (copy it from your browser's address bar).
3. Claude will do it and tell you where the folder is.

If Claude asks you to sign in to GitHub, follow what it says. This happens once.

## Step 3: Open the project folder in Claude Code

1. In Claude Code, choose **Open folder** (or the folder icon) and pick the new folder, the one named after your project.
2. Check the folder name at the top. It should be your project's name, **not** `Documents`.

Claude Code must be opened in this folder, or it won't find its instructions.

## Step 4: Run the setup

1. Say **start**.
2. Claude will say what it's going to do and then ask a short list of questions, one at a time: client name, project name, who's on the team, where the Figma file and Linear project are, and so on.
3. Answer in plain words. **"I don't know yet" is a fine answer.** Claude writes "Unknown" and moves on.
4. Claude checks that Figma and Linear are connected. If one isn't, it will say so. That's normal. See **Connect Figma** or **Connect Linear** below, and then say "check Figma again" or "check Linear again".
5. At the end Claude tells you what it filled in and what is still unknown. Read it, and tell Claude anything that looks wrong.

## Step 5: Save your work

Say **save my work**. Claude backs the folder up to GitHub. From now on, say it whenever you finish for the day.

## Your first real session

Open Claude Code in the project folder and say what you're working on. Claude reads `INDEX.md`, tells you where the project stands and asks what's next. A few things worth saying out loud:

- *"Write up what we decided in that meeting."* Claude drafts a decision file for you to approve.
- *"Here's the kickoff call. Draft a design brief."* Claude uses the template in `design/briefs/`.
- *"What's still unknown on this project?"* Claude reads the open questions and `INDEX.md`.
- *"I'm done for today."* Claude offers to update `INDEX.md` and save your work.

## Connect Figma

1. In Claude Code, open **Settings** → **Connectors** (or **MCP servers**).
2. Find **Figma**, click **Connect** and sign in to Figma.
3. Back in the project, say *"check Figma again"*.

This folder already lists Figma in `.mcp.json`, so some setups connect on their own.

## Connect Linear

1. In Claude Code, open **Settings** → **Connectors** (or **MCP servers**).
2. Find **Linear**, click **Connect** and sign in to Linear.
3. Back in the project, say *"check Linear again"*.

## If your client uses Jira

Linear is the default for our own tasks. If the client's tasks are in Jira, ask your design lead before connecting it. Claude can read Jira but never writes to it. It drafts the text, and you paste it.

## If something goes wrong

| What happened | What to do |
|---|---|
| "Use this template" button isn't there | Sign in to GitHub first. If the page says "not found", the template may still be private. Ask Steven. |
| Claude can't clone the repository | Say *"sign me in to GitHub"* and follow what it says. If that doesn't work, tell your design lead. |
| Claude doesn't start the setup when you say "start" | Paste the fallback prompt from the top of `README.md`. |
| Claude seems to know nothing about the project | You probably opened the wrong folder. Open the project folder itself, not the one above it. |
| Figma or Linear isn't connected | See **Connect Figma** and **Connect Linear** above. Setup can finish without them. |
| You stopped halfway | Open Claude Code in the folder and say *"continue setup"*. |
| You made a mistake in an answer | Say what's wrong. Claude fixes it. |
| Anything else | Copy what Claude said, and send it to your design lead. |
