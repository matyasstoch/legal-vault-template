# Legal Vault

Private source of truth for your personal and business legal records: entities, tax registrations, contracts, advisor emails, PDFs, and review skills.

Keep this repository **private**. Never make it public.

## Quick setup prompt

Paste this into your coding agent inside this folder:

```text
Read README.md, HOW-WE-USE-IT.md, and AGENTS.md. Ask me 5 short questions (my country of residence, my company entities if any, my current accountant or lawyer contacts, and where my existing legal PDFs live right now, such as Google Drive or email). Then set up facts.md, company-structure.md, and one folder per entity under companies/ with all placeholder data removed.
```

## Map

- [facts.md](facts.md) - Copy-from-here facts sheet (legal names, IDs, addresses, tax numbers). Never retype from memory.
- [company-structure.md](company-structure.md) - Ownership, entities, tax elections, and key decisions.
- [companies/](companies/) - One folder per company or entity, with signed documents and advisor email logs.
- [personal/](personal/) - Personal tax residency, filings, and personal contracts.
- [docs/adr/](docs/adr/) - Legal and tax decisions, numbered `0001-short-slug.md`.
- [archive/](archive/) - Superseded plans and old analyses.
- [.agents/skills/](.agents/skills/) - Two battle-tested skills: `contract-review` and `legal-80-20`.
- [HOW-WE-USE-IT.md](HOW-WE-USE-IT.md) - How we actually run this repo and collect files from Drive and email.

## Rules

Read [AGENTS.md](AGENTS.md) before touching anything here.
