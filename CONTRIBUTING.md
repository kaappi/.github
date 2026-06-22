# Contributing to Kaappi

Thanks for your interest in contributing! All kaappi repositories are MIT
licensed and contributions are welcome.

## Getting started

1. Fork the repository and clone it locally.
2. Follow the **README** in the specific repo for build and test instructions.
3. For the core interpreter, see the
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

Open an issue in the affected repository using the bug report template. Include
the Kaappi version (`kaappi --version`), your platform, and a minimal
reproduction.

## Questions

Open a GitHub issue with the question label, or start a discussion on the
[kaappi/kaappi](https://github.com/kaappi/kaappi) repository.
