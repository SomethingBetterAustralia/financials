# Financials

**The audit trail behind the Something Better Australia's [Financials page](https://somethingbetteraustralia.com/financials).**

While some political parties do the bare minimum (disclosing donations once a year and only if they're above the AEC threashhold), Something Better Australia believes Australians deserve full transparency. Every dollar in. Every dollar out. Every transaction visible. [Something Better Australia](https://somethingbetteraustralia.com) (SBA) is an evidence-led grassroots movement working toward Australia's next major political party, and committed to publishing every transaction, regularly, in a public repository where history can't be quietly rewritten. This is that repository.

## Project status: zero

There is no ledger in this repository yet. The pipeline that will produce it is not live.

## How to read the ledger

What will be published here, once live:

- **Every transaction**, each income and expense will be categorised.
- **A versioned history.** Corrections, reclassifications and late entries are made as new commits. `Git log` shows every change ever made and when it was made; `git diff` shows exactly what changed.
- **A regular cadence**, not real time — entries land after bank reconciliation (see the privacy section on lag).

The exact file format and schema are **TODO** — not yet decided. This section will be updated when the first export lands.

## Where the data comes from

The intended pipeline, described here as the model — none of it is live yet:

1. Donations and expenses flow through a bank account and a payment processor.
2. Transactions are reconciled in standard accounting software (likely Xero).
3. A categorised export is committed to this repository on a regular cadence.
4. The SBA website's [Financials page](https://somethingbetteraustralia.com/financials) reads from this repository — what you see there is what's here, not a separate copy.

Every step that can be open source will be. Every correction stays visible in version history — that visibility is the point.

## Privacy: what's on the ledger and what isn't

A public ledger is not a public donor list. The rules:

- **Individual donors are aggregated by default**, in line with the AEC's privacy regime. Donations will appear as a generic "individual donation" with no identifying information.
- **Donors who specifically request public acknowledgement may be named.** Consent first, always.
- **Founder contributions are named openly**, where the founder has consented.
- **There is a short lag** typically a few days between a transaction settling and appearing here, as bank reconciliation takes time. Slow and right beats fast and wrong.

## Contributing — verifying us, and the pipeline

This repo's first contribution is scrutiny. If anything here doesn't add up — a balance that doesn't sum, a category that looks wrong, a gap in the history — open an [issue](../../issues). Being checked is the point.

For engineers: the export pipeline that produces the ledger will be open source, built in public like everything else SBA ships. If transparent public-interest data is your thing, [discussions](../../discussions) is where that work gets shaped. <!-- TODO: link to the pipeline code once it exists; its location is not yet decided. -->

## Governance & licence

This repository is community-governed under the umbrella of [Something Better Australia](https://somethingbetteraustralia.com), owned by no party. Corrections are made in the open, via commits — never quiet edits. If we get something wrong, the fix and the mistake both stay on the record.

**Licence:** [MIT](LICENSE). Use it, fork it, audit it — that's the point. The published financial data itself is a factual public record rather than a creative work; the MIT licence covers this repository's contents and any code in it.

---

This ledger is one piece of a larger bet: that Australian politics can be done better — hopeful, evidence-led, and accountable. That bet is [Something Better Australia](https://somethingbetteraustralia.com). See the books in context on the [Financials page](https://somethingbetteraustralia.com/financials) — and come audit us.
