# Decisions

One short file per decision, so anyone (and any Claude session) can answer "why is it like this?" without rereading every brief, and won't reopen settled questions.

**Owner:** Definition needed.

## When to read this folder

Before you question, change or contradict anything that looks established. Read `README.md` (the index) first, then open the files that match.

## When to write here

- A decision is made in a meeting, a review, or a conversation with the designer.
- An open question from `../product/open-questions.md` gets an answer. Add the decision, then move the question to **Answered** there.

**Offer to write a decision whenever you notice one being made.** Don't write it without the designer's yes.

## How to add one

1. Copy `_template.md`. See `0001-example-delete-me.md` for a filled-in one.
2. Take the next number. Name the file `NNNN-short-slug.md`, for example `0007-archive-instead-of-delete.md`.
3. Keep it to about 10 lines. If the reason was never recorded, write "Not recorded." Don't invent one.
4. Add a row to the index in `README.md`.

## Changing a decision

Don't edit the old reasoning. Set its **Status** to `Superseded by NNNN`, and write a new file that explains the change and says what it replaces.

## Format

```
# <Decision, stated as a sentence>

- **Date:** YYYY-MM-DD
- **Tickets:** links or keys, or None
- **Status:** Accepted

**Decision.** What was decided.

**Why.** The reason. "Not recorded." if unknown.

**Replaces.** NNNN, or None

**Applies to.** Where this holds.
```
