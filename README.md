# The Median Canadian

A curious Canadian explaining Canada through numbers, every week.

Site: https://mediancanadian.ca/ (the link in the Instagram bio)

Each week's story has its own repository, with its page, data, analysis code and full methodology, so anyone can check or challenge any number.

| Week | Story | Where |
|---|---|---|
| 3 | How B.C. elected a Conservative majority, October 24, 2026 | [bc-election-oct26](https://github.com/mediancanadian/bc-election-oct26) |
| 2 | Talking trade with Türkiye, October 2026 | [canada-turkey-oct26](https://github.com/mediancanadian/canada-turkey-oct26) |
| 1 | Alberta's separation vote, October 19, 2026 | [ab-referendum-live](https://github.com/mediancanadian/ab-referendum-live) |

## The hub page

`index.html` is built by `hub/build_hub.py` from each week's own files: the cover slide in `covers/`, and the findings and numbers from the week's data, so the hub always matches the week's page. The build stops with a message if a finding listed on the hub no longer holds for the data.

To rebuild it:

1. Clone every week into this folder (git ignores them):
   `git clone https://github.com/mediancanadian/ab-referendum-live ab-referendum-live`
   `git clone https://github.com/mediancanadian/canada-turkey-oct26 canada-turkey-oct26`
   `git clone https://github.com/mediancanadian/bc-election-oct26 bc-election-oct26`
2. `pip install pillow`
3. `python3 hub/build_hub.py`

Every week: its cover slide (the first image of the Instagram post) in `covers/` as `week-NN-cover.jpg`, and one entry in the `POSTS` list in `hub/build_hub.py` that reads its findings from the week's own files. The build stops if a week's folder has no entry or no cover.

## Licence

- **Code:** Apache License 2.0 (LICENSE and NOTICE).
- **Text, charts, maps and slides:** CC BY 4.0 (LICENSE-CONTENT.md).
- **Photo in the week 2 cover slide:** Anıtkabir, Ankara, by Nicoleon on Wikimedia Commons, CC0 1.0.
- **Photo in the week 3 cover slide:** the Parliament Buildings, Victoria, by dronepicr on Wikimedia Commons, CC BY 2.0 (https://commons.wikimedia.org/wiki/File:Legislative_Assembly_of_British_Columbia_Vancouver_island_(29786723167).jpg).
- **Data:** belongs to its publishers; each week's folder lists its sources and their licences.
