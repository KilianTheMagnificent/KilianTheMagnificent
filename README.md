# Andre Romero-Carey

**Technical Co-Founder @ [Kestrel](https://meetkestrel.com)** · St. Louis, MO · [LinkedIn](https://www.linkedin.com/in/andre-romerocarey)

I build deterministic, human-in-the-loop operational software and verification tools—currently co-founding **Kestrel** ([meetkestrel.com](https://meetkestrel.com)), where we build lightweight back-office automation and workflow diagnostics for mid-market operating companies.

### Security & engineering principles

Because operational workflows touch untrusted business inboxes, attachments, and accounting exports, my engineering work focuses heavily on defensive boundaries:

- **Strict untrusted-input screening:** Validating attachments, magic bytes, CSV exports, and inbound emails against spoofing, formula injection, and hidden prompt-override payloads before downstream processing.
- **Deterministic data protection:** Redacting personal and account identifiers locally before text crosses external API boundaries, and keeping all financial arithmetic in deterministic code rather than language models.
- **Human-gated actions:** Staging outputs strictly as drafts for employee review rather than autonomous outbound execution.

### Public repositories

- **[`inbox-guard`](https://github.com/KilianTheMagnificent/inbox-guard)** — Zero-dependency defensive validation and deterministic PII redaction for untrusted business emails, attachments, and CSV exports.
- **[`open-proofs`](https://github.com/KilianTheMagnificent/open-proofs)** — Machine-checked Lean 4 formal verification proofs of open statements from `google-deepmind/formal-conjectures`, verified against a strict proof checker.
- **[`flowclone-updates`](https://github.com/KilianTheMagnificent/flowclone-updates)** — Official signed macOS release feed and update notes for FlowClone, a local-first macOS voice dictation app.
