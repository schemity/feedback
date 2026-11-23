# Schemity Roadmap

What we recently shipped, what we are building, and what we are considering. This page exists so you can see where [Schemity](https://schemity.com) is heading - and influence it: if something in "Considering" matters to you, [open a feature request](https://github.com/schemity/feedback/issues/new?assignees=&labels=enhancement&template=feature_request.md&title=%5BFEATURE%5D+) or vote with a 👍 on the existing issue.

## Recently shipped

- **Schemity Free** (v2.15.0) - after the Pro trial the desktop app stays free: connect, reverse engineer, and migrate PostgreSQL, MySQL, MariaDB, and SQLite
- **Lint auto-fix** (v2.15.0) - a Fix button turns a finding into one reviewed, undoable edit
- **Exclusion and temporal constraints** (v2.15.0) - PostgreSQL EXCLUDE, WITHOUT OVERLAPS, PERIOD, and NOT ENFORCED kept as declared
- **Migration Check** (v2.14.9) - a free GitHub Action and CLI that report what a pull request's migrations do, with no database
- **Cloudflare D1 as its own database** (v2.14.9) - read over Cloudflare's API or from a local wrangler file, never migrated
- **Drafts on every database** (v2.14.9) - a reopened draft merges three-way with the database as it is now
- **Starred diagrams** (v2.14.8) - a Starred group above the workspaces, across every workspace
- **Refresh keeps your edits** (v2.14.7) - a three-way merge brings the database's changes in and keeps yours pending

## Building now

- **More lint rules** - schema lint is incremental by design. Still open: rules that need the live connection (counting duplicates before an ALTER, NOT NULL without a default on a populated table), the remaining architecture rules that read context views, and stable public rule ids to use as documentation anchors

## Considering

If any of these matter to you, open a feature request or vote with a 👍 on the existing issue - that is exactly what moves them up this list.

- **Headless diagram CLI** - the `schemity` CLI already checks migrations in CI; still open: render SVG/PNG, emit SQL or DBML from the diagram file, and a check that fails when the committed ERD drifts from a target database
- **Large-schema abstraction** - collapse entities to title-only or keys-only, and a focus mode that dims everything not connected to the selected entity (the minimap half of this shipped in v2.9.0)
- **File-vs-file schema diff** - diff two versions of a diagram file (or two git commits) into a visual changelog and generated ALTER statements
- **Notation switching** - numeric/min-max cardinalities as an alternative to crow's foot

---

This roadmap is directional, not a commitment - priorities shift based on the feedback in this repository. Release details land in the [changelog](CHANGELOG.md) when features ship.
