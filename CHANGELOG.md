# Changelog

All notable changes to this reference are documented here.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html)
informally — versioning the *content*, not software.

## [1.1] — 2026-05

### Changed (general.md)

- **Web/dev terminology defaults**: `Header → Хедер` and `Footer → Футер` are
  now the primary terms for web/dev/product contexts (matches how Ukrainian
  developers actually speak). Previous defaults ("шапка/підвал" and
  "заголовок/нижній колонтитул") demoted to context-specific alternates.
- Added `хедер` and `футер` to the established/acceptable anglicisms list
  in Section 6.1 of `general.md`.

### Changed (trucking.md)

This release also includes native-speaker corrections to the trucking domain
supplement from a working US-Ukrainian fleet operator. See
`docs/domain-supplements/trucking.md` Section 12 for the full v1.1 changelog
of trucking-specific changes (added formal-vs-operational register hierarchy,
corrected truck/load/fleet/log terminology to match actual driver usage,
added forbidden-words list).

## [1.0] — 2026-05

### Added

- Initial release of `docs/general.md` — universal Ukrainian localization
  reference covering modern standard and diaspora flavors.
- Initial release of `docs/domain-supplements/trucking.md` — industry-specific
  supplement for US trucking/logistics use cases.
- Content types covered: business, product/SaaS, marketing, casual, social,
  creative, legal.
- Includes: IT/SaaS glossary (~150 terms), Russification anti-patterns
  (~60 words + 6 syntax patterns), side-by-side examples, pre-output checklist,
  10 commandments quick reference.

---

## How Changes Are Tracked

Each reference doc (`general.md`, `trucking.md`, etc.) has its own internal
version history in its final section. This top-level CHANGELOG tracks
repository-wide changes — version bumps to the docs themselves, structural
additions (new domain supplements, new integration guides), and meta changes.

Individual rule corrections, glossary additions, and other small content
changes within a doc are tracked in that doc's own version history table,
not here, unless they're significant enough to warrant a new release.

## Native-Speaker Credits

Native-speaker corrections incorporated in each version are credited in the
respective doc's internal changelog. Significant contributions are also
called out by GitHub handle in the GitHub release notes.
