# YearlyRank AI Tool data file

This folder contains a public extract of the directory and official totals already published on [aitool.yearlyrank.com](https://aitool.yearlyrank.com).

**File:** [yearlyrank-aitool-scores-2026-11-15.csv](yearlyrank-aitool-scores-2026-11-15.csv) (UTF-8, no BOM)

The same official totals and positions also appear in the site’s downloadable file: [https://aitool.yearlyrank.com/data/rank-2026.csv](https://aitool.yearlyrank.com/data/rank-2026.csv). This repository file adds a status column and the YearlyRank tool-page URL.

Edition figures: **286** families; **85** scored; **180** insufficient data; **21** method under review. Data as of **2026-11-15**. Official scores were published on 2026-11-16.

## Columns

| Column | Meaning |
| --- | --- |
| `slug` | Public identifier used in the tool-page URL |
| `name` | English display name as shown on the site |
| `type` | One of `app`, `agent`, `model`, `api`. The four types are ranked separately |
| `primary_category` | English name of the primary task category |
| `official_score` | Official overall score (one decimal). Blank when the family is not scored |
| `status` | `scored`, `insufficient_data`, or `method_under_review` |
| `rank_within_type` | Position within that type, as shown on the site. Ties share a position (competition ranking: 1, 2, 2, 4). Blank when the family is not scored, or if a type has fewer than 5 scored families (the site then hides positions) |
| `url` | Tool page on the live site, `https://aitool.yearlyrank.com/tool/<slug>/` |
| `data_as_of` | Directory cutoff shown on the site: 2026-11-15 |

`official_score` is the official overall total only. On some listing and detail pages the same total is shown as an integer; a one-decimal value is shown when nearby scores in that type would otherwise look the same. Quote a score or position only as shown on the page.

## What is not in this file

Per-signal values, weights, and other unpublished inputs are **not** included. The live site states that only the official overall score is published; values for the individual signals are not published.

## Licence

Scores and directory data produced by the site are licensed for non-commercial use with attribution (CC BY-NC 4.0 equivalent). Please attribute YearlyRank and link to [https://aitool.yearlyrank.com](https://aitool.yearlyrank.com). Upstream signals keep their own licences (listed on the [methodology page](https://aitool.yearlyrank.com/rank/methodology/); for example CrUX is CC BY 4.0).

## How to reproduce or verify

The scoring **method** is public: [https://aitool.yearlyrank.com/rank/methodology/](https://aitool.yearlyrank.com/rank/methodology/). The signals (CrUX website traffic, multilingual Wikipedia pageviews, new GitHub stars, package downloads, Hugging Face downloads) come from public sources that anyone can query, under each source’s own licence and terms.

This does **not** mean you can exactly reproduce the per-signal inputs used for a given edition. Those per-signal values are not published, retrieval windows and source snapshots can differ, and some families have too few countable signals or a method still under review.

What you *can* verify from public pages:

- Official totals and positions against the [ranking page](https://aitool.yearlyrank.com/rank/), a tool page, or [rank-2026.csv](https://aitool.yearlyrank.com/data/rank-2026.csv)
- Status labels (“Insufficient data”, “Method under review”) on those pages
- That community stars and comments are not used in the official score

Scores are computed from public signals only. Suggesting a listing, or leaving a community rating, does not change an official score.
