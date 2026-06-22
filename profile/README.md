<p align="center">
  <img src="https://kaappi.github.io/assets/logo.svg" width="140" alt="Kaappi">
</p>

<h3 align="center">Kaappi — R7RS Scheme, brewed in Zig</h3>

<p align="center">
  A complete <strong>R7RS-small</strong> Scheme implementation with a JIT compiler, C FFI, OS threads, and a curated package ecosystem.
</p>

<p align="center">
  <a href="https://kaappi.github.io/guide/">Get Started</a> · <a href="https://kaappi.github.io/procedures/">Procedures</a> · <a href="https://kaappi.github.io/ecosystem/">Ecosystem</a> · <a href="https://kaappi.github.io/">Docs</a>
</p>

---

### The runtime

[**kaappi/kaappi**](https://github.com/kaappi/kaappi) is the core interpreter — ~39 000 lines of Zig implementing every identifier from R7RS Appendix A: 600+ built-in procedures, 33 syntax forms, all 14 standard libraries, and 51 SRFIs. Hot functions JIT-compile to native AArch64/x86_64. First-class `call/cc`, hygienic macros, green fibers, OS threads, a stepping debugger, a profiler, and sandbox mode are all built in.

### Ecosystem packages

Installable via [**thottam**](https://kaappi.github.io/ecosystem/thottam/), the Kaappi package manager.

| Package | What it does |
|---|---|
| [kaappi-http](https://github.com/kaappi/kaappi-http) | HTTP/1.1 client and server (pre-fork, threaded) |
| [kaappi-web](https://github.com/kaappi/kaappi-web) | Web framework — routes, middleware, JSON helpers |
| [kaappi-pg](https://github.com/kaappi/kaappi-pg) | PostgreSQL client (libpq, parameterized queries, cursors) |
| [kaappi-redis](https://github.com/kaappi/kaappi-redis) | Redis client (RESP2, pipelining, pub/sub) |
| [kaappi-json](https://github.com/kaappi/kaappi-json) | RFC 8259 JSON parser and serializer |
| [kaappi-net](https://github.com/kaappi/kaappi-net) | TCP/TLS networking (shared by http, redis, pg) |
| [kaappi-cli](https://github.com/kaappi/kaappi-cli) | CLI framework — arg parsing, subcommands, auto help |
| [kaappi-examples](https://github.com/kaappi/kaappi-examples) | Example apps: REST API, task queue, CRUD, file server |

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

| | macOS aarch64 | Linux x86_64 | Linux aarch64 | Linux riscv64 |
|---|:---:|:---:|:---:|:---:|
| Build + tests | yes | yes | yes | yes |
| JIT | AArch64 | x86_64 | AArch64 | — |

### Links

- [Documentation](https://kaappi.github.io/) — user guide, procedure reference, ecosystem docs
- [Benchmarks](https://kaappi.github.io/benchmarks/) — fib, tak, triangular against Chez, Gauche, Chibi
- [Library authoring guide](https://kaappi.github.io/libraries/) — R7RS `define-library`, SRFIs, bytecode caching

<p align="center"><sub>MIT License — built with Zig</sub></p>
