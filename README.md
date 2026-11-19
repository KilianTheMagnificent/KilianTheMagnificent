**Andre Romero-Carey** · St. Louis, MO · [Notes](https://kilianthemagnificent.github.io) · [LinkedIn](https://www.linkedin.com/in/andre-romerocarey)

I direct Claude Code and Codex to build tools for office data and machine-checked mathematics. I give the agents examples, decide what a correct result looks like, and ask for a check I can repeat without reading the implementation.

[Try the four-invoice check](https://github.com/KilianTheMagnificent/inbox-guard/blob/main/docs/checking-a-change.md). Two invoice memos start with arithmetic expressions. Preparing the CSV for import should add an apostrophe to those two cells and leave a refund of `-42.50` intact. The guide gives you the original file so you can compare every value yourself.

## Projects

- [inbox-guard](https://github.com/KilianTheMagnificent/inbox-guard) screens incoming mail, attachments and CSV exports before review. The invoice check above uses its CSV tool.
- [open-proofs](https://github.com/KilianTheMagnificent/open-proofs) checks AI-written mathematical proofs with Lean. I [reported eight statements](https://github.com/google-deepmind/formal-conjectures/issues/7590) in Google DeepMind’s Formal Conjectures project where the written answer ignored an input that could change the result.
- [agent-verification-playbook](https://github.com/KilianTheMagnificent/agent-verification-playbook) provides a zero-dependency AI-policy scanner, empirical-proof issue templates, and checklists for verifying AI-assisted open-source contributions.
- [wcp](https://github.com/KilianTheMagnificent/wcp) coordinates multiple coding agents in one Git repository using isolated worktrees, atomic leases, and hash-bound change bundles.
- [luck-filter](https://github.com/KilianTheMagnificent/luck-filter) is a zero-dependency Python backtest-overfitting and multiple-testing tool (DSR, PSR, PBO, White’s Reality Check, SPA) with an offline HTML companion.
- [orrery](https://github.com/KilianTheMagnificent/orrery) is an offline, local-first counterfactual decision instrument ([live demo](https://kilianthemagnificent.github.io/orrery/)) with zero dependencies and zero network calls.
- [broadsheet-obsidian-theme](https://github.com/KilianTheMagnificent/broadsheet-obsidian-theme) is an editorial newspaper theme for Obsidian in light (Day) and dark (Night Print) modes with offline font stacks.

## Outside contributions

- [modelcontextprotocol/inspector#2980](https://github.com/modelcontextprotocol/inspector/issues/2980) → merged in [PR #3016](https://github.com/modelcontextprotocol/inspector/pull/3016) — Tested `configs/demo.json` over stdio with Codex and suggested adding it as a minimal runnable example for the composable test server’s config reference; the maintainer included it in the merged documentation and credited the issue comment.
- [google-deepmind/formal-conjectures#7590](https://github.com/google-deepmind/formal-conjectures/issues/7590) — Reported eight statements where the written answer ignored a quantified parameter, backed by machine-checked Lean 4 negation proofs (built with Claude Code, disclosed in the report). Four were later updated upstream independently; a November 18 follow-up tracks the four remaining statements.

## Technical notes

- [Verifying AI-Assisted Contributions Without Reading Code](https://kilianthemagnificent.github.io/notes/verifying-ai-contributions-without-reading-code.html) walks through verifying AI-assisted open-source work with independent oracles across three case studies.
- [Checking Untrusted AI-Authored Lean 4 Proofs](https://kilianthemagnificent.github.io/notes/lean4-verifier-adversarial-suite.html) walks through the checks, what they can establish, and the evidence behind the report.
- [Screening Untrusted Office Inputs Before LLM Triage](https://kilianthemagnificent.github.io/notes/untrusted-office-input-defenses.html) explains which file, email and spreadsheet patterns the tool flags and what still needs human review.
