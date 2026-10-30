<div align="center">

# Suzuki Taro

<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/rust/rust-original.svg" alt="Rust" width="64" height="64" />

### Rust · Systems Programming · Distributed Systems

**Correctness by design. Performance by measurement. Reliability under pressure.**

[![Rust](https://img.shields.io/badge/Rust-Systems_Programming-CE422B?style=flat-square&logo=rust&logoColor=white)](https://www.rust-lang.org/)
[![Tokio](https://img.shields.io/badge/Async-Tokio_%2F_Futures-24292F?style=flat-square)](https://tokio.rs/)
[![Linux](https://img.shields.io/badge/Linux-Tooling-24292F?style=flat-square&logo=linux&logoColor=white)](https://kernel.org/)
[![GitHub](https://img.shields.io/badge/GitHub-sharmis--tp-24292F?style=flat-square&logo=github&logoColor=white)](https://github.com/sharmis-tp)

<p align="center">
  <a href="https://github.com/sharmis-tp" title="Profile views">
    <img src="https://komarev.com/ghpvc/?username=sharmis-tp&label=PROFILE%20VIEWS&color=CE422B&style=for-the-badge" alt="Profile views" height="28" />
  </a>
  &nbsp;
  <a href="https://github.com/sharmis-tp?tab=followers" title="Followers">
    <img src="https://img.shields.io/github/followers/sharmis-tp?style=for-the-badge&logo=github&logoColor=white&label=FOLLOWERS&labelColor=24292F&color=CE422B" alt="GitHub followers" height="28" />
  </a>
</p>

</div>

---

## `whoami`

I'm a software engineer focused on **Rust, systems programming, async services, and performance-conscious backend architecture**.

I care about more than getting code past the borrow checker. I care about the guarantees behind it: **who owns a resource, which invariants hold across a state transition, what cancellation leaves behind, and how a service behaves when something fails at the worst possible moment.**

> I borrow ideas. I own results.

## Areas of depth

| Domain | What I pay attention to |
| :--- | :--- |
| **Ownership & lifetimes** | Borrowing, API lifetime design, interior mutability, move semantics, resource lifecycles |
| **Type-driven APIs** | Traits, generics, enums, newtypes, typestate, errors that express actionable failure |
| **Async & concurrency** | Tokio, futures, `Send` / `Sync`, task supervision, cancellation safety, backpressure |
| **Memory & performance** | Heap allocation, cache behavior, memory layout, benchmarks, zero-copy trade-offs |
| **FFI & unsafe Rust** | ABI compatibility, raw pointers, aliasing, safety invariants, safe public wrappers |
| **Networking & protocols** | Framing, parsing, versioning, timeouts, connection lifecycle, partial I/O |
| **Production reliability** | Tracing, structured errors, graceful shutdown, deterministic tests, fault isolation |

## The engineering questions I ask

```rust
// Before adding a new abstraction or optimizing a hot path:
//
// 1. Which invariants must remain true?
// 2. Who owns the data, and how long must it live?
// 3. Can this operation block, panic, or be cancelled?
// 4. Is concurrency bounded? Where is backpressure applied?
// 5. Which allocations or copies are actually measurable?
// 6. How will failure be observed, reproduced, and recovered?
```

## Selected repositories

These are **Rust and systems-oriented codebases available on my account**. Some may be forks or explorations; the repository history is the source of truth for individual contributions.

| Repository | What makes it technically interesting |
| :--- | :--- |
| [**Dbgeng-sys**](https://github.com/sharmis-tp/Dbgeng-sys) | Low-level Rust bindings, foreign interfaces, ABI considerations |
| [**napi-rs**](https://github.com/sharmis-tp/napi-rs) | Rust ↔ Node.js FFI, ownership across language boundaries |
| [**swc**](https://github.com/sharmis-tp/swc) | High-performance parsing, transforms, compiler infrastructure |
| [**deno**](https://github.com/sharmis-tp/deno) | Rust runtime architecture, asynchronous I/O, developer tooling |
| [**cross**](https://github.com/sharmis-tp/cross) | Rust cross-compilation and reproducible build environments |
| [**slint**](https://github.com/sharmis-tp/slint) | Native UI systems, declarative components, Rust integration |

## How I build systems

**01 — Make invariants visible.** Prefer expressive types, explicit state transitions, and narrow interfaces over comments that merely ask callers to be careful.

**02 — Treat async as a resource-management problem.** Spawned tasks still need owners. Queues need limits. Cancellation, timeouts, and graceful shutdown should be intentional.

**03 — Keep unsafe code small and auditable.** `unsafe` does not switch off correctness requirements; it transfers the obligation to document and uphold them.

**04 — Profile before optimizing.** Throughput, tail latency, allocations, and contention matter more than assumptions about what "should" be faster.

**05 — Test the failure paths.** Validate malformed inputs, partial reads, retries, timeouts, state recovery, and boundary conditions—not just successful execution.

## Tools & technologies

`Rust` · `Cargo` · `rustfmt` · `Clippy` · `Tokio` · `Serde` · `tracing` · `Linux` · `Git` · `Docker` · `CI`

Also comfortable working across language boundaries with **C/C++, TypeScript, Go, and Python**.

---

<div align="center">

**Rust · Reliable Software · Thoughtful Systems Design**

[Explore repositories](https://github.com/sharmis-tp?tab=repositories)

<sub>Build software that stays understandable under load, under failure, and under review.</sub>

</div>
