+++
aliases = ["posts", "articles", "blog", "voting", "unfairness"]
title = "RIPE NCC EB voting system analysis"
author = "Better RIPE Team"
tags = ["index"]
+++

# Why We Open This Topic

Many of us have been following the recent RIPE NCC General Meeting elections and the discussions around Instant Runoff Voting (IRV). I've heard many conspiracy theories about the IRV system and how it is unfair. I decided to write this report to highlight the pros and cons of the IRV system and compare it with other RIRs' voting systems.

# Introduction

The current Instant Runoff Voting (IRV) system in use is quite complex and has many options, making it hard for the community to understand how the system works. This report aims to provide an overview of the IRV system, its key issues, and a case study of the General Meeting 2023 to illustrate its flaws. Additionally, it will raise critical questions for consideration and propose a call to action for reform.

# History of the RIPE NCC EB Voting

As mentioned at [RIPE-176](https://www.ripe.net/publications/docs/ripe-176/), the initial version of the RIPE NCC bylaws used a simple majority voting system, where the number of votes depended on the size of the membership. This is similar to the systems used by ARIN and APNIC. The voting system was changed to IRV at the October 2009 General Meeting in [RIPE-487](https://www.ripe.net/membership/meetings/gm/meetings/october-2009/general-meeting-minutes/), with the following explanation from the meeting minutes:

> Jochem explained that changes to the Articles of Association would be needed to support e-voting and also that this was a good time to introduce any housekeeping changes that were necessary.

It is interesting to highlight that the voting system was changed to support e-voting, but it is not clear why IRV was chosen or if there was any public discussion or consultation about the voting system. In my personal opinion, under the pretext of e-voting, the system was changed to IRV, which is more complex and less transparent to the average voter and introduces unfairness into the system.

Initially, voting was done in person, so two weeks prior registration was required as RIPE NCC needed to provide appropriately sized facilities for the meeting. Currently, voting is done online, so we can logically assume that there is no need for registration. The duration of the voting was also dependent on the in-person meeting, so it was limited to just one day, which is no longer necessary with the introduction of e-voting.

# Instant Runoff Voting System and RIPE Choices Overview

IRV does not have a strictly defined configuration and can be implemented in various ways. Generally, the system allows voters to rank candidates in order of preference, with the candidate receiving the least number of first-preference votes being eliminated in each round. Certain versions of the IRV system are immune to various voting manipulations, such as the spoiler effect and strategic voting, but the system used by RIPE NCC is not immune to certain manipulations due to configuration choices.

One example of such vulnerability is the "strategic voting" problem, where voters can follow a specific voting strategy to:
1. Increase the chances of their preferred candidates winning. For example, voters from a particular country might vote for a candidate from the same country, then for a candidate from the same region, and then for a candidate of the same nationality. This strategy is called the "lesser evil" strategy.
2. Decrease the chances of their least preferred candidates winning. For example, if there is a candidate offering changes in policies not liked by the voter, the voter might build a strategy to lower the chances of such a candidate winning (turkey-raising/pushover/pied piper strategy).

The existence of such strategies raises questions about the fairness of the system and whether it truly represents the community.

# Pros of the Instant Runoff Voting System

Majority Rule ensures that controversial candidates are not elected without broad support. However, as history shows, controversial candidates in May 2020 had no chance of being elected even with the simple majority system.

# Key Issues with the Instant Runoff Voting System

**Complexity and Inconsistency**

The IRV system is inherently complex and can be implemented in various ways. The particular version chosen by RIPE introduces additional layers of complexity that are not transparent to the average voter. This complexity can lead to confusion and disenfranchisement, as many voters may not fully understand how their votes are counted and transferred. For example, it may not be clear if it is necessary to vote for each candidate or not.

**Majority Dominance**

The IRV system inherently favors candidates from the majority, often at the expense of strong minority candidates. In scenarios where there is a rift within the society, the system still tends to favor multiple candidates from the majority over a single strong candidate from the minority. The "50% threshold" required to win often necessitates the use of secondary votes, which further skews results in favor of the majority.

**Multiple Votes for Majority Preferences**

Technically, the IRV system allows voters to rank multiple candidates, effectively giving them more than one vote if they have multiple preferences. For example, if a majority voter ranks three preferred candidates, it can be seen as having three votes. This reduces the fairness of the system, as minority voters typically have fewer preferred candidates, thereby diminishing their overall influence.

**Lack of Voter Knowledge**

Many voters are unaware of the nuances and strategies needed to vote effectively within the IRV system. For instance, some voters may not know that they can skip ranking certain candidates without invalidating their vote. This lack of knowledge leads to improper representation and unfair outcomes.

# Case Study: General Meeting 2023

The General Meeting of 2023 serves as a prime example of the IRV system's flaws. Below are the detailed voting results:

**General Meeting 2023**

**Candidates & Rounds:**
- Raymond Jetten: 314, 322, 342, 355, 410, 580, 746
- Maria Häll: 495, 505, 522, 539, 603, 675, 738, 0
- Dmytro Kohmanyuk: 227, 242, 265, 325, 335, 356, 0, 0
- Fahad AlShirawi: 262, 269, 283, 285, 296, 0, 0, 0
- Harald Summa: 222, 231, 237, 245, 0, 0, 0, 0
- Olena Kushnir: 126, 131, 134, 0, 0, 0, 0, 0
- Salam Yamout: 103, 107, 0, 0, 0, 0, 0, 0

**Transferred Votes from Eliminated Candidates:** 0, 58, 83, 100, 140, 263, 229, 591
**Exhausted Votes:** 0, 34, 58, 92, 197, 230, 357, 504

**Abstain:** 525
**Total Votes:** 2366
**Quota:** 921

**Winners under IRV:**
- Raymond Jetten
- Maria Häll
- Harald Summa

**Hypothetical Winners with Single Vote System:**
- Maria Häll
- Raymond Jetten
- Fahad AlShirawi

**Analysis**

If each voter had a single vote, the results would have been different. Despite Fahad AlShirawi having strong community backing, he did not receive enough secondary votes to be elected. This outcome demonstrates how the current system unfairly excludes strong minority candidates in favor of majority-preferred candidates.

# Conclusion

The analysis confirms the unfairness of the current system, highlighting how majority voice multiplication works. This creates a significant rift within the community, as minority voices are not adequately represented, which might lead to further division, distrust, and conflicts.

# Call to Action

- We would like to know why IRV was chosen and, after recent discoveries about its flaws, if there is any plan to discuss reconsidering the voting system or its configuration.
- We suggest canceling prior registration for voting and extending the voting period to one week to allow more people to vote. We will send a separate email with a comparative analysis of the voting systems used by other RIRs.
- Push for reforms that ensure every vote is equal and every voice is heard. At the current moment, RIPE NCC cannot claim that it is inclusive enough, as the voting system is tuned for "majority dominance."

# Broken Links, References, and Other Problems on the RIPE NCC Website

1. [Minutes of the October 2009 GM](https://www.ripe.net/ripe/mail/archives/ncc-announce/2009-October/000342.html) - Link is broken
2. [RIPE 59 Meeting Report](https://www.ripe.net/publications/news/ripe-59-meeting-report/) - Link is broken
