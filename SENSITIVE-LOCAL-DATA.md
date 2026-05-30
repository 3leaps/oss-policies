# 3 Leaps Open Source — Sensitive Local Data Policy

## Purpose

This is the canonical, public statement of how 3 Leaps keeps proprietary and
user data out of its open-source repositories. Each 3 Leaps OSS repo references
this policy rather than copying it, so the statement stays consistent and
updates propagate from one place. A repo conforms by declaring conformance and,
where useful, recording repo-specific implementation in its own architecture
decision records and local (non-published) operator notes.

## Policy statement

The tools, applications, processes, and documentation in our open-source
repositories are implemented and maintained so as to be free of any specific
reference to proprietary data, or to any entity that might use them. We
implement standards and processes to help ensure the OSS repositories remain
free of such artifacts and references.

It is our policy to:

- **Keep proprietary material separate.** Proprietary implementation notes,
  test cases, recipes, fixtures, and references are maintained apart from the
  open-source surface.
- **Keep such material outside the repository surface.** In the course of
  maintaining and extending our OSS repositories, we keep this material outside
  of the repository entirely. It is not sufficient to `.gitignore` a
  proprietary file — any such artifact is maintained outside the repository's
  folder space, so that it cannot be committed by accident.

It is acceptable to reference required external information by location: use
environment variables or the other mechanisms described in our CI/CD and
general documentation to point at files or folders that hold such information,
rather than placing the information itself in the repository.

This extends to `.env` files. While we follow industry practice and support
`.env` files in certain cases, our practice is to use them for **secrets by
reference** — pointing at where a secret lives — rather than embedding secret
or proprietary values directly.

**A rule of thumb:** a mistaken change to a `.gitignore` file must not result in
the leak of any of our users' information through an unintended commit. Because
`.gitignore` is a convenience filter and not a security boundary, the data it
would have hidden lives outside the repository in the first place.

In the event that, despite these policies and processes, such information is
nonetheless exposed, we will work in good faith to remove it promptly.

## Scope

This policy concerns the _relationship and context clues_ an organization
defines as confidential — client, customer, project, or person identifiers;
engagement codenames; proprietary data samples and derived fixtures; and any
artifact that reveals private names or operational structure. It complements,
and is distinct from, secrets/credential scanning and regulated-PII handling.

## How repositories conform

- **Declare conformance.** A repo states that it complies with this policy
  (for example in its `AGENTS.md` or contributor documentation).
- **Make the rule concrete where work happens.** Conformance is not achieved by
  a generic "follow all policies" line — such references are easily missed. A
  repo records the rule specifically in the places contributors and agents
  actually read (architecture decision records, agent/role prompts), stated as
  a clear principle rather than a catalog of forbidden names.
- **Keep implementation detail out of the public surface.** Concrete local
  locations, tooling configuration, and any enforcement mechanics belong in a
  repo's local (non-published) operator notes, not in published files — so the
  public surface states the policy without describing internal process in a way
  that would itself reveal private structure.

---

_Canonical policy. Repos link here rather than copying. Last updated: 2026-05-30._
