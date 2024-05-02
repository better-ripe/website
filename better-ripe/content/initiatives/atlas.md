+++
aliases = ["posts", "articles", "blog", "showcase", "docs"]
title = "RIPE Atlas Project state"
author = "Better RIPE Team"
tags = ["index"]
+++

## Introduction

The RIPE Atlas project is a global network of probes that measure Internet connectivity and reachability. The probes are distributed around the world and are hosted by volunteers. The project is operated by the RIPE NCC, one of the five Regional Internet Registries (RIRs) that manage the allocation of IP addresses and AS numbers.

## History of project

The RIPE Atlas project was launched in 2010. The project was created to provide a global, distributed, and open platform for Internet measurement. The project was designed to be easy to use and to provide a wide range of measurement capabilities. The project has grown rapidly since its launch, at 2023 there are 12081 probes connected.

## Project goals

The RIPE Atlas project has several goals. The project is designed to provide a global, distributed, and open platform for Internet measurement. The project is also designed to be easy to use and to provide a wide range of measurement capabilities. The project is intended to help improve the security, stability, and resilience of the Internet. The project is also intended to help improve the performance and reliability of the Internet.
But one of problems is that project doesn't add direct value to RIPE NCC members, so it's hard to justify the costs of the project. We believe with slight changes in project direction and more active community involvement we can make it more valuable and usable for the community.

## Project architecture

While source code is open, project architecture is not documented. This requires reverse engineering to understand how the project works. This is a significant barrier to entry for new contributors. We believe that documenting the project architecture would make it easier for new contributors to get involved and would help to grow the community around the project.

## Project state

[2015 Article](https://labs.ripe.net/author/paul_de_weerd/processing-ripe-atlas-and-ripestat-data-with-hadoop/)

- Cloudera's Hadoop distribution
- two clusters with 119 servers
- HDFS 400TB, 3.5TB RAM, and peak cluster bandwidth of 80Gbit/s (~32GB ram per server?)

## Initiative status

- Research

## Questions to answer

- Last 2 years there is a lot of complaints about the project abandonment, lack of updates, and communication with the community. What is the current state of the project?
- Some important questions in maillist left unanswered [link](https://www.ripe.net/ripe/mail/archives/ripe-atlas/2024-February/005698.html)
- Github repositories have no updates for 1-2 years (state at 1 May 2024) [link](https://github.com/RIPE-NCC/ripe-atlas-probe-measurements) [link](https://github.com/RIPE-NCC/ripe-atlas-tools)
- Github maintainers are not active, not reviewing PRs, not responding to issues
- No communication about development process with community (roadmap, plans, weekly updates)
- Project code is non-portable, visible legacy from Lantronix times, which limits the ability to run it on different platforms. With some upstreaming efforts we can get much greater coverage.
- Choice of platforms quite exotic, while much more common platforms are available.

## Discussion

Short discussion in telegram about opensource, community-funded projects, and how they should be managed, and accountability turned into argument, that certain parts of typical
opensource projects are not applicable to RIPE NCC projects, and that RIPE NCC is not a typical opensource project.
> what you should remember is that a lot of the software the NCC develops is not typical open source projects, it is software specifically made for the NCC

On [my](/team/nuclearcat) opinion if this is considered seriously and there is no intention to make process more transparent and project community-driven, then there is serious reason to fork Atlas initiative and make it community-driven, and opensource, and make it more valuable for the community and find proper sponsorship.
By this reason i am not willing to publish project roadmap proposal, as situation might turn into fair competition between community-driven project and RIPE NCC project.

References:
- [RIPE Atlas project](https://atlas.ripe.net/)
- [RIPE NCC](https://www.ripe.net/)
- [RIPE Atlas wikipedia page](https://en.wikipedia.org/wiki/RIPE_Atlas)
