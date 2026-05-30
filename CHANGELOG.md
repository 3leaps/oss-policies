# Changelog

All notable changes to the 3 Leaps OSS Policies repository will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html) for policy updates.

## [Unreleased]

### Added

- SENSITIVE-LOCAL-DATA.md: Canonical policy for keeping proprietary/user data out of OSS repositories — sensitive material lives outside the repository tree (`.gitignore` is a convenience filter, not a security boundary); reference external files by location; `.env` holds secrets by reference. Repos conform by declaring conformance and recording the rule as a principle in their ADRs/role prompts.
- TRADEMARK-POLICY.md: Project-name guidance for sysprims, docprims, sfetch, and seclusor.

### Fixed

- README.md: Corrected the Code of Conduct link target to `CODE-OF-CONDUCT.md` (matched the actual filename).

## [1.0.0] - 2025-08-04

Initial stable release of the oss-policies repository.

### Added

- README.md: Repo overview, purpose, key documents, and sync process.
- TRADEMARK-POLICY.md: Guidelines for using 3 Leaps trademarks, including Fulmen, MDMeld, and Docemist marks/logos.
- CONTRIBUTING.md: Instructions for suggesting policy changes.
- LICENSE.md: Proprietary notice for policy documents.
- CODE_OF_CONDUCT.md: Standard Contributor Covenant, customized for OSS and proprietary contexts.
- SECURITY.md: Vulnerability reporting policy with PGP encryption support.

### Changed

- N/A (Initial release).

### Fixed

- N/A (Initial release).

[1.0.0]: https://github.com/3leaps/oss-policies/releases/tag/v1.0.0
