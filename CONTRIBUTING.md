# Contributing to Kaappi

Thanks for your interest in contributing! All kaappi repositories are MIT
licensed and contributions are welcome.

## Start with Discussions

**[GitHub Discussions](https://github.com/orgs/kaappi/discussions)** is the
entry point for new contributors. Use it to ask questions, report bugs,
propose features, or introduce yourself.

Issues and pull requests across all kaappi repos are restricted to members of
the [kaappi GitHub org](https://github.com/kaappi). If you'd like to
contribute directly, ask for an invite in Discussions — we're happy to add
anyone who's genuinely interested.

## Getting started

1. Introduce yourself or start a conversation in
   [Discussions](https://github.com/orgs/kaappi/discussions).
2. Once you have org access, fork the repository and clone it locally.
3. Follow the **README** in the specific repo for build and test instructions.
4. For the core interpreter, see the
   [kaappi/kaappi CONTRIBUTING guide](https://github.com/kaappi/kaappi/blob/main/CONTRIBUTING.md)
   for Zig-specific setup.

## Workflow

1. Create a branch from `main`.
2. Make your changes and add tests where applicable.
3. Run the test suite (`zig build test` for core, or the Scheme test files for
   ecosystem libraries).
4. Open a pull request against `main`.

## Code style

- **Zig** (core): follow `zig fmt` — CI enforces this.
- **Scheme** (libraries): standard R7RS style with 2-space indentation.
- **Commits**: short imperative subject line, optional body explaining _why_.

## Reporting bugs

Post in [Discussions](https://github.com/orgs/kaappi/discussions) with the
Kaappi version (`kaappi --version`), your platform, and a minimal
reproduction. Org members can also open issues directly.

## Questions

Start a thread in
[GitHub Discussions](https://github.com/orgs/kaappi/discussions).
