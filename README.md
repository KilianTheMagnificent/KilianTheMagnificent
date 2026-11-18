**Andre Romero-Carey** · St. Louis, MO · [Notes](https://kilianthemagnificent.github.io) · [LinkedIn](https://www.linkedin.com/in/andre-romerocarey)

I direct Claude Code and Codex to build tools for office data and machine-checked mathematics. I give the agents examples, decide what a correct result looks like, and ask for a check I can repeat without reading the implementation.

[Try the four-invoice check](https://github.com/KilianTheMagnificent/inbox-guard/blob/main/docs/checking-a-change.md). Two invoice memos start with arithmetic expressions. Preparing the CSV for import should add an apostrophe to those two cells and leave a refund of `-42.50` intact. The guide gives you the original file so you can compare every value yourself.

## Projects

- [inbox-guard](https://github.com/KilianTheMagnificent/inbox-guard) screens incoming mail, attachments and CSV exports before review. The invoice check above uses its CSV tool.
- [open-proofs](https://github.com/KilianTheMagnificent/open-proofs) checks AI-written mathematical proofs with Lean. I [reported eight statements](https://github.com/google-deepmind/formal-conjectures/issues/7590) in Google DeepMind’s Formal Conjectures project where the written answer ignored an input that could change the result.

## Outside contributions

- [modelcontextprotocol/inspector#2980](https://github.com/modelcontextprotocol/inspector/issues/2980) → merged in [PR #3016](https://github.com/modelcontextprotocol/inspector/pull/3016) — Tested `configs/demo.json` over stdio with Codex and suggested adding it as a minimal runnable example for the composable test server’s config reference; the maintainer included it in the merged documentation and credited the issue comment.
- [google-deepmind/formal-conjectures#7590](https://github.com/google-deepmind/formal-conjectures/issues/7590) — Reported eight statements where the written answer ignored a quantified parameter, backed by machine-checked Lean 4 negation proofs (built with Claude Code, disclosed in the report). Four were later updated upstream independently; a November 18 follow-up tracks the four remaining statements.

## Technical notes

- [Checking Untrusted AI-Authored Lean 4 Proofs](https://kilianthemagnificent.github.io/notes/lean4-verifier-adversarial-suite.html) walks through the checks, what they can establish, and the evidence behind the report.
- [Screening Untrusted Office Inputs Before LLM Triage](https://kilianthemagnificent.github.io/notes/untrusted-office-input-defenses.html) explains which file, email and spreadsheet patterns the tool flags and what still needs human review.
