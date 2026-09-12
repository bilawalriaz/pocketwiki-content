# PocketWiki content

Article text and the pack manifest for [PocketWiki](https://github.com/bilawalriaz/pocketwiki-esp32), an offline
library that runs on an ESP32-C3 or ESP32-S3 board and serves its articles over
its own Wi-Fi network.

This repository contains no code. The firmware, packer, Android companion app,
and web tooling live in the [code repository](https://github.com/bilawalriaz/pocketwiki-esp32), and that tooling
reads this checkout to build packs and to embed the built-in archive into the
firmware.

## Why this is a separate repository

Every article here is adapted from English Wikipedia and is therefore licensed
**CC BY-SA 4.0**. That is a content license, and it is not the Apache-2.0
license that covers the code. Splitting the two keeps each repository
unambiguous: a code contributor never has to reason about a content license,
and a content contributor never has to reason about a software license.

## Layout

| Path | Contents |
| --- | --- |
| `articles/db-packs/` | 27 thematic pack directories, 2209 articles in total, plus `selection-report.json` recording how each pack's titles were selected. |
| `articles/distilled/` | 3948 study-grade distillations derived from the Wikipedia vital-article lists. |
| `articles/starter/` | 100 articles: the curated starter pack shipped on a fresh device. |
| `packs/catalog-source.json` | The pack manifest. Holds the schema, catalogue version, and base URL, and for each of its 30 packs the id, name, version, description, source directory, and ordered list of article ids. |

Article filenames are numeric ids that trace back to each pack's selection
list; the first `h1` in a file is the article title, and for Wikipedia imports
that title is the source article title.

## Building packs

Clone both repositories side by side and run the code repository's tools. They
resolve this checkout at `../pocketwiki-content` by default, or wherever
`POCKETWIKI_CONTENT_DIR` points.

```sh
git clone https://github.com/bilawalriaz/pocketwiki-esp32 pocketwiki-esp32
git clone https://github.com/bilawalriaz/pocketwiki-content.git pocketwiki-content
cd pocketwiki-esp32

# Build the published catalogue and the device's copy of it.
python3 tools/build_pack_catalog.py

# Build one pack by hand.
python3 tools/pack_content.py build \
  ../pocketwiki-content/articles/db-packs/biology-health build/biology --codec gzip
```

No step fetches anything over the network, so pack and firmware builds work
offline.

## License and attribution

The text in this repository is licensed under CC BY-SA 4.0. See `LICENSE` for
the full license text and `ATTRIBUTION.md` for provenance, the attribution
actually carried by the published packs, and the one gap that remains.
