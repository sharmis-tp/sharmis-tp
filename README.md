# sharmis-tp

<div align="center">

<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/rust/rust-original.svg" alt="Rust" width="64"/>

### Rust · Systems Engineering · Blockchain Infrastructure

**Engineering for correctness, predictable performance, and clearly defined failure modes.**

[![Rust](https://img.shields.io/badge/Rust-Systems_Engineering-CE422B?style=flat-square&logo=rust&logoColor=white)](https://www.rust-lang.org/)
[![Solana](https://img.shields.io/badge/Solana-On--Chain_Programs-242038?style=flat-square)](https://solana.com/)
[![Tokio](https://img.shields.io/badge/Async-Tokio_%2F_Futures-234a73?style=flat-square)](https://tokio.rs/)

<p align="center">
  <a href="https://github.com/sharmis-tp"><img src="https://komarev.com/ghpvc/?username=sharmis-tp&label=PROFILE%20VIEWS&color=CE422B&style=for-the-badge" alt="Profile Views" height="28"/></a>
  &nbsp;
  <a href="https://github.com/sharmis-tp?tab=followers"><img src="https://img.shields.io/github/followers/sharmis-tp?style=for-the-badge&logo=github&logoColor=white&label=FOLLOWERS&labelColor=24292F&color=CE422B" alt="Followers" height="28"/></a>
</p>

</div>

---

## `whoami`

I'm a software engineer focused on **Rust, distributed systems, and blockchain infrastructure**, working across on-chain programs, networked services, runtime integration, and full-stack applications.

My interest in Rust goes beyond satisfying the borrow checker. I care about the contracts a system must preserve: resource ownership, state transitions, cancellation and partial failure, and well-defined behavior at system boundaries.

```rust
// Questions worth answering before optimizing a system:
//
// 1. What invariants must always hold?
// 2. Where are ownership and mutation boundaries?
// 3. What can fail, block, panic, or be cancelled?
// 4. Where are allocations, copies, and contention introduced?
// 5. How are failure paths tested?
```

## Rust engineering: areas of focus

| Area | Engineering considerations |
| :--- | :--- |
| **Ownership & lifetimes** | Borrowing, API lifetimes, interior mutability, resource management |
| **Type-driven design** | Newtypes, enums, traits, generics, domain invariants |
| **Async & concurrency** | Futures, Tokio, cancellation safety, `Send`/`Sync`, backpressure |
| **Memory & performance** | Memory layout, allocations, profiling, zero-copy trade-offs |
| **FFI & systems** | ABI contracts, raw pointers, safe abstractions around `unsafe` |
| **Protocol engineering** | Deterministic execution, serialization, transaction semantics |
| **Reliability** | Structured errors, tracing, reproducible tests, failure recovery |

## Selected repositories

A curated selection of repositories on this account. Individual contribution and authorship history can be inspected in their commits and pull requests.

| Repository | Technical focus |
| :--- | :--- |
| [Dbgeng-sys](https://github.com/sharmis-tp/Dbgeng-sys) | Rust FFI and Windows debugging interfaces |
| [napi-rs](https://github.com/sharmis-tp/napi-rs) | Rust–Node.js native bindings |
| [raydium-cp-swap](https://github.com/sharmis-tp/raydium-cp-swap) | Solana AMM program architecture |
| [whirlpool-tx-replayer](https://github.com/sharmis-tp/whirlpool-tx-replayer) | Concentrated liquidity and transaction replay |
| [agave](https://github.com/sharmis-tp/agave) | Solana validator and runtime architecture |
| [ic](https://github.com/sharmis-tp/ic) | Internet Computer canister infrastructure |
| [subtensor](https://github.com/sharmis-tp/subtensor) | Substrate runtime and state transitions |
| [hyperbridge](https://github.com/sharmis-tp/hyperbridge) | Cross-chain interoperability |

## Engineering philosophy

### 01 / Make invalid states difficult to represent

Use domain types rather than loosely coupled primitives. Model state transitions explicitly and make trust boundaries visible in function signatures.

### 02 / Treat concurrency as resource management

Async does not automatically mean scalable. Task ownership, cancellation, bounded queues, timeouts, contention, and graceful shutdown all matter.

### 03 / Make unsafe boundaries explicit

`unsafe` is not a performance switch. Keep unsafe surfaces small, document their invariants, and expose safe abstractions wherever possible.

### 04 / Measure before optimizing

Distinguish throughput from tail latency. Profile allocation behavior, copying, and contention using realistic workloads before choosing a more complex implementation.

### 05 / Engineer for adversarial conditions

In distributed systems and blockchains, correctness depends on authority boundaries, replay resistance, idempotency, consistent state transitions, and failure recovery.

## Rust × Blockchain

- **Solana / Anchor:** PDAs, CPIs, account validation, token programs, deterministic state transitions, compute budgets.
- **Internet Computer:** Rust canisters, Candid, ledger interfaces, state upgrades, inter-canister calls.
- **Substrate:** Runtime modules, storage models, dispatch logic, transaction weights.
- **Cross-chain systems:** Message validation, finality assumptions, settlement and trust models.

I approach on-chain programs as **state machines exposed to adversarial inputs**, not merely functions deployed to a blockchain.

## Tooling

`Rust` · `Cargo` · `Clippy` · `rustfmt` · `Tokio` · `Serde` · `tracing` · `Anchor` · `Solana` · `Candid` · `Linux` · `Docker`

Also working across **TypeScript, Go, Python, C/C++, Move, and Solidity**.

## Principles

> Correctness before cleverness. Explicit invariants before abstraction. Measurement before optimization.

- Keep safety contracts explicit.
- Prefer deterministic and reproducible tests.
- Make failures observable and recoverable.
- Design for maintenance, not just initial implementation.
- Keep the distinction between demonstrated contributions and explored technologies clear.

---

<div align="center">

**Rust · Protocols · Distributed Systems**

[Explore my repositories](https://github.com/sharmis-tp?tab=repositories)

<sub>Build things that remain understandable under load, under failure, and under review.</sub>

</div>
