# Attribution

## What is licensed here

All article text in this repository is adapted from **English Wikipedia** and is
licensed **CC BY-SA 4.0** (`LICENSE`). Wikipedia text is written collaboratively
by Wikipedia contributors and is itself CC BY-SA. The distillations under
`articles/distilled/` and the curated selections under `articles/db-packs/` are
adaptations of that text, so they carry the same license and the same
attribution requirement.

`packs/catalog-source.json` is factual metadata about that text (pack ids,
names, descriptions, and article id lists) rather than an adaptation of it.

## How attribution is carried

Two layers, because a pack is distributed as a single archive and read back one
article at a time.

**Per article.** Every article file ends with a footer written by
`tools/article_text.py:attribution_footer` in the code repository:

```
Source: adapted from "<title>" on English Wikipedia, whose text is written by
Wikipedia contributors, under CC BY-SA 4.0
(https://creativecommons.org/licenses/by-sa/4.0/): <article url>
```

That names the creator (Wikipedia contributors), states the license with its
URI, and links the source article, which is what CC BY-SA 4.0 section 3(a) asks
for. Because the footer travels inside the article, it survives extraction from
the pack and renders wherever the article is read.

**Per pack.** Each pack's entry in the published catalogue at
`packs.educated.space/index.json` also carries `"license": "CC BY-SA 4.0"`,
written by `tools/build_pack_catalog.py`. The device and the Android app both
read that catalogue, and the same catalogue is embedded in the firmware from
`android/app/src/main/assets/pack_catalog.json`.

## Keeping it that way

`tools/article_text.py` is the single definition of a finalized article: no
generator commentary, exactly one `h1` title, and the attribution footer. Every
generator calls `finalize_article` before writing, so regenerated content cannot
lose the footer. To check or repair the corpus:

```sh
python3 tools/finalize_articles.py --check    # CI: fail if any article drifts
python3 tools/finalize_articles.py --apply    # rewrite drifted articles
```

`tools/audit_meta_commentary.py` is the recall check for the generator-commentary
rules: it asks a local model to quote any remaining non-article text, verifies
each quote verbatim, and reports what the rules missed.

## History of the footer

The footer was added in a corpus-wide pass on 2026-09-12. Before that, no
article carried per-article attribution, and `tools/export_distilled.py`
explicitly set `ATTRIBUTION = ""` with the note that article pages carried no
source footer. The same pass removed generator commentary from 11 articles and
fixed `h1`-as-section-heading in 8 more. Pack bytes changed for every pack, so
the pack versions were bumped and the catalogue must be republished.

## Pack inventory

`articles/db-packs/` — 27 packs, 2209 articles:

| Pack directory | Articles | Size |
| --- | --- | --- |
| `ancient-worlds-and-archaeology` | 100 | 501 kB |
| `arts-language-culture` | 100 | 540 kB |
| `biology-health` | 100 | 568 kB |
| `climate-and-the-living-planet` | 24 | 142 kB |
| `cosmos-and-spaceflight` | 100 | 540 kB |
| `creative-arts-and-world-languages` | 24 | 144 kB |
| `earth-climate-environment` | 100 | 570 kB |
| `engineering-everyday-systems` | 100 | 562 kB |
| `essential-computing` | 100 | 555 kB |
| `history-civilizations` | 100 | 563 kB |
| `ideas-ethics-and-society` | 100 | 557 kB |
| `inventors-and-everyday-engineering` | 24 | 138 kB |
| `living-world` | 100 | 567 kB |
| `machines-materials-and-infrastructure` | 100 | 547 kB |
| `mathematical-thinking` | 100 | 533 kB |
| `mind-and-behavior` | 100 | 562 kB |
| `mind-ethics-and-meaning` | 24 | 151 kB |
| `money-markets-and-work` | 100 | 539 kB |
| `music-art-and-design` | 100 | 549 kB |
| `natural-sciences` | 100 | 537 kB |
| `oceans-weather-and-earth` | 100 | 520 kB |
| `philosophy-religion-ethics` | 100 | 570 kB |
| `society-government-economy` | 100 | 581 kB |
| `space-and-the-cosmos` | 22 | 123 kB |
| `story-language-and-media` | 100 | 540 kB |
| `uk-curriculum` | 67 | 380 kB |
| `world-history-turning-points` | 24 | 147 kB |

`articles/distilled/` — 3948 articles, 28.5 MB.
`articles/starter/` — 100 articles, 0.1 MB.

## If you redistribute a pack

Keep each article's source footer and the pack's `"license"` field intact, keep
this repository's `LICENSE`, and make clear that the text is adapted from
Wikipedia by Wikipedia contributors. If you modify the text, your version must
stay under CC BY-SA 4.0 or a compatible license, and you may not add
restrictions on top.
