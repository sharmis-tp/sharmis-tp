<div align="center">

### Senior Rust Engineer · AI/ML Infrastructure

**The systems layer under machine learning: training libraries, checkpoints, agent orchestration, LLM observability and developer tooling.**

<p>
  <img src="https://img.shields.io/badge/Rust-000000?style=flat-square&logo=rust&logoColor=white" alt="Rust" />
  <img src="https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white" alt="Go" />
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/OpenTelemetry-425CC7?style=flat-square&logo=opentelemetry&logoColor=white" alt="OpenTelemetry" />
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
| **Agent orchestration & safety** | Lock lifecycle in task orchestrators, eval-dimension scoring, per-agent event types, scope enforcement |
| **LLM observability** | OpenTelemetry spans for agent and tool events, error capture in LangChain tracing, token-usage parsing, AI memory and knowledge planes |
| **Grafana & monitoring** | ECharts plugin hardening, template variable regex, Pyroscope datasource fixes |
| **Forecasting & anomaly detection** | Exogenous-feature support in time-series foundation-model pipelines |
| **Systems foundations** | Tokio, cancellation safety, backpressure, zero-copy I/O, FFI and `unsafe` audits |

## Open-source contributions

All links go to my own pull requests. 55+ merged across 30+ repositories.

### AI/ML & agent infrastructure

