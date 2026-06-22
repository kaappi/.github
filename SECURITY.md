# Security Policy

## Reporting a vulnerability

If you discover a security vulnerability in any kaappi repository, please report
it through GitHub's
[private security advisory](https://docs.github.com/en/code-security/security-advisories/guidance-on-reporting-and-writing-information-about-vulnerabilities/privately-reporting-a-security-vulnerability)
feature on the affected repository.

Please do **not** open a public issue for security vulnerabilities.

## Scope

This policy applies to all repositories in the
[kaappi](https://github.com/kaappi) organization, including the core
interpreter, ecosystem libraries, and tooling.

## Sandbox mode

The core interpreter provides a `--sandbox` flag that disables FFI, file I/O,
`eval`, `load`, and environment variable access. If you are running untrusted
Scheme code, use sandbox mode.
