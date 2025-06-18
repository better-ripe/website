+++
aliases = ["posts", "articles", "blog", "showcase", "docs"]
title   = "State of the RIPE Atlas Project – June 2025"
author  = "Better RIPE Team"
tags    = ["index"]
+++

### Introduction

RIPE Atlas is the world’s largest open Internet-measurement network, with **“12 000-plus distributed probes”** collecting real-time data from thousands of vantage-points worldwide ([labs.ripe.net][1]). The service is run by the RIPE NCC (one of the five RIRs).

---

### Historical context

| Year | Milestone                                                                                                                                                        |
| ---- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 2010 | Project launched.                                                                                                                                                |
| 2015 | **Hadoop era** – two 119-node Cloudera CDH clusters (≈400 TB HDFS, 3.5 TB RAM, 80 Gbit/s) processed Atlas + RIPEstat data ([labs.ripe.net][2])                   |
| 2023 | Only *one* visible roadmap deliverable (“Renew data streaming”, finished Q1 2023) ([ripe.net][3])                                                                |
| 2024 | **Hybrid-storage migration** started: hot data on a new bare-metal cluster, cold data moved to AWS S3 → goal: cut 46 racks → 10 by end-2025 ([labs.ripe.net][4]) |
| 2025 | Q2 2025 plan focuses on UI renewal, full containerisation, probe-farm abuse limits and firmware packaging ([ripe.net][5])                                        |

---

### Code & firmware activity

*Firmware release cadence illustrates a clear gap followed by renewed work.*

| Version  | Date            | Gap (months) |
| -------- | --------------- | ------------ |
| 5080     | 23 Sep 2022     | –            |
| **5090** | **12 Jul 2024** | **22**       |
| 5100     | 24 Sep 2024     | 2            |
| 5110     | 03 Apr 2025     | 6            |

Source: RIPE Atlas firmware index ([atlas.ripe.net][6]).
The **22-month hiatus (Oct 2022 → Jul 2024)** was widely criticised on the Atlas mailing list; see the thread *“Meaning and the future of the project”* (6 Feb 2024) ([ripe.net][7]). Within five months of that discussion, the project shipped the first new firmware in almost two years and resumed a roughly quarterly release rhythm.

Similar stagnation affected the public GitHub tools (e.g. `ripe-atlas-tools`, `ripe-atlas-probe-measurements`). Commits restarted mid-2024 in parallel with the firmware work; maintainers are again triaging issues and PRs.

---

### Architecture documentation

Until 2024 most internal architecture was undocumented; contributors relied on a 2017 Labs post for high-level diagrams ([labs.ripe.net][8]). Following repeated community requests, RIPE NCC added:

* **Comprehensive docs site** (`atlas.ripe.net/docs/…`) with sections on controller/probe security, REST/streaming APIs and probe source code ([atlas.ripe.net][9]).
* Public firmware-build CI and cross-architecture packages (v5 HW, OpenWrt, Debian, CentOS) in 2024-2025 firmware releases ([atlas.ripe.net][10]).

---

### Backend evolution

Old: 400 TB on-prem Hadoop/HBase (2015 design) ([labs.ripe.net][2]).
New (2024-): **tiered object + bare-metal storage** – hot data local, ≥2021 data served from S3; full decommission of Hadoop cluster planned Aug 2024 ([labs.ripe.net][4]). Migration driven by rising DC costs and pushed forward after public feedback.

---

### Governance & planning

* **Quarterly plans** have been published since Q2 2022. 2023 showed *one* substantive Atlas work-item; the lightweight output bolstered claims of stagnation ([ripe.net][3]).
* **Q2 2025 plan** lists five active work-streams and is updated transparently on the RIPE site ([ripe.net][5]).

---

### Current status (-06 / 2025)

* **Network size:** >12 k probes, coverage concentrated in Europe; new distribution policy targets under-represented ASNs and regions ([labs.ripe.net][1]).
* **Codebase:** Firmware and tools again under active maintenance after 2022–2024 lull.
* **Backend:** Hadoop cluster being retired; hybrid object storage already serving pre-2021 data.
* **Docs:** Security, API and firmware build docs now public; deeper controller design still missing.
* **Community dialogue:** Mailing-list questions now receive responses; Roadmap items tracked quarterly.

---

### Take-aways

1. **Community pressure worked.** The February 2024 mailing-list critique directly preceded firmware, code and planning updates.
2. **Technical debt is being paid down.** Containerisation, CI, hybrid storage and anti-“probe-farm” controls are in progress.
3. **Still to fix:** sparse contributor guidelines, opaque controller internals, and limited probe diversity outside Europe.

The RIPE Atlas project is no longer “abandoned”, but sustained transparency and timely releases will determine whether the 2024-2025 momentum endures.

[1]: https://labs.ripe.net/author/ulka_athale_1/how-we-distribute-ripe-atlas-probes/ "How We Distribute RIPE Atlas Probes | RIPE Labs"
[2]: https://labs.ripe.net/author/paul_de_weerd/processing-ripe-atlas-and-ripestat-data-with-hadoop/ "Processing RIPE Atlas and RIPEstat Data with Hadoop | RIPE Labs"
[3]: https://www.ripe.net/publications/documentation/quarterly-planning/ripe-atlas/archived-plans/ "
      
        Archived Plans — RIPE Network Coordination Centre
      
    "
[4]: https://labs.ripe.net/author/felipe_victolla_silveira/reducing-the-ripe-nccs-data-centre-footprint/ "Reducing the RIPE NCC's Data Centre Footprint | RIPE Labs"
[5]: https://www.ripe.net/publications/documentation/quarterly-planning/ripe-atlas/ "
      
        RIPE Atlas Quarterly Planning — RIPE Network Coordination Centre
      
    "
[6]: https://atlas.ripe.net/docs/releases/firmware.html?utm_source=chatgpt.com "Probe Firmware Releases | Docs - RIPE Atlas"
[7]: https://www.ripe.net/ripe/mail/archives/ripe-atlas/2024-February/005698.html " [atlas] Meaning and the future of the project ripe-atlas — RIPE Network Coordination Centre"
[8]: https://labs.ripe.net/author/kistel/ripe-atlas-architecture-how-we-manage-our-probes/?utm_source=chatgpt.com "RIPE Atlas Architecture - How We Manage Our Probes"
[9]: https://atlas.ripe.net/docs/security/ "Security Disclosures | RIPE Atlas Documentation"
[10]: https://atlas.ripe.net/docs/releases/firmware_index/5090?utm_source=chatgpt.com "Release of probe firmware 5090 | RIPE Atlas Documentation"
