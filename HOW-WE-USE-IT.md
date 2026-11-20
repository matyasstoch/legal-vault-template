# How We Use Legal Vault

Legal paperwork usually ends up scattered across five email threads, random Google Drive folders, and downloads from two years ago. Putting every entity, contract, and filing into one private Git repo changes everything once you work with coding agents.

Important note: an AI agent is not your lawyer or CPA. Use it to organize records, spot real dealbreakers fast, and prepare sharp questions for your actual lawyer or accountant.

## Our day-to-day workflow

### 1. Gather your existing files first
Use your agent (with Gmail or Google Drive connectors, or by pointing it at a local Downloads folder) to pull every incorporation certificate, tax ID letter, signed contract, and engagement letter into `companies/<entity>/documents/`.

Rename files clearly with dates: `YYYY-MM-DD-short-description.pdf`.

### 2. Fill out `facts.md` once
Put your exact legal entity names, registration numbers, tax IDs, registered address, and advisor emails into `facts.md`. Every time you fill a form, write a contract, or draft an email, the agent copies from `facts.md` instead of guessing.

### 3. Review contracts in 5-page batches
Use `.agents/skills/contract-review/SKILL.md` whenever someone sends you a PDF contract. Instead of dumping a 40-page PDF into one prompt (where models miss tables, fine print, and signatures), the skill renders 5 pages at a time as both text and images, checks key terms against normal market practice, and flags only genuine signing dealbreakers.

### 4. Stay 80/20 on legal overhead
Use `.agents/skills/legal-80-20/SKILL.md` to stop overthinking standard paperwork. Legal and tax work is overhead. Use standard setups, run one focused check for serious risks, sign, and get back to building.

### 5. Draft short advisor emails, approve before sending
When you need your accountant or lawyer, ask the agent to bundle all open questions into one short email. Keep drafts as plain text while reviewing. Only copy or send after you explicitly approve the final wording.

### 6. Archive superseded plans
Never delete old plans or mix them with active tasks. Move replaced plans to `archive/` with a superseded banner pointing to the current file so agents never treat old checkboxes as live todos.
