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
| **Version** | 1.0.0 · data current as of 2026-06-19 |
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

PolitiFinder. (2026). *U.S. Election Records* (Version 1.0.0) [Data set]. 137 Finder
LLC. https://politifinder.com/data

Attribution (CC BY 4.0):

> Data source: U.S. Election Records by PolitiFinder (politifinder.com), licensed
> under CC BY 4.0.

## License

CC BY 4.0 (see `LICENSE.txt`). The underlying figures are public facts; PolitiFinder
claims rights only in the selection and arrangement of these records.
