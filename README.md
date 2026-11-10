# U.S. Election Records — PolitiFinder

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.20768539.svg)](https://doi.org/10.5281/zenodo.20768539)

A small, tidy file of the most striking records in American election history:
biggest landslides, closest races, most votes, the presidents who won while losing
the popular vote, the youngest and oldest senators, and more — across President,
U.S. Senate, U.S. House, and Governor.

Compiled by [PolitiFinder](https://politifinder.com) (137 Finder LLC). Licensed
**CC BY 4.0** — free to use, including commercially, with attribution.

## At a glance

| | |
|---|---|
| **File** | `politifinder_election_records.csv` (+ `.json`) |
| **Rows** | 115 (one per record entry, ~12 record categories) |
| **Version** | 1.0.2 · data current as of 2026-11-06 |
| **License** | CC BY 4.0 |
| **Landing page** | https://politifinder.com/data |

This file is the public "greatest hits" already shown on PolitiFinder's
[records & rankings](https://politifinder.com/rankings) pages, packaged for reuse.
Every record reconciles to its live ranking page. It contains **names and public
URLs only** — no internal identifiers and no underlying race-by-race data.

## Records included

Presidents who won while losing the popular vote · biggest presidential landslides ·
closest presidential elections · most popular votes in one election · highest
popular-vote percentage · most electoral votes in one election · closest U.S.
Senate / House / Governor elections · strongest third-party & independent runs ·
youngest and oldest U.S. senators · most career popular votes (named-candidate basis).

## Columns

| field | type | description |
|---|---|---|
| `record` | string | the record category, e.g. "Biggest presidential landslides" |
| `rank` | integer | 1..N within that record |
| `subject` | string | candidate name or election (display text) |
| `detail` | string | short context, e.g. "def. James M. Cox" or "Minnesota · def. Norm Coleman" |
| `metric` | string | what is measured, e.g. "popular-vote margin (pts)" |
| `value` | number | the figure |
| `unit` | string | points / votes / % / electoral votes / years |
| `year` | integer | election year (blank for career records) |
| `office` | enum | President / U.S. Senate / U.S. House / Governor |
| `url` | uri | the public PolitiFinder page for that record or candidate |

## Note on career records

Career totals count a person **only as the named candidate**; running-mate (vice-
presidential) ticket votes are **excluded**. There are no grand totals and no party
sums in this file.

## Sources

Records are derived from PolitiFinder's compilation of official U.S. election
results: the FEC and the Clerk of the U.S. House (federal, 1976+), the MIT Election
Data and Science Lab, the Constituency-Level Elections Archive (historical
Senate/House), official state canvasses (governors), and official/public returns
(ICPSR; *A New Nation Votes*) with electoral votes from the National Archives. See
https://politifinder.com/methodology and `NOTICE.md`.

## How to cite

PolitiFinder. (2026). *U.S. Election Records* (Version 1.0.2) [Data set]. 137 Finder
LLC. https://politifinder.com/data

Attribution (CC BY 4.0):

> Data source: U.S. Election Records by PolitiFinder (politifinder.com), licensed
> under CC BY 4.0.

## Changelog

- **1.0.2 (2026-11-06):** Four record lists changed; the other nine are identical
  to 1.0.1. The three all-time closest lists (U.S. House, U.S. Senate, governor) are
  now ranked by the exact vote margin, winner's votes minus runner-up's, with ties
  broken by the gap in vote share; their `metric` is now "vote margin (votes)" and
  `value` is that vote count. In 1.0.1 they were ranked by the share gap rounded to
  two decimals, so races decided by 4 and by 12 votes both read 0.00 and their order
  was arbitrary. Closest House now runs Indiana 1984 (4 votes), Iowa 2020 (6),
  Indiana 1930 (9), Wisconsin 1944 (11), Indiana 1960 (12); Ohio 1900, Colorado 1952
  and Illinois 1930 enter, Missouri 1990, Illinois 1922 and Indiana 1986 leave.
  Closest Senate: New Hampshire 1974 (2 votes), Nevada 1964 (48), North Dakota 1974
  (186), Minnesota 2008 (312); Delaware 1922, South Dakota 2002, Utah 1922, South
  Dakota 1962 and Nevada 1974 enter, Iowa 1924, Washington 2000, Missouri 1944,
  Florida 2018 and New Hampshire 2016 leave. Closest governor: Kansas 1912 (29 votes)
  is now first, ahead of Maine 1840 (67), New Hampshire 1856 (88) and Minnesota 1962
  (91); New Hampshire 1856 and 1890, Connecticut 1871 and Wisconsin 1857 and 1855
  enter, Kansas 1940, Michigan 1950, New York 1850 and 1854 and Maryland 1919 leave.
  "Strongest third-party / independent runs" now includes Gary Johnson (2016,
  4,489,341 votes) and Jo Jorgensen (2020, 1,865,535 votes), from the FEC-official
  third-party totals for 2004–2024 that PolitiFinder added after 1.0.1; Strom
  Thurmond (1948) and James B. Weaver (1892) drop out of the top 10 by raw vote
  count. No 2026 results: they enter as each state certifies.
- **1.0.1:** Version bump on Zenodo only (1.0.0's record was tombstoned and
  reissued); file contents unchanged from 1.0.0.
- **1.0.0 (2026-06-19):** Initial release.

## License

CC BY 4.0 (see `LICENSE.txt`). The underlying figures are public facts; PolitiFinder
claims rights only in the selection and arrangement of these records.
