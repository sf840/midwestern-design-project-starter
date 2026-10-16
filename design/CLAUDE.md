# Design: execution rules

These rules apply to any task that reads or writes this project's Figma files or the files in this folder. Follow them even when a request doesn't repeat them.

**Owner:** Definition needed.

## What's in this folder

| Path | What it is |
|---|---|
| `design-system.md` | Where this client's design system lives, and the rules for using it |
| `briefs/` | Design briefs: the design lead's point of view on a feature or workflow. Start from `briefs/_template.md`. |
| `specs/` | Specs: the field-by-field or screen-by-screen detail behind a design. Start from `specs/_template.md`. |

## Read before design work

1. `design-system.md`, to know which components, tokens and rules to use.
2. The design brief and spec for the feature, if they exist.
3. `../decisions/`, to avoid reopening settled questions. Read `../decisions/README.md` (the index) first.
4. `../product/glossary.md`, before writing any sample content or labels.

**Precedence:** documented decisions in Figma, especially on pages marked ready for development, override every written file here. When they disagree, tell the designer and offer to update the written file.

## Rules

### 1. Inspect before building
Before adding or modifying anything, read the actual components and existing structure of the frame you're working in. Never assume what exists; check first. If a request names a component, find the real instance in the file and use it. Don't approximate it with plain text, a generic shape or a new style.

### 2. Never invent new visual styles
Use only components, tokens and styles that already exist in the file or the design system. If something has no component to reuse, match the file's current conventions exactly (same type scale, spacing, corner radius, color tokens) instead of introducing anything new. If you can't find a reasonable match, stop and flag it.

### 3. Treat duplicates as drafts, not content
If you find two versions of the same section, don't fill in both or treat the leftover as real. Flag the duplicate and ask which one is final, unless the request says which to keep.

### 4. Don't collapse distinct fields into the same value
When two fields look alike but mean different things, give them different, realistic values. Never default several distinct fields to the same placeholder just because they share a component. Example: a "Start date" and a "Renewal date" should not both read "Jan 1".

### 5. Confirm what actually happened
After any task that touches Figma, say plainly:
- whether the change was written into the Figma file, or only analyzed or previewed;
- which elements had no existing component to reuse and had to be approximated.
Never leave this ambiguous.

### 6. Work in small, confirmable steps
For any task covering more than one card or section, stop after a reasonably sized chunk and summarize before continuing.

## Writing a brief or a spec

- Copy the template. Don't start from a blank file.
- Mark anything you don't know **Unknown** or **Definition needed**. Never fill it in with a plausible guess.
- Cite where each claim comes from (a call, a PRD, a research file, a decision number).
- Update the **Status and next step** table in a brief every time something changes. It's the first thing anyone reads.
- Link the decisions a brief produced.
