**Andre Romero-Carey** · St. Louis, MO · [Notes](https://kilianthemagnificent.github.io) · [LinkedIn](https://www.linkedin.com/in/andre-romerocarey)

I direct Claude Code and Codex to build tools for office data and machine-checked mathematics. I give the agents examples, decide what a correct result looks like, and ask for a check I can repeat without reading the implementation.

[Try the four-invoice check](https://github.com/KilianTheMagnificent/inbox-guard/blob/main/docs/checking-a-change.md). Two invoice memos start with arithmetic expressions. Preparing the CSV for import should add an apostrophe to those two cells and leave a refund of `-42.50` intact. The guide gives you the original file so you can compare every value yourself.

## Projects

- [inbox-guard](https://github.com/KilianTheMagnificent/inbox-guard) screens incoming mail, attachments and CSV exports before review. The invoice check above uses its CSV tool.
- [open-proofs](https://github.com/KilianTheMagnificent/open-proofs) checks AI-written mathematical proofs with Lean. I [reported eight statements](https://github.com/google-deepmind/formal-conjectures/issues/7590) in Google DeepMind’s Formal Conjectures project where the written answer ignored an input that could change the result.

## Technical notes

- [Checking Untrusted AI-Authored Lean 4 Proofs](https://kilianthemagnificent.github.io/notes/lean4-verifier-adversarial-suite.html) walks through the checks, what they can establish, and the evidence behind the report.
- [Screening Untrusted Office Inputs Before LLM Triage](https://kilianthemagnificent.github.io/notes/untrusted-office-input-defenses.html) explains which file, email and spreadsheet patterns the tool flags and what still needs human review.
