---
name: contract-review
description: Review a PDF contract together in 5-page batches, check material terms against normal local practice, and give short page-by-page summaries focused only on genuine signing dealbreakers.
---

# Contract Review

Help the user understand a contract and make a practical signing decision. Remember: an AI review does not replace a licensed attorney for high-stakes or complex deals.

## Context and progress

- Identify the exact file, jurisdiction, business context, and signing deadline from the conversation or repo notes. Ask only for missing info that changes the assessment.
- Track the file version, last reviewed page, and unresolved cross-references. Start at page 1 for a new review; "next" continues after the last reviewed page.
- Never store private contract details inside this skill file.

## One batch per turn

1. Select the next 5 physical PDF pages (or remaining pages if fewer than 5 remain). Respect an explicit range if requested.
2. Extract text AND render images for only that range so you do not miss tables, prices, crossed-out terms, or signatures:

   ```bash
   pdftotext -f 1 -l 5 -layout "$contract_pdf" /tmp/contract-batch.txt
   pdftoppm -f 1 -l 5 -scale-to 2000 -png "$contract_pdf" /tmp/contract-page
   ```

3. Inspect both the rendered page images and the extracted text. Check original-language wording when a contract is bilingual.
4. Run up to 3 focused web searches for consequential terms or local market norms. Use generic queries without pasting private contract text or personal details.
5. Give the short assessment below, then stop. Continue only when the user asks for the next batch.

## Decision threshold

- Account for the cost of delay and the real deadline. Minor wording quirks, small ordinary fees, and negotiable preferences are not signing blockers.
- Do not say "needs clarification" or "send it back" unless the issue is serious enough that you would actually recommend delaying or refusing signature.
- If there is a genuine dealbreaker, state the clause, the likely consequence, and the smallest fix needed. Never hide a real risk just because a deadline is close.
- Limit conclusions to the pages reviewed so far. Carry forward any cross-references to later pages without guessing what they say.

## Output

- Lead with the page range and a clear verdict on whether this batch has a genuine signing blocker.
- Give 1 bullet per page with a short label and 1 or 2 plain-English sentences explaining what it says and why it matters.
- Put short source links next to market or legal comparisons.
- Skip long disclaimers, negotiation wish lists, or padding on cover/blank pages.
- Review only. Never edit the contract, email the other party, or sign anything unless explicitly asked.
