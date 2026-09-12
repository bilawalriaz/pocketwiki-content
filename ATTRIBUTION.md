# Attribution

## What is licensed here

All article text in this repository is adapted from **English Wikipedia** and
is licensed **CC BY-SA 4.0** (`LICENSE`). Wikipedia text is written
collaboratively by Wikipedia contributors and is itself CC BY-SA; the
distillations under `articles/distilled/` and the curated selections under
`articles/db-packs/` are adaptations of that text, so they carry the same
license and the same attribution requirement.

`packs/catalog-source.json` is factual metadata about that text (pack ids,
titles, descriptions, and article id lists) rather than an adaptation of it.

## What the published packs carry today

Each pack's entry in the published catalogue at `packs.educated.space/index.json`
carries `"license": "CC BY-SA 4.0"`, written by
`tools/build_pack_catalog.py` in the code repository. The device and the
Android app both read that catalogue, so the license name travels with every
pack a user installs. The same catalogue is embedded in the firmware from
`android/app/src/main/assets/pack_catalog.json`.

## Known gap: no per-article source link

None of the 4075 article files embed a per-article
source link or license notice. `tools/export_distilled.py` sets
`ATTRIBUTION = ""` with the comment that article pages carry no per-article
Source/Licence footer, and the checked-in corpus matches that. The promise in
`tools/fetch_starter_pack.py`'s docstring — that every checked-in article keeps
a source link and CC BY-SA notice — does not hold for the current files.

CC BY-SA 4.0 section 3(a) requires anyone sharing the material to identify the
creator, keep a copyright notice, refer to the license, and, to the extent
reasonably practicable, give a URI to the material. The pack-level
`"license"` field covers the license reference and the packs name their source
in the catalogue, but the source URI is missing, and it is cheap here: an
article's `h1` title is its Wikipedia title, so
`https://en.wikipedia.org/wiki/<title>` is derivable without any lookup.

Recommended fix, in order of preference:

1. Append a one-line attribution footer to every article, built from the `h1`
   title: title, "adapted from Wikipedia", and the CC BY-SA 4.0 URI. Then
   rebuild and republish the catalogue so pack bytes and versions match.
2. Set `ATTRIBUTION` in `tools/export_distilled.py` to that same template so
   regenerated content cannot lose the footer again.

Either way the packs change bytes, so the pack versions in `packs/catalog-source.json` must
be bumped and the catalogue republished to `packs.educated.space` before the
next firmware release.

## Pack inventory

`articles/db-packs/` — 27 packs, 2209 articles:

| Pack directory | Articles | Size |
| --- | --- | --- |
| `ancient-worlds-and-archaeology` | 100 | 478 kB |
| `arts-language-culture` | 100 | 516 kB |
| `biology-health` | 100 | 545 kB |
| `climate-and-the-living-planet` | 24 | 137 kB |
| `cosmos-and-spaceflight` | 100 | 516 kB |
| `creative-arts-and-world-languages` | 24 | 139 kB |
| `earth-climate-environment` | 100 | 547 kB |
| `engineering-everyday-systems` | 100 | 539 kB |
| `essential-computing` | 100 | 530 kB |
| `history-civilizations` | 100 | 540 kB |
| `ideas-ethics-and-society` | 100 | 534 kB |
| `inventors-and-everyday-engineering` | 24 | 133 kB |
| `living-world` | 100 | 544 kB |
| `machines-materials-and-infrastructure` | 100 | 524 kB |
| `mathematical-thinking` | 100 | 509 kB |
| `mind-and-behavior` | 100 | 538 kB |
| `mind-ethics-and-meaning` | 24 | 145 kB |
| `money-markets-and-work` | 100 | 516 kB |
| `music-art-and-design` | 100 | 526 kB |
| `natural-sciences` | 100 | 514 kB |
| `oceans-weather-and-earth` | 100 | 497 kB |
| `philosophy-religion-ethics` | 100 | 546 kB |
| `society-government-economy` | 100 | 558 kB |
| `space-and-the-cosmos` | 22 | 118 kB |
| `story-language-and-media` | 100 | 516 kB |
| `uk-curriculum` | 67 | 368 kB |
| `world-history-turning-points` | 24 | 141 kB |

`articles/distilled/` — 3948 articles, 27.7 MB.
`articles/starter/` — 100 articles, 0.1 MB.

## If you redistribute a pack

Keep the pack's `"license"` field and the catalogue's attribution intact, keep
this repository's `LICENSE`, and make clear that the text is adapted from
Wikipedia by Wikipedia contributors. If you modify the text, your version must
stay under CC BY-SA 4.0 or a compatible license; you may not add restrictions
on top.
