+++
aliases = ["voting-analysis", "ripe-ncc-irv", "comparison"]
title   = "RIPE NCC IRV vs. Simpler RIR Voting Models"
author  = "Better RIPE Team"
tags    = ["governance", "voting", "RIR"]
+++

## 1  Purpose

Evaluate the Instant-Runoff Voting (IRV) configuration used by the RIPE NCC, compare it with the current systems at ARIN and APNIC, and outline practical reform options.

---

## 2  Snapshot of Three RIR Voting Models

| Registry     | Ballot given to each voter                                                        | Counting rule                                        | Typical work for the voter                    | Transparency                                                                                          |
| ------------ | --------------------------------------------------------------------------------- | ---------------------------------------------------- | --------------------------------------------- | ----------------------------------------------------------------------------------------------------- |
| **RIPE NCC** | Rank all or some candidates                                                       | IRV — iterative elimination until one reaches 50 %+1 | Must decide rankings and understand transfers | Algorithm buried in Articles of Association; detailed round data not always published ([ripe.net][1]) |
| **ARIN**     | Tick up to *N* names (where *N* = open seats)                                     | Highest total approvals win (weighted by org count)  | Single screen; no ranking                     | Results list and vote weights published; no transfers ([arin.net][2])                                 |
| **APNIC**    | Cast the organisation’s vote-weight for as many candidates as desired (up to *N*) | Simple plurality; top totals win                     | Choose candidates; no ranking                 | BigPulse summary with raw totals; algorithm trivial ([apnic.net][3])                                  |

> **Key point** – ARIN and APNIC have *both abandoned pure single-vote plurality*, but they **still use flat “approval” or block ballots, far simpler than RIPE NCC’s multi-round IRV** and therefore easier for members to audit and predict.

---

## 3  RIPE NCC: Complexity in Practice

* **Legal basis** – Article 18.4 of the RIPE NCC Articles of Association mandates IRV for Executive-Board elections. ([ripe.net][1])
* **2023 data** – 2 366 weighted ballots were cast; published report confirms IRV with accumulating exhausted ballots. ([ripe.net][4])
* **Ballot exhaustion** – Nearly a quarter of ballots ceased to transfer before the final round (504 exhausted), meaning those members lost influence once their preferences ran out.
* **User burden** – Voters must understand that skipping ranks may waste influence, yet ranking all names may inadvertently help a less-preferred candidate.

---

## 4  Why ARIN & APNIC Feel “Fairer” to Members

1. **One screen, one click-set** – Voters tick names; no cognitive cost of ordering.
2. **No ballot exhaustion** – Every tick counts once, no transfers.
3. **Deterministic outcome** – Highest totals win; members can replicate the count from the published CSV.
4. **Auditability** – Both RIRs publish raw totals immediately; no hidden elimination rounds.

These advantages stem from the choice of *approval / block* counting, not from plurality. The methods still allow multiple winners and weighted ballots, yet avoid IRV’s cascading rules.

---

## 5  Recommendations for RIPE NCC Reform

* **Short term**

  * Publish machine-readable round-by-round files for every IRV contest.
  * Add an “exhausted-ballot” line in the public summary so members see representation loss.

* **Medium term**

  * Open a consultation on replacing IRV with a simpler **approval ballot** (ARIN style) or weighted block vote (APNIC style). Both meet majority legitimacy without transfers.
  * Trial the alternative method in a non-binding poll at the next GM to gauge acceptance.

* **Operational**

  * Eliminate pre-registration for online voters and keep polls open a full week, matching ARIN’s seven-day window.
  * Provide a plain-language voter guide explaining strategic effects of ranking vs. skipping.

---

## 6  Conclusion

IRV gives RIPE NCC a formal majority criterion, but at the cost of opacity and 20 %+ ballot exhaustion. ARIN and APNIC show that **simpler approval-style systems can deliver credible results with far less complexity**. A modest bylaws change could bring RIPE NCC in line with its peers while strengthening transparency and member trust.

[1]: https://www.ripe.net/documents/758/Proposed_Amendments_to_the_RIPE_NCC_Articles_of_Association.pdf?utm_source=chatgpt.com "[PDF] RIPE NCC Articles of Association – Proposed Amendments"
[2]: https://www.arin.net/participate/oversight/elections/instructions/ "Election Instructions - American Registry for Internet Numbers"
[3]: https://www.apnic.net/community/participate/elections/ec/voting/ "EC election voting procedures – APNIC"
[4]: https://www.ripe.net/membership/gm/meetings/may-2023/voting-report/?utm_source=chatgpt.com "Voting Report - RIPE NCC"
