# 3 Leaps Ecosystem GitHub Templates

This directory contains standardized GitHub issue templates and PR templates for all 3 Leaps OSS organizations and projects (fulmenhq, mdmeld, docemist, etc.). These templates provide a consistent experience across our ecosystem while allowing project-specific customization.

## Purpose

- **Consistency**: Unified issue/PR structure across all 3 Leaps organizations (fulmenhq, mdmeld, docemist, etc.)
- **Quality**: Ensure reporters provide necessary information for triage
- **Maintainability**: Update templates in one place, sync to all projects
- **Community**: Guide new contributors through the contribution process

## Templates Included

### Issue Templates

1. **bug_report.yml** - Structured bug reports with environment details
2. **feature_request.yml** - Feature proposals with use cases and priority
3. **question.yml** - Questions and discussions
4. **config.yml** - Template configuration and contact links

### Pull Request Template

- **PULL_REQUEST_TEMPLATE.md** - Comprehensive PR checklist covering testing, documentation, security, and quality

## How to Use These Templates

### Option 1: Direct Copy (Recommended for Most Projects)

Copy the `.github/` directory to your project repository:

```bash
# From your project root
cp -r ~/dev/3leaps/oss-policies/.github .
```

Then customize as needed (see Customization section below).

### Option 2: Symbolic Link (Advanced)

For projects that want automatic updates, create a symlink:

```bash
# From your project root
ln -s ~/dev/3leaps/oss-policies/.github .github
```

**Note**: This requires the oss-policies repo to be cloned locally. Not recommended for public projects as paths may vary across contributors.

### Option 3: Manual Sync

1. Copy templates to your project
2. Add a comment at the top noting they're synced from oss-policies
3. Periodically check oss-policies for updates and re-sync

## Customization Guide

All templates include comments at the top indicating what should be customized. Here's what to customize for each project:

### Bug Report Template

**File**: `ISSUE_TEMPLATE/bug_report.yml`

**Customize**:
- Line 2: `description` - Add project name
- Lines 26-29: `reproduction` placeholder - Add project-specific example
- Line 54: `version` label - Change "Version" to "ProjectName Version" if desired
- Line 117-119: `checklist` - Update version references

**Example for TSFulmen**:
```yaml
description: Report a bug or unexpected behavior in TSFulmen
# ...
placeholder: |
  1. Install TSFulmen v0.1.x
  2. Import module '...'
# ...
label: TSFulmen Version
```

**Example for GoFulmen**:
```yaml
description: Report a bug or unexpected behavior in GoFulmen
# ...
placeholder: |
  1. Install GoFulmen: go get github.com/fulmenhq/gofulmen
  2. Import package '...'
# ...
label: GoFulmen Version
```

### Feature Request Template

**File**: `ISSUE_TEMPLATE/feature_request.yml`

**Customize**:
- Line 2: `description` - Add project-specific note about status (alpha, stable, etc.)
- Add module/component dropdown if applicable (see TSFulmen example below)

**Example module dropdown for library projects**:
```yaml
  - type: dropdown
    id: module
    attributes:
      label: Related Module
      description: Which module is this feature related to?
      options:
        - config
        - logging
        - schema
        - other
```

### Question Template

**File**: `ISSUE_TEMPLATE/question.yml`

**Customize**:
- Line 2: `description` - Add project name if desired
- Add module/component dropdown if applicable (same as feature request)

### Config Template

**File**: `ISSUE_TEMPLATE/config.yml`

**Customize**:
- Line 8: Documentation URL - Update to project-specific docs
- Line 13: Discussions URL - Update to project-specific discussions
- Consider adding project-specific contact links (e.g., Mattermost channel)

**Example for TSFulmen**:
```yaml
contact_links:
  - name: 📖 Documentation
    url: https://github.com/fulmenhq/tsfulmen
    about: Read the TSFulmen documentation and examples
  - name: 🔒 Security Vulnerability
    url: https://github.com/fulmenhq/tsfulmen/blob/main/SECURITY.md
    about: Report security vulnerabilities privately via security@3leaps.net
  - name: 💬 GitHub Discussions
    url: https://github.com/fulmenhq/tsfulmen/discussions
    about: Ask questions and discuss TSFulmen with the community
```

### Pull Request Template

**File**: `PULL_REQUEST_TEMPLATE.md`

**Customize**:
- Quality checks section - Update commands to match project (e.g., `make test`, `npm test`, `go test`)
- Documentation references - Update paths to project-specific CONTRIBUTING.md
- Add project-specific sections if needed (e.g., cross-language alignment for helper libraries)

**Example quality checks**:
```markdown
## Quality Checks

- [ ] `make check-all` passes (lint, typecheck, test)  <!-- TypeScript/Node -->
- [ ] `go test ./...` passes                           <!-- Go -->
- [ ] `pytest` passes with coverage                    <!-- Python -->
- [ ] Build succeeds
```

## Project-Specific Examples

### TSFulmen (TypeScript Library)

TSFulmen customizes templates with:
- Module dropdown listing all TSFulmen modules (config, logging, pathfinder, etc.)
- Runtime environment dropdown (Node.js, Bun)
- Alpha status note in feature request
- TypeScript-specific quality checks in PR template

### GoFulmen (Go Library)

GoFulmen should customize with:
- Module dropdown for Go modules
- Go version and environment details
- Go-specific quality checks (`go test`, `golangci-lint`)

### PyFulmen (Python Library)

PyFulmen should customize with:
- Module dropdown for Python modules
- Python version and environment details
- Python-specific quality checks (`pytest`, `mypy`, `ruff`)

### Crucible (SSOT Repository)

Crucible should customize with:
- Category dropdown (schemas, docs, config, templates)
- Asset type information
- Sync and versioning considerations

## Syncing Updates

When templates are updated in oss-policies:

1. **Announcement**: Update CHANGELOG.md in oss-policies with template changes
2. **Notification**: Notify project maintainers via Mattermost or GitHub
3. **Manual Sync**: Each project maintainer reviews changes and updates their copy
4. **Version Tracking**: Update "Last synced" comment in template headers

## Template Design Principles

1. **Required vs Optional**: Mark truly required fields as `required: true`, make others optional
2. **Clear Labels**: Use descriptive labels and help text
3. **Reasonable Defaults**: Provide good placeholder examples
4. **Progressive Disclosure**: Start simple, add details as needed
5. **Accessibility**: Use clear language, avoid jargon in field descriptions
6. **Consistency**: Keep field names and structure consistent across templates

## Testing Templates

Before syncing templates to a project:

1. Create a test issue in your project using each template
2. Verify all fields render correctly
3. Test required field validation
4. Check dropdown options display properly
5. Ensure customized sections make sense for your project

## Questions or Improvements

For questions about these templates or to suggest improvements:
- Open an issue in [3leaps/oss-policies](https://github.com/3leaps/oss-policies)
- Contact: legal@3leaps.net

## Version History

- **2025-11-03**: Initial templates established (based on TSFulmen v0.1.4 public release)

---

**Status**: Active
**Maintained By**: 3 Leaps, LLC
**License**: Same as oss-policies (see [LICENSE.md](../LICENSE.md))
