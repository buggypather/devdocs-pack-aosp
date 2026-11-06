# Android OS (AOSP) docs for DevDocs

The [Android Open Source Project's documentation](https://source.android.com/docs) (how the
Android operating system is built, ported, tested and secured) as a DevDocs doc pack: searchable
and readable offline, and scraped again every week.

**To add it:** in DevDocs (the [doc packs version](https://github.com/buggypather/devdocs/tree/main-custom-docs)),
open **Preferences → Doc packs**, paste `https://github.com/buggypather/devdocs-pack-aosp/tree/pack`,
and click **Add**. Then tick **Android OS (AOSP)** in the list on the left and click **Apply**.

It has the guides (about 1,500 pages). It leaves out the generated API references (Trade
Federation, HALs) and the monthly security bulletins, which together are two thirds of the site.

## How it's made

A GitHub Actions workflow (`.github/workflows/scrape.yml`) checks out the DevDocs fork, runs its
AOSP scraper (`lib/docs/scrapers/aosp.rb`) and publishes the result to the `pack` branch. The
scraper reads at most four pages a second, to go easy on the site. To scrape now, open the
**Actions** tab, choose **Scrape docs** and click **Run workflow**.

## Licence

The documentation is © Google LLC and the Android Open Source Project. Its text is licensed under
the [Creative Commons Attribution 4.0 License](https://creativecommons.org/licenses/by/4.0/) and its
code samples under the [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0); each page
in the pack credits Google and links to its original. This repository's own files are under the
MIT licence.
