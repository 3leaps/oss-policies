# 3 Leaps OSS Policies Repository

This repository (`oss-policies`) is the central source of truth for the policies governing the open-source work of [3 Leaps, LLC](https://3leaps.net). These policies apply to **all repository organizations owned and/or substantially supported by 3 Leaps, LLC**. The current organizations include:

- [fulmenhq](https://github.com/fulmenhq)
- [mdmeld](https://github.com/mdmeld)
- [docemist](https://github.com/docemist)
- [namelens](https://github.com/namelens)
- [verilis](https://github.com/verilis)
- [enacthq](https://github.com/enacthq)
- [lanytehq](https://github.com/lanytehq)

This list is illustrative, not exhaustive — the policies apply to any such organization whether or not it is named above. These policies are synced automatically to relevant repositories via GitHub Actions to ensure consistency across our ecosystem.

## Purpose

- **Centralized Management**: All policy updates happen here in the [3leaps](https://github.com/3leaps) org, with contributions often originating from core maintainers (e.g., @3leapsdave).
- **Automated Syncing**: Changes are pushed to downstream repos in our maintained orgs. We actively support these OSS projects through funding, consulting, and maintenance as part of our community work, and these policies apply collaboratively to ensure fair and consistent governance.
- **Scope**: Covers trademarks, contributions, code of conduct, and more for our consulting-driven OSS projects.

## Policies

The governing documents. Repos conform by citing the relevant policy specifically
in their role prompts/ADRs (not a generic "follow all policies" line). This set
grows as governance needs evolve — propose additions via [CONTRIBUTING.md](CONTRIBUTING.md).

| Policy | Scope |
|---|---|
| [Trademark Policy](TRADEMARK-POLICY.md) | Using 3 Leaps marks and names in OSS work |
| [Sensitive Local Data](SENSITIVE-LOCAL-DATA.md) | Keeping proprietary/identifying material out of repo surfaces (`.gitignore` is not a security boundary) |

## Governance & community health

| Document | Purpose |
|---|---|
| [Code of Conduct](CODE-OF-CONDUCT.md) | Expected behavior in our communities |
| [Security Policy](SECURITY.md) | Reporting security issues (public keys in [`keys/`](keys/)) |
| [Contributing](CONTRIBUTING.md) | How to propose changes to these documents |
| [Support](SUPPORT.md) | Getting help and support resources |
| [License](LICENSE.md) | Licensing of these documents |

## Meta & templates

| Item | Purpose |
|---|---|
| [Changelog](CHANGELOG.md) | History of updates |
| [.github/](.github/) | Shared issue/PR templates synced across the ecosystem |

For questions or suggestions, open an issue in this repo. Contributions welcome—see [CONTRIBUTING.md](CONTRIBUTING.md).

Last updated: 2026-06-28
