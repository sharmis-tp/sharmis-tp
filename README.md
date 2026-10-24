<div align="center">

# sharmis-tp

<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/rust/rust-original.svg" alt="Rust logo" width="64" height="64" />

### Rust · Systems Engineering · Blockchain Infrastructure

**Engineering for correctness, predictable performance, and clearly defined failure modes.**

[![Rust](https://img.shields.io/badge/Rust-systems%20engineering-000000?style=flat-square&logo=rust&logoColor=white)](https://www.rust-lang.org/)
[![Solana](https://img.shields.io/badge/Solana-on--chain%20programs-242038?style=flat-square)](https://solana.com/)
[![Async](https://img.shields.io/badge/Async-Tokio%20%2F%20futures-234a73?style=flat-square)](https://tokio.rs/)
[![GitHub](https://img.shields.io/badge/GitHub-sharmis--tp-181717?style=flat-square&logo=github)](https://github.com/sharmis-tp)

</div>

---

## `whoami`

I'm a software engineer focused on **Rust, distributed systems, and blockchain infrastructure**, with experience working across on-chain programs, networked services, runtime integration, and full-stack applications.

My interest in Rust goes beyond writing code that passes the borrow checker. I care about the contracts a system must preserve: who owns each resource, where state can change, what happens under cancellation or partial failure, which operations can block, and how the implementation behaves at its boundaries.

```rust
// The questions I ask before optimizing a system:
//
// 1. What invariants must always hold?
// 2. Where are ownership and mutation boundaries?
// 3. What can fail, block, panic, or be cancelled?
// 4. Where are allocations, copies, and contention introduced?
// 5. How do we test the failure paths, not just the happy path?
```

## Rust engineering: areas of focus

| Area | What matters in practice |
| :--- | :--- |
| **Ownership & lifetimes** | Explicit resource ownership, borrowing, API lifetimes, interior mutability, and avoiding unnecessary cloning |
| **Type-driven design** | Newtypes, enums, traits, generics, state transitions, domain invariants, and errors that callers can act on |
| **Async & concurrency** | Futures, Tokio, task lifecycles, cancellation safety, `Send`/`Sync`, backpressure, and bounded concurrency |
| **Memory & performance** | Allocation behavior, layout, zero-copy trade-offs, profiling, benchmarking, and avoiding premature `unsafe` |
| **FFI & low-level interfaces** | ABI boundaries, raw pointers, layout assumptions, lifetime contracts, and keeping unsafe surface area small |
| **Protocol engineering** | Serialization formats, deterministic execution, versioning, replay resistance, transaction semantics, and failure recovery |
| **Reliability** | Structured errors, tracing, property-based thinking, reproducible tests, adversarial inputs, and observability |

## Selected repositories

These links are a **curated view of repositories available on this GitHub account**, not a claim of sole authorship or upstream maintainership. For a precise record of individual contributions, check commit history and pull requests.

| Repository | Technical area |
| :--- | :--- |
| [**Dbgeng-sys**](https://github.com/sharmis-tp/Dbgeng-sys) | Rust bindings and systems-level interoperability around Windows debugging interfaces |
| [**napi-rs**](https://github.com/sharmis-tp/napi-rs) | Rust ↔ Node.js native module interfaces and language boundaries |
| [**raydium-cp-swap**](https://github.com/sharmis-tp/raydium-cp-swap) | Solana AMM program architecture, account constraints, and token accounting |
| [**whirlpool-tx-replayer**](https://github.com/sharmis-tp/whirlpool-tx-replayer) | Replaying and inspecting concentrated-liquidity transaction behavior |
| [**agave**](https://github.com/sharmis-tp/agave) | Solana validator/runtime architecture and transaction execution |
| [**ic**](https://github.com/sharmis-tp/ic) | Internet Computer canister/runtime and distributed protocol architecture |
| [**subtensor**](https://github.com/sharmis-tp/subtensor) | Substrate-based protocol logic and on-chain state transitions |
| [**hyperbridge**](https://github.com/sharmis-tp/hyperbridge) | Cross-chain messaging and interoperability architecture |

## How I approach system design

### 01 / Make invalid states difficult to represent

Prefer domain types over loosely coupled primitive values. Model lifecycle transitions explicitly, separate validation from execution, and make trust boundaries visible in function signatures.

### 02 / Treat concurrency as a resource-management problem

Async code is not automatically scalable. I pay attention to task ownership, bounded work queues, cancellation, timeouts, contention, shutdown semantics, and whether synchronous work is accidentally blocking the executor.

### 03 / Establish a safety boundary before crossing it

`unsafe` is a tool for expressing guarantees the compiler cannot verify—not a performance switch. The objective is a small, documented, auditable unsafe boundary with safe abstractions around it. FFI deserves the same scrutiny for ownership, aliasing, layout, and unwind behavior.

### 04 / Optimize only after characterizing the workload

I distinguish throughput from tail latency, measure allocation and copying costs, and benchmark realistic inputs. Fewer allocations are not automatically a win if the result increases complexity, contention, or maintenance risk.

### 05 / Design protocols around adversarial inputs and partial failure

For on-chain and distributed systems, the hard parts are state transitions, authority, replay protection, idempotency, consistency, serialization compatibility, and recovery when a step is interrupted.

## Where Rust meets blockchain

My technical interests span:

- **Solana / Anchor:** PDAs, account validation, CPI boundaries, token programs, deterministic state transitions, compute budgets, and transaction replay considerations.
- **Internet Computer:** Rust canisters, Candid interfaces, ledger integration, upgrade-safe state, and asynchronous inter-canister calls.
- **Substrate ecosystems:** Runtime modules, storage models, dispatch logic, weights, and chain-level invariants.
- **Cross-chain infrastructure:** Message validation, settlement assumptions, finality, and explicit trust models.

I approach smart contracts as **state machines exposed to adversarial inputs**, not just functions that happen to run on a blockchain.

## Tooling & adjacent stack

`Rust` · `Cargo` · `Clippy` · `rustfmt` · `Tokio` · `Serde` · `tracing` · `Anchor` · `Solana` · `Candid` · `Linux` · `Git` · `Docker`

Additional experience: **TypeScript, Go, Python, C/C++, Move, Solidity**, and service/frontend integration. Rust remains the focus of this profile.

## Engineering principles

> Correctness before cleverness. Explicit invariants before abstraction. Measurement before optimization.

- Keep interfaces small and failure states observable.
- Prefer deterministic tests over assumptions about the happy path.
- Document non-obvious ownership, lifetime, and safety contracts.
- Make operations reproducible: pinned dependencies, automated checks, and reviewable changes.
- Separate what a codebase demonstrates from what a project merely explores.

---

<div align="center">

**Interested in Rust, protocol engineering, or difficult systems problems?**

[Explore repositories](https://github.com/sharmis-tp?tab=repositories) · [GitHub profile](https://github.com/sharmis-tp)

<sub>Build things that remain understandable under load, under failure, and under review.</sub>

</div>
