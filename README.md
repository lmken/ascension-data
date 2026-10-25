<!-- PLACEHOLDER COPY (REPO-1, Oct 25, 2026): written by the Engineer as a stand-in. The Writer will approve or replace
     every line of this README before the repo goes public. Do not treat this wording as final. -->

> **PLACEHOLDER:** this README is draft copy awaiting the Writer's review.

# Ascension open data

Daily and weekly ranks for consumer AI apps on the App Store and Google Play, from
[Ascension](https://ascension.fyi). This repo mirrors the open data files published at
[ascension.fyi/press/](https://ascension.fyi/press/#open-data).

## What's in it

| Path | What it is |
| --- | --- |
| `daily/YYYY-MM-DD.csv` / `.json` | Every app on that day's board (US Eastern time), in rank order |
| `daily/latest.csv` / `.json` | Same content as the newest daily file |
| `weekly/YYYY-MM-DD.csv` / `.json` | The full board as frozen each Friday, named for the Monday of the week |
| `weekly/latest.csv` / `.json` | Same content as the newest weekly file |
| `index.json` | Every dated file, with the credit line and license |

Every file has the same five columns:

- `rank`: position on the blended App Store + Google Play board of consumer AI apps
- `app`: the app's name
- `platform`: `ios`, `android`, or `ios+android`
- `change`: places moved since the previous day or week (positive = up), `new` if the app wasn't on the previous board, or empty when there's no comparable previous board
- `date`: the day (daily files) or the Monday of the week (weekly files), as YYYY-MM-DD

Ranks come from public App Store and Google Play charts. They aren't download or revenue figures.

## How often it updates

Daily, right after Ascension's refresh at around 6 AM ET. Weekly files are added every Friday.
Dated files never change once they're written.

## License

The data is licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). You can share and
adapt it, including for commercial use, as long as you credit it as "Data powered by Ascension (ascension.fyi)"
and link to [https://ascension.fyi](https://ascension.fyi) when you can. Full text: [LICENSE](LICENSE).

## How to cite it

Use this line, and link "Ascension" to ascension.fyi when you can:

> Data powered by Ascension (ascension.fyi)

In a sentence:

> [App] ranked No. [rank] on the [store] [chart] in [country] for the week of [date], according to data powered by Ascension.

Rankings move every day, so name the date you're citing. It's in each file.
