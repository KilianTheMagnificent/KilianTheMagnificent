**Andre Romero-Carey** · St. Louis, MO · [Notes](https://kilianthemagnificent.github.io) · [LinkedIn](https://www.linkedin.com/in/andre-romerocarey)

I direct Claude Code and Codex to build tools for office data and machine-checked mathematics. I give the agents examples, decide what a correct result looks like, and ask for a check I can repeat without reading the implementation.

One example comes from an invoice export. A memo starting with `=2+3` should become text when the CSV is prepared for spreadsheet import. A refund of `-42.50` should keep its minus sign. You can see both kinds of input in the [inbox-guard CSV tests](https://github.com/KilianTheMagnificent/inbox-guard/blob/12614543d6ca2d993f0c3aec1b011ca5e10c4987/test/inbox-guard.test.mjs).

## Projects

- [`open-proofs`](https://github.com/KilianTheMagnificent/open-proofs) — Lean 4 proofs and 5-layer proof checker built with Claude Code and Codex: [48 self-test checks](https://github.com/KilianTheMagnificent/open-proofs/blob/main/tests/run_adversarial.py) (41 negative tamper/bypass checks + 7 positive controls), 131 verified proofs of textbook/test/solved statements (no open math problems solved), and 11 negation certificates across 9 Erdős problems (unfiled local drafts in [`outbox/`](https://github.com/KilianTheMagnificent/open-proofs/tree/main/outbox) + 1 filed issue [`google-deepmind/formal-conjectures#7590`](https://github.com/google-deepmind/formal-conjectures/issues/7590), covering 8 declarations across 7 Erdős problems).
- [`inbox-guard`](https://github.com/KilianTheMagnificent/inbox-guard) — Zero-dependency Node.js screening for untrusted emails, attachments, and CSV exports, plus randomized session-scoped regex PII tokenization, tested with `node:test` and CodeQL ([`SECURITY.md`](https://github.com/KilianTheMagnificent/inbox-guard/blob/main/SECURITY.md)).

## Technical notes

- [Checking Untrusted AI-Authored Lean 4 Proofs](https://kilianthemagnificent.github.io/notes/lean4-verifier-adversarial-suite.html) — Write-up on the 5-layer `open-proofs` checker, its 48 self-test checks, scope limits, and the negation proofs applying a previously reported missing-parameter pattern (`#7327`, `#7434`, `#7493`) to the 8 declarations in [`#7590`](https://github.com/google-deepmind/formal-conjectures/issues/7590) (4 later parameterized independently upstream in `#7946` and `#8015`).
- [Screening Untrusted Office Inputs Before LLM Triage](https://kilianthemagnificent.github.io/notes/untrusted-office-input-defenses.html) — Write-up on `inbox-guard` design and scope limits: leading magic-byte checks, Unicode `U+202E` and Windows/SMB filename spoofing, accounting-safe OWASP CSV neutralization, linear HTML5 comment and CSS declaration scanning, Plane-14 Unicode Tag (`U+E0000..U+E007F`) stripping, RFC 5322 sender spoofing, and randomized session-scoped PII tokenization.
