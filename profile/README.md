<p align="center">
  <img src="https://kaappi-lang.org/assets/logo.svg" width="140" alt="Kaappi">
</p>

<h3 align="center">Kaappi — R7RS Scheme, brewed in Zig</h3>

<p align="center">
  A complete <strong>R7RS-small</strong> Scheme implementation with an LLVM native compiler, C FFI, OS threads, and a curated package ecosystem.
</p>

<p align="center">
  <a href="https://kaappi-lang.org/guide/">Get Started</a> · <a href="https://kaappi-lang.org/procedures/">Procedures</a> · <a href="https://kaappi-lang.org/ecosystem/">Ecosystem</a> · <a href="https://kaappi-lang.org/playground/">Playground</a> · <a href="https://kaappi-lang.org/">Docs</a>
</p>

---

### The runtime

[**kaappi/kaappi**](https://github.com/kaappi/kaappi) is the core interpreter — written in Zig, implementing every identifier from R7RS Appendix A plus all 14 standard libraries and a broad set of SRFIs. The LLVM native backend compiles Scheme to standalone binaries on AArch64/x86_64. First-class `call/cc`, hygienic macros, green fibers, OS threads, a stepping debugger, a profiler, sandbox mode, and a built-in [LSP server](https://kaappi-lang.org/guide/editor-support/) are all included.

### Ecosystem packages

Installable via [**thottam**](https://kaappi-lang.org/ecosystem/thottam/), the Kaappi package manager.

| Package | What it does |
|---|---|
| [kaappi-http](https://github.com/kaappi/kaappi-http) | HTTP/1.1 client and server (pre-fork, threaded) |
| [kaappi-web](https://github.com/kaappi/kaappi-web) | Web framework — routes, middleware, JSON helpers |
| [kaappi-pg](https://github.com/kaappi/kaappi-pg) | PostgreSQL client (libpq, parameterized queries, cursors) |
| [kaappi-redis](https://github.com/kaappi/kaappi-redis) | Redis client (RESP2, pipelining, pub/sub) |
| [kaappi-json](https://github.com/kaappi/kaappi-json) | RFC 8259 JSON parser and serializer |
| [kaappi-net](https://github.com/kaappi/kaappi-net) | TCP/TLS networking (shared by http, redis, pg) |
| [kaappi-sqlite](https://github.com/kaappi/kaappi-sqlite) | SQLite bindings (DB-API, parameterized queries) |
| [kaappi-crypto](https://github.com/kaappi/kaappi-crypto) | Cryptography (OpenSSL — hashing, HMAC, random) |
| [kaappi-email](https://github.com/kaappi/kaappi-email) | Email (MIME construction, SMTP) |
| [kaappi-cli](https://github.com/kaappi/kaappi-cli) | CLI framework — arg parsing, subcommands, auto help |

Plus [csv](https://github.com/kaappi/kaappi-csv), [yaml](https://github.com/kaappi/kaappi-yaml), [toml](https://github.com/kaappi/kaappi-toml), [log](https://github.com/kaappi/kaappi-log), [template](https://github.com/kaappi/kaappi-template), [test](https://github.com/kaappi/kaappi-test), [bdd](https://github.com/kaappi/kaappi-bdd), and [examples](https://github.com/kaappi/kaappi-examples).

### Quick taste

```scheme
(import (scheme base) (scheme write))

(define (fib n)
  (if (< n 2) n
      (+ (fib (- n 1))
         (fib (- n 2)))))

(display (fib 30))  ;=> 832040
```

### Platforms

| | macOS aarch64 | Linux x86_64 | Linux aarch64 | Linux riscv64 | WebAssembly |
|---|:---:|:---:|:---:|:---:|:---:|
| Build + tests | yes | yes | yes | yes | yes |
| Native compiler | AArch64 | x86_64 | AArch64 | — | — |

### Links

- [Documentation](https://kaappi-lang.org/) — user guide, procedure reference, ecosystem docs
- [Playground](https://kaappi-lang.org/playground/) — browser REPL powered by `kaappi.wasm`
- [Tour](https://kaappi-lang.org/tour/) — 12-lesson guided tour with live code

<p align="center"><sub>MIT License — built with Zig</sub></p>
