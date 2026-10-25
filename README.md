<!-- README copy: Ascension Writer (site-copy/repo-1.md, Oct 25, 2026). The three Engineer TODOs are filled in by the Engineer and await the Writer's check. -->

# Ascension open data

Daily and weekly ranks of consumer AI apps from [Ascension](https://ascension.fyi), a daily leaderboard that blends the App Store and Google Play charts into one board. This repo mirrors the open-data files published at https://ascension.fyi/data/.

The files hold ranks only.

## What's here

- `daily/YYYY-MM-DD.csv` and `.json`: one board per day, in US Eastern time (that day's last read). History starts Oct 19, 2026.
- `weekly/YYYY-MM-DD.csv` and `.json`: the full board as frozen each Friday, named for the Monday of the week.
- `daily/latest.*` and `weekly/latest.*`: copies of the newest file.
- `index.json`: every dated file, with the credit line and license.

This repo, [lmken/ascension-data](https://github.com/lmken/ascension-data), uses exactly this layout: `daily/`, `weekly/`, and `index.json` at the top level, next to this README and the LICENSE file. It mirrors only those files. The weekly top 10 (`/week/YYYY-MM-DD/top.csv`), `leaderboard.json`, and `climbers.json` aren't mirrored here; you can get them from https://ascension.fyi/press/.

## Updates

The board updates daily at around 6 AM ET, and a new weekly file is added every Friday. Dated files don't change once they're written.

This repo syncs right after the site's daily build and live check, at around 6 AM ET. It only gets a new commit when a file changed.

## Fields

CSV and JSON files share the same five fields. JSON files also carry a `meta` object with the title, date, source URL, credit line, and license.

| Field | Meaning |
|---|---|
| `rank` | Position on the blended App Store and Google Play board, starting at 1. |
| `app` | The app's name as shown on the board. |
| `platform` | `ios`, `android`, or `ios+android`. An app on both stores is ranked once. |
| `change` | Places moved since the previous day (weekly files: previous week). Positive means up. `new` if the app wasn't on the previous board. Empty (null in JSON) if there's no comparable earlier board. |
| `date` | Daily files: the day in US Eastern time. Weekly files: the Monday of the week. Both YYYY-MM-DD. |

## License

The data is licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). You can share and adapt it, including for commercial use, as long as you credit it as "Data powered by Ascension (ascension.fyi)" and link to [ascension.fyi](https://ascension.fyi) when you can.

This repo includes a [LICENSE](LICENSE) file with the full CC BY 4.0 text.

## How to cite

Use this line, and link "Ascension" to ascension.fyi when you can:

> Data powered by Ascension (ascension.fyi)

In a sentence: "[App] ranked No. [rank] on the Ascension leaderboard of consumer AI apps on [date], according to data powered by Ascension."

Ranks move every day, so name the date you're citing. More on citing the data: https://ascension.fyi/press/
