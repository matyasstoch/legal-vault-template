# Legal Vault Agent Rules

Private source of truth for business and personal legal records: entities, taxes, contracts, research, PDFs, and skills.

Keep this repository **private**. Never publish or share its contents outside authorized people.

## Response style

- Write short, plain answers. Lead with the outcome.
- Explain every legal or tax term in plain words the first time you use it. Never assume the reader knows the jargon.
- Avoid overthinking. Focus on moving fast and flagging only what actually matters.
- Use clear Markdown headings and bullet lists. Avoid walls of text.
- Keep emails to advisors or counterparties to the one thing you need to ask.
- Show email drafts as normal text while being reviewed. Put a draft in a copyable code block only after the owner approves it as final.

## Where things belong

- `facts.md` - Authoritative entity names, IDs, addresses, and advisors. Copy from here; never retype from memory.
- `company-structure.md` - Summary of entities, ownership, and tax setup.
- `companies/<entity>/` - Company records, signed PDFs (`documents/`), and advisor email logs (`email-log.md`). Read `companies/AGENTS.md`.
- `personal/` - Personal taxes and personal contracts.
- `docs/adr/` - Legal and tax decisions, numbered `0001-short-slug.md`. Never rewrite an old decision; add a new one.
- `archive/` - Superseded plans and analyses. Read `archive/AGENTS.md`.
- `.agents/skills/` - Reusable legal workflows (`contract-review`, `legal-80-20`).

## Records and evidence

- Separate documented facts, research, decisions, and unresolved questions. Cite supporting files or sources.
- Never invent dates, registration numbers, filing statuses, or legal citations.
- A missing file in this repo does not prove nothing was filed. Check email or ask the owner before claiming something was missed.
- Distinguish clearly between `draft`, `signed`, `submitted`, `completed`, and `superseded`. A completed payment does not prove a filing was submitted.
- Preserve signed originals and submission confirmations. Ask before deleting or replacing original documents.

## Editing and checks

- Stay within scope and preserve existing records.
- Review your diff and reconcile any changed status against real evidence before committing.
- Never commit bank logins, API keys, or passwords.
