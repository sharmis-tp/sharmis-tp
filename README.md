<div align="center">

### Senior Rust Engineer · AI/ML Infrastructure

**The systems layer under machine learning: training libraries, checkpoints, agent evaluation and LLM observability.**

<p>
  <img src="https://img.shields.io/badge/Rust-000000?style=flat-square&logo=rust&logoColor=white" alt="Rust" />
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/OpenTelemetry-425CC7?style=flat-square&logo=opentelemetry&logoColor=white" alt="OpenTelemetry" />
  <img src="https://img.shields.io/badge/Tokio-000000?style=flat-square&logo=rust&logoColor=white" alt="Tokio" />
</p>

<a href="https://github.com/sharmis-tp?tab=followers"><img src="https://img.shields.io/github/followers/sharmis-tp?style=flat-square&label=followers&color=CE422B" alt="followers" /></a>
<a href="mailto:sharmis.tp@gmail.com"><img src="https://img.shields.io/badge/email-sharmis.tp%40gmail.com-24292F?style=flat-square&logo=gmail&logoColor=white" alt="email" /></a>
<img src="https://img.shields.io/badge/open_to-remote_work_(US_timezones)-2ea44f?style=flat-square" alt="open to remote work" />

</div>

---

## `whoami`

I've been building software since 2018, most of it in **Rust**: async services, FFI, memory allocators and protocol code that has to stay correct under load.

Today I work where that background matters most in AI: **the infrastructure that models and agents run on.** That means numerical correctness in training code, checkpoints that survive a crash, evaluation scores you can trust, and traces that tell you why an agent did what it did.

> Models are only as reliable as the systems that train, evaluate and serve them.

## What I work on

| Area | What I focus on |
| :--- | :--- |
| **Training library internals** | Optimizer math (RMSprop variance, epsilon placement), weight initialization (Kaiming/Xavier), RNN input validation, numerically stable edge cases |
| **Checkpointing & data integrity** | Atomic checkpoint writes, batched tensor serialization, verified dataset downloads |
| **Agent evaluation** | Scoring and weighting of eval dimensions |
| **LLM observability** | OpenTelemetry spans for agent and tool events, error capture in LangChain tracing, token-usage parsing |
| **Forecasting & anomaly detection** | Exogenous-feature support in time-series foundation-model pipelines |
| **Systems foundations** | Tokio, cancellation safety, backpressure, zero-copy I/O, FFI and `unsafe` audits |

## Open-source work in AI/ML

All links go to my own pull requests.

**Merged**

| Project | Contribution |
| :--- | :--- |
| [**FastNN**](https://github.com/CanReader/FastNN): neural-network library in Rust + CUDA | [Reject zero-length sequences in LSTM/GRU with a clear message](https://github.com/CanReader/FastNN/pull/78) |
| | [Verify MNIST download integrity before using a cached file](https://github.com/CanReader/FastNN/pull/72) |
| [**jamjet**](https://github.com/jamjet-labs/jamjet): safety layer for AI agents | [Fix `DimensionScores.composite()` weight normalization](https://github.com/jamjet-labs/jamjet/pull/176) |
| | [Add OpenTelemetry span attributes for coordinator and agent-tool events](https://github.com/jamjet-labs/jamjet/pull/197) |

**In review**

| Project | Contribution |
| :--- | :--- |
| [**FastNN**](https://github.com/CanReader/FastNN) | [Fix centered RMSprop: clamp variance, move eps outside sqrt](https://github.com/CanReader/FastNN/pull/73) |
| | [Atomic checkpoint writes](https://github.com/CanReader/FastNN/pull/74) · [Batch tensor I/O in checkpoint serialization](https://github.com/CanReader/FastNN/pull/76) |
| | [Assert `fan_in > 0` in Kaiming/Xavier init](https://github.com/CanReader/FastNN/pull/77) |
| [**foundationforecast**](https://github.com/TimeCopilot/foundationforecast): time-series foundation models | [Accept `X_df` and `futr_exog_list` in `detect_anomalies`](https://github.com/TimeCopilot/foundationforecast/pull/82) |
| [**lemma**](https://github.com/uselemma/lemma): LLM tracing | [Record handled LangChain tool errors as span errors](https://github.com/uselemma/lemma/pull/137) |
| [**oxtrace**](https://github.com/aashrith/oxtrace): LLM usage tracing | [Parse usage from gzip-encoded responses](https://github.com/aashrith/oxtrace/pull/23) |
| [**runanywhere-sdks**](https://github.com/RunanywhereAI/runanywhere-sdks): on-device AI SDKs | [Typecheck core test files](https://github.com/RunanywhereAI/runanywhere-sdks/pull/1159) |

## Systems & distributed work

Merged contributions to [**py-libp2p**](https://github.com/libp2p/py-libp2p/pulls?q=author%3Asharmis-tp), [**papi-console**](https://github.com/polkadot-api/papi-console/pulls?q=author%3Asharmis-tp) (Polkadot), [**circom**](https://github.com/project-llzk/circom/pulls?q=author%3Asharmis-tp), [**beancount-language-server**](https://github.com/polarmutex/beancount-language-server/pulls?q=author%3Asharmis-tp), [**perun-ckb-backend**](https://github.com/perun-network/perun-ckb-backend/pulls?q=author%3Asharmis-tp), [**uor-addr**](https://github.com/UOR-Foundation/uor-addr/pulls?q=author%3Asharmis-tp) and [**metal2vk**](https://github.com/joshuaswarren/metal2vk/pulls?q=author%3Asharmis-tp).

Own repositories: [smalloc](https://github.com/sharmis-tp/smalloc) (memory allocator for Solana programs), [Dbgeng-sys](https://github.com/sharmis-tp/Dbgeng-sys) (Rust FFI bindings for the Windows debugger engine), [Solana-Credit-Score](https://github.com/sharmis-tp/Solana-Credit-Score), [AsyncCSVX](https://github.com/sharmis-tp/AsyncCSVX).

## How I work

**01. Measure, then optimize.** Throughput, tail latency and allocations, not guesses.

**02. Make failure boring.** Writes are atomic, inputs are validated at the boundary, and errors say what to do next.

**03. Trust numbers only when they're tested.** An eval score or a loss curve is only as good as the code that computes it.

**04. Small, reviewable changes.** Every PR above is scoped to one problem and easy to review.

---

<div align="center">

**Open to remote roles and contracts with AI/ML startups: ML infrastructure, inference, evaluation and Rust performance work.**

[sharmis.tp@gmail.com](mailto:sharmis.tp@gmail.com)

</div>
