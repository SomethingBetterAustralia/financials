# aec-financials

**The public, versioned ledger of every Something Better Australia transaction — the audit trail behind the website's [Financials page](https://somethingbetteraustralia.com/financials).**

Every dollar in. Every dollar out. Every transaction visible. Australian political parties are only legally required to disclose donations above a threshold, once a year, in returns to the [Australian Electoral Commission](https://www.aec.gov.au) (AEC). [Something Better Australia](https://somethingbetteraustralia.com) (SBA) — an evidence-led grassroots movement working toward Australia's next major political party — has committed to the opposite extreme: publish every transaction, regularly, in a public repository whose history can't be quietly rewritten. This is that repository.

## Why this exists

The legal baseline for party finances in Australia is thin: an annual return to the AEC, disclosing only donations above a threshold, published long after the fact. Everything under the threshold — most of a grassroots movement's money — is invisible by default. SBA's commitment is voluntary and runs the other way: every dollar in and every dollar out, committed here on a regular cadence, so anyone can check the books at any time. The commit history is the audit trail.

## Project status: zero

There is no ledger in this repository yet. The pipeline that will produce it is not live.

That's honesty, not evasion. SBA is early, and the first entries land here once the pipeline is wired and the first transactions clear. Until then, what's on the record is the commitment itself — this README, versioned like everything that will follow it.

## How to read the ledger

What will be published here, once live:

- **Every transaction**, income and expense, categorised, with a running balance — so the books always sum, and you can check that they do.
- **A versioned history.** Corrections, reclassifications, and late entries are made as new commits, never as quiet edits. `git log` shows every change ever made and when it was made; `git diff` shows exactly what changed.
- **A regular cadence**, not real time — entries land after bank reconciliation (see the privacy section on lag).

The exact file format and schema are **TODO** — not yet decided. This section will be updated when the first export lands.

## Where the data comes from

The intended pipeline, described here as the model — none of it is live yet:

1. Donations and expenses flow through a bank account and a payment processor.
2. Transactions are reconciled in standard accounting software (Xero).
3. A categorised export is committed to this repository on a regular cadence.
4. The SBA website's [Financials page](https://somethingbetteraustralia.com/financials) reads from this repository — what you see there is what's here, not a separate copy.

Every step that can be open source will be. Every correction stays visible in version history — that visibility is the point.

## Privacy: what's on the ledger and what isn't

A public ledger is not a public donor list. The rules:

- **Individual donors are aggregated by default**, in line with the AEC's privacy regime. Most donations appear as a generic "individual donation" line with no identifying information.
- **Donors who specifically request public acknowledgement may be named.** Consent first, always.
- **Founder contributions are named openly**, where the founder has consented.
- **There is a short lag** — typically a few days — between a transaction settling and appearing here, because bank reconciliation takes time. Slow and right beats fast and wrong.

## What this is not

This is not a real-time feed — entries land after reconciliation, not the moment a card is charged. It is not a complete donor list — individuals are aggregated by design, for privacy. It is not financial advice. And it is not the AEC's official annual return — that is a separate, legal process. This repository is SBA's own voluntary, fuller-than-required transparency record.

## Contributing — verifying us, and the pipeline

This repo's first contribution is scrutiny. If anything here doesn't add up — a balance that doesn't sum, a category that looks wrong, a gap in the history — open an [issue](../../issues). Being checked is the point.

For engineers: the export pipeline that produces the ledger will be open source, built in public like everything else SBA ships. If transparent public-interest data is your thing, [discussions](../../discussions) is where that work gets shaped. <!-- TODO: link to the pipeline code once it exists; its location is not yet decided. -->

## Governance & licence

This repository is community-governed under the umbrella of [Something Better Australia](https://somethingbetteraustralia.com), owned by no party. Corrections are made in the open, via commits — never quiet edits. If we get something wrong, the fix and the mistake both stay on the record.

**Licence:** [MIT](LICENSE). Use it, fork it, audit it — that's the point. The published financial data itself is a factual public record rather than a creative work; the MIT licence covers this repository's contents and any code in it.

---

This ledger is one piece of a larger bet: that Australian politics can be done better — hopeful, evidence-led, and accountable. That bet is [Something Better Australia](https://somethingbetteraustralia.com). See the books in context on the [Financials page](https://somethingbetteraustralia.com/financials) — and come audit us.
