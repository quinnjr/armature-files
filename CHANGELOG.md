# Changelog — `armature-files`

All notable changes to this crate will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this crate adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

Earlier changes are recorded in the workspace [`CHANGELOG.md`](../CHANGELOG.md).

## [Unreleased]

## [0.3.0] - 2026-10-17

### Security

- **Breaking:** `zip` upgraded 8.6 → 9.0.4, fixing RUSTSEC-2026-0367, RUSTSEC-2026-0368 and RUSTSEC-2026-0369. The crate never used zip's own `extract` family; `ZipExtractor` keeps its custom path-traversal (`enclosed_name`), entry-count and uncompressed-size protections. `zip` types do not appear in this crate's public API, but the major bump changes the dependency tree.

## [0.2.2] - 2026-09-15

### Changed

- Dependencies bumped to their latest releases: `lopdf` 0.43 → 0.45, `tokio` 1.52 → 1.53, `lopdf` 0.43 → 0.45, `tokio` 1.52 → 1.53.
- Migrate to upgraded dependencies.

