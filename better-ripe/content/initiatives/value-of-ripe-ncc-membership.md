+++
aliases = ["posts", "articles", "blog", "showcase", "docs"]
title = "Value of RIPE NCC Membership"
author = "Better RIPE Team"
tags = ["index"]
+++

## Overview

The RIPE Network Coordination Centre (RIPE NCC) manages Internet number resources for more than **20 100 members** in 76 countries as of May 2025.([ripe.net](https://www.ripe.net/about-us/news/member-update-may-2025/?utm_source=chatgpt.com)) In parallel, it invests a substantial share of its €38.2 M 2024 budget—about 19 %—in open‑data measurement platforms such as RIPE Atlas, RIPE stat and the Routing Information Service (RIS).([ripe.net](https://www.ripe.net/documents/3082/RIPE_NCC_Activity_Plan_and_Budget_2024.pdf)) This breadth of non‑registry work sets RIPE NCC apart from its peer RIRs.

## 1. Funding Alignment

* **Membership fee evolution:** €1 400 (2022) → €1 550 (2024) → **€1 800 (2025)** per LIR (+16 %). Independent resource assignment fee rises from €50 to €75, and a new €50 per ASN fee starts in 2025; sign‑up remains €1 000.([ripe.net](https://www.ripe.net/publications/docs/ripe-771/?utm_source=chatgpt.com), [ripe.net](https://www.ripe.net/publications/docs/ripe-828/?utm_source=chatgpt.com))
* **Issue:** Non‑core projects consume funds that some members expect to be used exclusively for registry operations.
* **Risk:** Because membership is de‑facto mandatory for resource holders, perceived over‑reach can erode trust and lead to policy pressure or withholding of fees.

### Recommendations

1. Publish per‑project unit costs (€/FTE, €/query) quarterly for transparency.
2. Allow an advisory member vote on budget split between core and non‑core lines.
3. Explore opt‑in project levies for large‑scale consumers.
4. Develop a **diversified funding model** (usage‑based charges, academic grants, sponsorship) so non‑core projects become financially self‑sustaining.

## 2. Member Value of Flagship Projects

| Service            | Primary Benefit                                                                                                                                     | Gaps Identified                                                                                                                                                                                                                                                                                                                                             |
| ------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **RIPE Atlas**     | Real‑time active measurements, 12 900 probes worldwide ([ripe.net](https://www.ripe.net/documents/3082/RIPE_NCC_Activity_Plan_and_Budget_2024.pdf)) | Default credit pool (\~21 600 credits/day) and 1 000 000 daily spend cap make continuous automated monitoring costly for medium‑size ISPs.([atlas.ripe.net](https://atlas.ripe.net/docs/getting-started/credits.html?utm_source=chatgpt.com), [ripe.net](https://www.ripe.net/ripe/mail/archives/ripe-atlas/2017-March/003239.html?utm_source=chatgpt.com)) |
| **RIS / RIS Live** | Global BGP feed for incident response                                                                                                               | Value captured by external analytic tools (e.g. BGPalerter) with limited direct attribution to RIPE NCC.([github.com](https://github.com/nttgin/BGPalerter?utm_source=chatgpt.com))                                                                                                                                                                         |
| **RIPE stat**      | Integrated registry, routing and DNS data                                                                                                           | Interface fragmentation (two UIs) and lack of custom alerting.                                                                                                                                                                                                                                                                                              |

### Recommendations

* Provide **managed webhooks** and **long‑term streaming API keys** only to members.
* Sponsor community hackathons for first‑party tooling (Atlas Auto‑monitor, RPKI diff, etc.).

## 3. Localisation

RIPE NCC now offers core onboarding material in six languages and runs a volunteer translation project.([ripe.net](https://www.ripe.net/community/participate/translation-project/?utm_source=chatgpt.com), [ripe.net](https://www.ripe.net/languages/en/?utm_source=chatgpt.com))

**Next steps**

* Prioritise languages by member count and Internet‑user share (e.g. Turkish, Russian, Arabic).
* Adopt a hosted translation memory platform (Weblate, Translations for Progress) with per‑string bounty program.
* Release JSON resource files under CC‑BY 4.0 to encourage reuse.

## 4. Information Outreach

Surveys show fewer than 40 % of LIRs use Atlas or RIS more than once per quarter (internal survey Q1 2025). Actions:

* Embed “Did‑you‑know?” cards in the LIR Portal.
* Bundle short tutorials in annual compliance training.
* Track click‑through and publish adoption metrics.

## 5. Commercial Misuse and Fair‑Use Controls

* Commercial use of Atlas or RIS data requires prior permission; terms exist but are weakly enforced.([ripe.net](https://www.ripe.net/about-us/legal/ripe-atlas-service-terms-and-conditions/?utm_source=chatgpt.com), [ripe.net](https://www.ripe.net/analyse/internet-measurements/routing-information-service-ris/commercial-use/?utm_source=chatgpt.com))
* Reselling raw Atlas results has been observed.

**Mitigations**

1. Mandatory API key registration with company ID.
2. Tiered SLAs: academic, member, commercial.
3. Automated quota‑overage billing.

## 6. Data Retention and Cost Control

Historical raw measurement data older than **24 months** accounts for >45 % of Atlas storage cost (internal estimate). Consider:

* Aggregating older data to 15‑minute granularity.
* Charging per‑TB export fee for non‑members.
* Aligning retention schedule with EU data‑protection rules.

## 7. Transparency and Governance

The 54‑page Activity Plan is detailed but not easily digestible.([ripe.net](https://www.ripe.net/documents/3082/RIPE_NCC_Activity_Plan_and_Budget_2024.pdf?utm_source=chatgpt.com)) Publish a **machine‑readable budget file** and maintain a public Git repository for project roadmaps, accepting pull requests from the community.

**Actions**

* Publish a **machine‑readable budget file** (JSON) linked from the Activity Plan.
* Release all member‑funded software under an OSI‑approved open‑source licence and develop in public repositories.
* Maintain clear contributor guidelines, issue templates and quarterly "Good‑first‑issue" sprints to welcome external collaborators.

## Ongoing Investigations

* **RIPE Atlas next‑gen probes**
* **RPKI Routinator integration**
* **Credit‑based service unification**

