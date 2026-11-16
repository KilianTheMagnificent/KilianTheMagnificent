# Andre Romero-Carey

**Software Developer & Co-Founder ([Kestrel](https://meetkestrel.com) — pre-launch)** · St. Louis, MO · [Security & Verification Notes](https://kilianthemagnificent.github.io) · [LinkedIn](https://www.linkedin.com/in/andre-romerocarey)

I build Lean 4 proof-checking pipelines, input-screening libraries, and deterministic human-in-the-loop workflow software—including co-building **Kestrel** ([meetkestrel.com](https://meetkestrel.com) · [security design](https://meetkestrel.com/security)), an unincorporated, pre-launch prototype for back-office workflow automation.

### Research notes & upstream reports

- **[Checking Untrusted AI-Authored Lean 4 Proofs](https://kilianthemagnificent.github.io/notes/lean4-verifier-adversarial-suite.html)** — 5-layer Lean 4 proof checker in `open-proofs`, its 48-case soundness-bypass test suite, scope limits, and machine-checked negation proofs uncovering upstream misformalizations ([`google-deepmind/formal-conjectures#7590`](https://github.com/google-deepmind/formal-conjectures/issues/7590)).
- **[Screening Untrusted Office Inputs Before LLM Triage](https://kilianthemagnificent.github.io/notes/untrusted-office-input-defenses.html)** — Design and known limitations of `inbox-guard`: magic-byte header mismatches, Unicode `U+202E` & Windows/SMB filename spoofing, accounting-safe OWASP CSV neutralization, Plane-14 Unicode Tag (`U+E0000..U+E007F`) & entity-decoded CSS-hidden overrides, `From` display-name spoofing, and single-pass session-scoped PII tokenization.

### Security & verification focus

- **Adversarial verifier & parser hardening:** Building multi-layer checkers and local regression suites against soundness bypasses, disguised file headers, spreadsheet formula injection, and hidden prompt-override markers.
- **Deterministic data protection:** Tokenizing structured personal and account identifiers locally before text crosses external API boundaries, and keeping all arithmetic in deterministic code rather than language models.
- **Human-gated execution:** Staging outputs strictly as drafts for human review rather than autonomous outbound actions.

### Public repositories

- **[`open-proofs`](https://github.com/KilianTheMagnificent/open-proofs)** — 5-layer Lean 4 proof checker with a **48-case adversarial bypass test suite** ([`tests/run_adversarial.py`](https://github.com/KilianTheMagnificent/open-proofs/blob/main/tests/run_adversarial.py)), 131 machine-checked proofs (textbook, test, and solved research statements), and **11 upstream misformalization write-ups** ([`outbox/`](https://github.com/KilianTheMagnificent/open-proofs/tree/main/outbox)) on `google-deepmind/formal-conjectures`.
- **[`inbox-guard`](https://github.com/KilianTheMagnificent/inbox-guard)** — Zero-dependency screening and session-scoped regex PII tokenization for untrusted emails, attachments, and CSV exports, tested with `node:test` and CodeQL ([`SECURITY.md`](https://github.com/KilianTheMagnificent/inbox-guard/blob/main/SECURITY.md)).
- **[`flowclone-updates`](https://github.com/KilianTheMagnificent/flowclone-updates)** — Code-signed macOS release channel for FlowClone, a local-first macOS voice dictation app.
