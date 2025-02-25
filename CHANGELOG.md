# Changelog

## Unreleased

## 1.10.0

### Changed

- MSRV (minimum supported rust version) is now 1.66.0 for mdbook v0.4.32 ([#109](https://github.com/tommilligan/mdbook-admonish/pull/109))

### Added

- Support `mdbook test` running doctests inside admonish blocks. Opt-in to this by setting `renderer.test.action_mode = "strip"` ([#109](https://github.com/tommilligan/mdbook-admonish/pull/109))
- Log a warning when an invalid admonish block is encountered ([#109](https://github.com/tommilligan/mdbook-admonish/pull/109))

### Fixed

- Document all `book.toml` configuration options [in the reference](https://tommilligan.github.io/mdbook-admonish/reference.html), some of which were previously undocumened ([#109](https://github.com/tommilligan/mdbook-admonish/pull/109))

## 1.9.0

### Changed

- Styles updated to `^2.0.1`. Run `mdbook-admonish install` to update.
- MSRV (minimum supported rust version) is now 1.64.0 for clap v4 ([#79](https://github.com/tommilligan/mdbook-admonish/pull/79))
- More verbose error messages for invalid TOML configurations ([#79](https://github.com/tommilligan/mdbook-admonish/pull/79))

### Added

- User can set book-wide default for title and collapsible properties ([#84](https://github.com/tommilligan/mdbook-admonish/pull/84)), thanks to [@ShaunSHamilton](https://github.com/ShaunSHamilton)

### Fixed

- Custom installation and CSS directories are now normalized ([#49](https://github.com/tommilligan/mdbook-admonish/pull/49))
- Fix title bars with no text rendering badly ([#83](https://github.com/tommilligan/mdbook-admonish/pull/83)), thanks to [@ShaunSHamilton](https://github.com/ShaunSHamilton)
- Better error message display on crash ([#48](https://github.com/tommilligan/mdbook-admonish/pull/48))
- Better support for commonmark code fence syntax ([#88](https://github.com/tommilligan/mdbook-admonish/pull/88), [#89](https://github.com/tommilligan/mdbook-admonish/pull/89))

## 1.8.0

### Changed

- MSRV (minimum supported rust version) is now 1.60.0 for clap v4

## 1.7.0

### Changed

- Required styles version is now `^2.0.0` (release `1.7.0`). Run `mdbook-admonish install` to update.

### Added

- Support key/value configuration ([#24](https://github.com/tommilligan/mdbook-admonish/pull/24), thanks [@gggto](https://github.com/gggto) and [@schungx](https://github.com/schungx) for design input)
- Support collapsible admonition bodies ([#26](https://github.com/tommilligan/mdbook-admonish/pull/26), thanks [@gggto](https://github.com/gggto) for the suggestion and implementation!)
- Make anchor links hoverable ([#27](https://github.com/tommilligan/mdbook-admonish/pull/27))
- Better handling for misconfigured admonitions ([#25](https://github.com/tommilligan/mdbook-admonish/pull/25))
  - Nicer in-book error messages
  - Option to fail the build instead

## 1.6.0

**Please note:** If updating from an older version, this release requires `mdboook-admonish install` to be rerun after installation.

This behaviour is [documented in the readme here](https://github.com/tommilligan/mdbook-admonish#semantic-versioning), and may appear in any future minor version release.

### Changed

- Required styles version is now `^1.0.0` (release `1.6.0`). Run `mdbook-admonish install` to update.

### Added

- Enforce updating installed styles when required for new features ([#19](https://github.com/tommilligan/mdbook-admonish/pull/19)
- Each admonition has a unique id. Click the header bar to navigate to the anchor link ([#19](https://github.com/tommilligan/mdbook-admonish/pull/19), thanks [@schungx](https://github.com/schungx) for the suggestion)

### Fixed

- Header bar overflow at some zoom levels on Firefox ([#21](https://github.com/tommilligan/mdbook-admonish/pull/21), thanks to [@sgoudham](https://github.com/sgoudham) for the report)

## 1.5.0

### Added

- Admonitions now have an autogenerated `id`, to support anchor links ([#16](https://github.com/tommilligan/mdbook-admonish/pull/16), thanks [@schungx](https://github.com/schungx) for the suggestion)

## 1.4.1

### Changed

- Bumped locked dependency versions (mdbook v0.4.18)

### Packaging

- Support building and releasing binary artefacts.

## 1.4.0

### Added

- Additional classnames can be specified using `directive.classname` syntax
- Support removing the title bar entirely

### Fixed

- Removed superfluous empty `<p>` tags in output

## 1.3.3

### Fixed

- Fixed compilation failure with no default features
- MSRV (minimum supported rust version) documented as 1.58.0

## 1.3.2

### Fixed

- Fixed incorrect admonition title/panic when terminating with non-ascii characters
- Updated readme to note double-JSON string escapes

## 1.3.1

### Fixed

- Flattened indentation of generated HTML, otherwise it's styled as a markdown code block
- Fixed edge cases where the info string changes length when parsed, causing title/body to be incorrectly split

## 1.3.0

### Added

- Add additional examples and images in readme
- Allow markdown styling in title content

### Fixed

- Fix HTML being stripping from body content

## 1.2.0

### Added

- Support custom title text

## 1.1.0

### Added

- CSS rules for the builtin mdbook themes, to adjust card background color

## 1.0.1

### Fixed

- Crate metadata and README wording

## 1.0.0

### Added

- `admonish <admonition type>` support for code fences
- Admonition type support is parity with mkdocs as of release
