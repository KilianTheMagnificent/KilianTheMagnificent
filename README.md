# Andre Romero-Carey

**Software Developer** · St. Louis, MO · [Security & Verification Notes](https://kilianthemagnificent.github.io) · [LinkedIn](https://www.linkedin.com/in/andre-romerocarey)

Software developer working on input-validation libraries and machine-checked Lean 4 verification.

### Research notes & upstream issues

- **[Checking Untrusted AI-Authored Lean 4 Proofs](https://kilianthemagnificent.github.io/notes/lean4-verifier-adversarial-suite.html)** — 5-layer Lean 4 proof checker in `open-proofs` (proofs and tooling built with Claude Code and Codex), its 48 self-test checks (41 negative tamper/bypass checks plus 7 positive controls), scope limits, and machine-checked negation proofs applying a previously reported missing-parameter pattern (`#7327`, `#7434`, `#7493`) to 8 declarations across 7 Erdős problems in [`google-deepmind/formal-conjectures#7590`](https://github.com/google-deepmind/formal-conjectures/issues/7590) (open, 0 comments; 4 declarations later parameterized independently upstream in `#7946` and `#8015`).
- **[Screening Untrusted Office Inputs Before LLM Triage](https://kilianthemagnificent.github.io/notes/untrusted-office-input-defenses.html)** — Design and known limitations of `inbox-guard`: leading magic-byte header mismatches, Unicode `U+202E` & Windows/SMB filename spoofing, accounting-safe OWASP CSV neutralization, linear HTML5 comment and CSS declaration scanning, Plane-14 Unicode Tag (`U+E0000..U+E007F`) stripping, RFC 5322 sender spoofing, and randomized session-scoped PII tokenization.

### Security & verification focus

- **Checker & parser verification:** Building multi-layer checkers and local regression suites against proof-checker bypasses, disguised file headers, spreadsheet formula injection, and hidden HTML/CSS prompt-override markers.
- **Session-scoped data redaction:** Tokenizing structured personal and account identifiers locally before text crosses external API boundaries.
- **Human-gated review:** Staging untrusted external inputs behind explicit validation and human review rather than autonomous outbound actions.

### Public repositories

- **[`open-proofs`](https://github.com/KilianTheMagnificent/open-proofs)** — Lean 4 proofs and 5-layer proof checker built with Claude Code and Codex: **48 self-test checks** (41 negative tamper/bypass checks plus 7 positive controls in [`tests/run_adversarial.py`](https://github.com/KilianTheMagnificent/open-proofs/blob/main/tests/run_adversarial.py)), 131 verified proofs of textbook/test/solved statements (no open mathematical problems solved), and 11 negation certificates across 9 Erdős problems with unfiled local draft notes in [`outbox/`](https://github.com/KilianTheMagnificent/open-proofs/tree/main/outbox) and 1 filed upstream issue ([`#7590`](https://github.com/google-deepmind/formal-conjectures/issues/7590), currently open with 0 comments, covering 8 declarations across 7 Erdős problems).
- **[`inbox-guard`](https://github.com/KilianTheMagnificent/inbox-guard)** — Zero-dependency screening and randomized session-scoped regex PII tokenization for untrusted emails, attachments, and CSV exports, tested with `node:test` and CodeQL ([`SECURITY.md`](https://github.com/KilianTheMagnificent/inbox-guard/blob/main/SECURITY.md)).