| Project | Contribution | Status |
| :--- | :--- | :---: |
| [**ClickHouse/loom**](https://github.com/ClickHouse/loom): AI agent memory & observability on ClickHouse | [Rewrite doc page opening sentences for search and LLM discovery](https://github.com/ClickHouse/loom/pull/726) | merged |
| [**FastNN**](https://github.com/CanReader/FastNN): neural-network library in Rust + CUDA | [Reject zero-length sequences in LSTM/GRU](https://github.com/CanReader/FastNN/pull/78) · [Assert fan_in > 0 in Kaiming/Xavier init](https://github.com/CanReader/FastNN/pull/77) | merged |
| | [Atomic checkpoint writes](https://github.com/CanReader/FastNN/pull/74) · [Verify MNIST download integrity](https://github.com/CanReader/FastNN/pull/72) | merged |
| [**jamjet**](https://github.com/jamjet-labs/jamjet): safety layer for AI agents | [Fix DimensionScores.composite() weight normalization](https://github.com/jamjet-labs/jamjet/pull/176) · [Add OTel span attributes](https://github.com/jamjet-labs/jamjet/pull/197) | merged |
| [**forge-orchestrator**](https://github.com/nxtg-ai/forge-orchestrator): agent task orchestration | [Release orphaned locks for completed tasks](https://github.com/nxtg-ai/forge-orchestrator/pull/100) · [Fix companion plugin on re-run](https://github.com/nxtg-ai/forge-orchestrator/pull/106) | merged |
| [**PrismorSec/prismor**](https://github.com/PrismorSec/prismor): security agent platform | [Detect --mount bind in host policy](https://github.com/PrismorSec/prismor/pull/902) · [Declare per-agent event_types](https://github.com/PrismorSec/prismor/pull/797) · [Synthesized scope asks instead of blocking](https://github.com/PrismorSec/prismor/pull/784) | merged |
| [**durare**](https://github.com/SamuelXing/durare): provider framework | [Add StepOutcome::from_columns](https://github.com/SamuelXing/durare/pull/263) · [Export types named by StateProvider methods](https://github.com/SamuelXing/durare/pull/255) | merged |
| [**Sentient**](https://github.com/existence-master/Sentient): AI agent desktop | [Keep names like Claude Code in generated setting labels](https://github.com/existence-master/Sentient/pull/530) | merged |
| [**automic-vault**](https://github.com/automic-vault/automic-vault): agent scripting | [Add agent skills for Blessed Scripts](https://github.com/automic-vault/automic-vault/pull/411) | merged |

### Observability & Grafana

| Project | Contribution | Status |
| :--- | :--- | :---: |
| [**grafana/dataViz**](https://github.com/grafana/dataViz): Grafana ECharts plugin monorepo | [Guard non-string config.src in getLayerSrc](https://github.com/grafana/dataViz/pull/201) · [Replace untracked plan file references](https://github.com/grafana/dataViz/pull/200) | in review |
| [**grafana-pyroscope-datasource**](https://github.com/grafana/grafana-pyroscope-datasource) | [Fix multi-value template variable regex](https://github.com/grafana/grafana-pyroscope-datasource/pull/113) | in review |
| [**getsentry/sentry-go**](https://github.com/getsentry/sentry-go): Sentry SDK for Go | [Add WithMechanism capture option](https://github.com/getsentry/sentry-go/pull/1472) | in review |
| [**lemma**](https://github.com/uselemma/lemma): LLM tracing | [Record handled LangChain tool errors as span errors](https://github.com/uselemma/lemma/pull/137) | in review |
| [**oxtrace**](https://github.com/aashrith/oxtrace): LLM usage tracing | [Parse usage from gzip-encoded responses](https://github.com/aashrith/oxtrace/pull/23) | in review |
| [**foundationforecast**](https://github.com/TimeCopilot/foundationforecast): time-series foundation models | [Forward futr_exog_list in detect_anomalies](https://github.com/TimeCopilot/foundationforecast/pull/82) | in review |

### Systems, networking & blockchain

| Project | Contribution | Status |
| :--- | :--- | :---: |
| [**libp2p/py-libp2p**](https://github.com/libp2p/py-libp2p): P2P networking in Python | [Use /sni/ name as TLS server name when dialing](https://github.com/libp2p/py-libp2p/pull/1564) | merged |
| [**libp2p/js-libp2p**](https://github.com/libp2p/js-libp2p): P2P networking in JS | [Wrap ErrorEvent in ConnectionFailedError on failed dial](https://github.com/libp2p/js-libp2p/pull/3701) · [Validate config options at startup](https://github.com/libp2p/js-libp2p/pull/3659) | in review |
| [**polkadot-api/papi-console**](https://github.com/polkadot-api/papi-console): Polkadot console | [Re-run runtime calls from workspace](https://github.com/polkadot-api/papi-console/pull/189) · [Keep fork lanes stable](https://github.com/polkadot-api/papi-console/pull/188) | merged |
| [**UOR-Foundation/uor-addr**](https://github.com/UOR-Foundation/uor-addr): content addressing in Rust | [Reject JSON objects with duplicate member names](https://github.com/UOR-Foundation/uor-addr/pull/17) · [Sort object members by UTF-16 code units](https://github.com/UOR-Foundation/uor-addr/pull/19) | merged |
| [**UOR-Foundation/kappa-registry**](https://github.com/UOR-Foundation/kappa-registry): OCI registry in Rust | [Carry page size in tags/list Link header](https://github.com/UOR-Foundation/kappa-registry/pull/23) · [Add dual MIT/Apache license](https://github.com/UOR-Foundation/kappa-registry/pull/20) | in review |
| [**project-llzk/circom**](https://github.com/project-llzk/circom): ZK circuit compiler | [Add location and expression to assertion messages](https://github.com/project-llzk/circom/pull/471) | merged |
| [**perun-network/perun-ckb-backend**](https://github.com/perun-network/perun-ckb-backend): payment channels | [Make subscription polling interval configurable](https://github.com/perun-network/perun-ckb-backend/pull/33) | merged |
| [**ScopeLift/umbra-protocol**](https://github.com/ScopeLift/umbra-protocol): privacy protocol | [Remove unimplemented relayWithdrawOnBehalf() stub](https://github.com/ScopeLift/umbra-protocol/pull/747) | merged |
| [**MorpheusAIs/Morpheus-Lumerin-Node**](https://github.com/MorpheusAIs/Morpheus-Lumerin-Node): decentralized AI | [Re-check sessions on chain before refusing](https://github.com/MorpheusAIs/Morpheus-Lumerin-Node/pull/1033) | in review |
| [**stellar-scaffold/cli**](https://github.com/stellar-scaffold/cli): Stellar dev CLI | [Build clients without a Cargo workspace](https://github.com/stellar-scaffold/cli/pull/652) | in review |

### Developer tools & language servers

| Project | Contribution | Status |
| :--- | :--- | :---: |
| [**eza-community/eza**](https://github.com/eza-community/eza): modern ls replacement | [Add EZA_SIZE_STYLE env var](https://github.com/eza-community/eza/pull/1981) | in review |
| [**beancount-language-server**](https://github.com/polarmutex/beancount-language-server): LSP for Beancount | [Advertise positionEncoding capability (LSP 3.17)](https://github.com/polarmutex/beancount-language-server/pull/971) · [Fix exit code on unclean shutdown](https://github.com/polarmutex/beancount-language-server/pull/970) | merged |
| [**tree-sitter-beancount**](https://github.com/polarmutex/tree-sitter-beancount): grammar | [Add injections.scm for BQL query highlighting](https://github.com/polarmutex/tree-sitter-beancount/pull/164) | in review |
| [**metal2vk**](https://github.com/joshuaswarren/metal2vk): Metal-to-Vulkan translation | [Key pipeline variants by library/name/constants](https://github.com/joshuaswarren/metal2vk/pull/107) · [Reject inconsistent push/descriptor metadata](https://github.com/joshuaswarren/metal2vk/pull/106) | merged |
| [**smolvm**](https://github.com/smol-machines/smolvm): lightweight VM manager | [Let a disk volume set its directory's owner and mode](https://github.com/smol-machines/smolvm/pull/2010) | in review |
| [**mimas**](https://github.com/imlazyeye/mimas): GML parser in Rust | [Accept loop, while, for, if and match as binary operands](https://github.com/imlazyeye/mimas/pull/103) | merged |

Own repositories: [smalloc](https://github.com/sharmis-tp/smalloc) (memory allocator for Solana programs), [Dbgeng-sys](https://github.com/sharmis-tp/Dbgeng-sys) (Rust FFI bindings for the Windows debugger engine), [Solana-Credit-Score](https://github.com/sharmis-tp/Solana-Credit-Score), [AsyncCSVX](https://github.com/sharmis-tp/AsyncCSVX).

## How I work

**01. Measure, then optimize.** Throughput, tail latency and allocations, not guesses.

**02. Make failure boring.** Writes are atomic, inputs are validated at the boundary, and errors say what to do next.

**03. Trust numbers only when they're tested.** An eval score or a loss curve is only as good as the code that computes it.

**04. Small, reviewable changes.** Every PR above is scoped to one problem and easy to review.

---

<div align="center">

**Open to remote roles and contracts with AI/ML startups: ML infrastructure, inference, evaluation and Rust performance work.**

</div>
