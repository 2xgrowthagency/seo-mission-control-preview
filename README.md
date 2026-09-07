# SEO Mission Control v0

[Open the dashboard](https://2xgrowthagency.github.io/seo-mission-control-preview/)

This public repository holds only the built static preview. The SEO source
repository remains private. The dashboard now uses the eight-site real fleet
inventory: 341 articles counted September 6, 2026, plus successful homepage
HTTP checks at 11:49 PM Pacific that day. These are not search-performance metrics.

## File-backed data

The app fetches `data/portfolio.local.json` on page load and when **Reload
source** is clicked, with `data/portfolio.example.json` as demo fallback.
Despite the historical filename, this published file contains only the
explicitly projected public snapshot, not the original private inventory.
It is a schema-validated JSON snapshot; no database or
API credentials are needed. Editing this file and committing to `main`
publishes the next snapshot through GitHub Pages. Change `generatedAt` for
each snapshot so stale browser-local edits do not override new source data.

The source schema and adapter documentation live under `mission-control/`
in the private SEO repository. Keep the full existing shape and represent
unknown metrics explicitly. Do not put private client goals, decision notes,
analytics, credentials, or raw exports here: every deployed file is public.

The real snapshot includes site identity, inventory count/date, and public
availability observations. Search performance remains unknown. Private client
goals, notes, repository mappings and analytics were not copied. Proposed
measurement tasks are not represented as approved client targets.

UI edits are local to each browser; they do not write back to GitHub or sync
between people. Shared changes go through the snapshot file. Additional private
fields require an approved public scope or authenticated hosting.

## App refresh and rollback

Build from a reviewed commit of the private SEO repository in a clean checkout,
without `portfolio.local.json`. Publish only the generated static assets and
sanitized snapshot to this repository. Do not copy the source repository or
its Git history. Revert a preview commit to restore its previous snapshot/build.

Initial build: SEO PR #9, source revision
`c5e7f95aa97f1962258ae3ce9d7ccf84d26f9fe0`, independently verified by Crosscheck.
