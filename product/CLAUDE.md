# Product

Facts about the product that don't depend on a particular screen: what the words mean, what the stakeholders asked for, and what nobody has answered yet.

**Owner:** Definition needed.

## What's here

| Path | What it is | Read it when | Write to it when |
|---|---|---|---|
| `glossary.md` | Terms that are easy to confuse, with their meaning | Before writing sample content, labels, specs or copy | A term is defined, or turns out to mean something different |
| `open-questions.md` | Every unresolved product question, in one table | Before asking a stakeholder something (it may already be asked), and before designing around a gap | A question comes up, or gets answered |
| `prds/` | Verbatim copies of product requirement documents, one file each | Before writing a brief or spec | A PRD arrives or changes |
| `engineering-reviews/` | Verbatim copies of engineering's response to a PRD | Before writing a spec that depends on engineering | An engineering review arrives |

## Rules

- **Never invent a definition.** If a term's meaning isn't confirmed, write **Definition needed** in the glossary. Ask the designer.
- **Copies of PRDs are verbatim.** Paste the text as it is, with a header giving the source link and date. Don't summarize inside the copy. Write your summary in a design brief instead, and link back.
- **When a question is answered, record it in `../decisions/`,** then move the row to **Answered** in `open-questions.md` with the decision number.
- **Number questions once and never reuse a number.**
- Mark anything unconfirmed **Unknown** or **Definition needed**.

## Adding a PRD

1. Name the file after the feature: `prds/<feature-slug>.md`.
2. Start it with: source link, author, date copied, status.
3. Paste the text below that header, unchanged.
4. Offer to start a design brief from it (`../design/briefs/_template.md`).
