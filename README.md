<h1 align="center">Shreyas Agarwal</h1>

<p align="center">
  Lead engineer and technical product manager<br>
  System design · data platforms · AI integration
</p>

<p align="center">
  <a href="https://linkedin.com/in/shreyasagarwal01"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
</p>

I design and lead the engineering of a product suite for construction and infrastructure data at a small B2B SaaS company. My work sits between the product question (what should this do, and for whom) and the system question (what has to be true for it to keep working at scale). I write the highest-value parts myself and set the standard for the rest.

I came to software from computational ecology, modelling how plant–pollinator networks hold together and how they fail under perturbation. I still approach systems the same way: follow the information, find where it breaks, and fix the flow before the friction becomes normal.

---

## What I bring

**System design.** Service boundaries, contracts and data flow for a multi-product, multi-tenant suite. I write the design doc or ADR before the build, and convert it into the record once the work ships. I design for the second and third product on the same foundation, not just the first.

**Data architecture.** Layered bronze, silver and gold pipelines, versioned workflows with preview and confirm, draft and publish layers, append-only changelogs and optimistic concurrency. Schema changes on live systems backfill and preserve data, and a destructive reset is an explicit decision.

**Product and technical leadership.** I run client demos, shape the roadmap and set the design language, then turn that into specifications other engineers can build against. I have written first versions of products myself and handed them on, and I step back into the code where it is highest value.

**Reliability.** Job reconciliation without an outbox, circuit breakers, fixes for thundering-herd and N+1 problems, run-level observability, and backup and point-in-time-recovery validation.

**Review and delivery standards.** Work is tracked in issues and reviewed in pull requests. Unplanned fixes get an issue first, and regressions from a refactor are filed and marked in the code. Lint, commit conventions, dependency versions and CI are set once and shared.

---

## Shared foundations

The less visible half of the work is the platform the products stand on.

| | |
| --- | --- |
| **Client-side data engine** | A mapping layer between visualisation libraries and DuckDB-WASM in the browser, covering interaction state, query scheduling, SQL generation, tiered caching and hierarchy filtering with predicate pushdown |
| **Shared UI library** | A component library used across the products, kept separate from the auth and state layer so each can change independently |
| **Packages and SDKs** | Shared packages and SDKs for platform services, with contracts that can be versioned |
| **Dependency management** | One place that decides dependency versions across the suite: a pnpm catalog delivered as a config-dependency plugin, so every repo takes the same exact versions through one reviewed pull request |
| **API gateway** | Reverse proxy and webhook broadcaster, rewritten from Node to Go on the standard library only, with observability and separate test and production instances |
| **Identity and control plane** | Authentication, licensing, connector uploads and pipeline execution, with short-lived scoped credentials for pipeline runs |
| **Infrastructure** | AWS accounts, identity, networking and storage as code with OpenTofu, and tenant isolation at the infrastructure level |

## AI integration

- **MCP connectors.** A production connector lets Claude author, validate and preview data pipelines and dashboards against a user's own data. The work is in tool design and scoping, in how identity and access carry through to the agent, and in keeping the human accept step inside the app.
- **Agent features.** Provider-agnostic agent loops, tool registries, a model gateway with usage accounting, and fixture-based evaluation.
- **Building with AI.** I write the design doc and the invariants first, the model implements against them, and review checks the result against the spec. That is how components in languages outside my daily stack, such as the C# desktop and Revit pieces, are built. I am not a .NET specialist. What I own there is the contract: what a run is, what a retry may repeat, and what must never be lost.

## Domains

Most of the work is private, so it is described by problem area.

- **Quantity and cost.** BIM-based quantity takeoff, bills of quantities and running-account bills.
- **Progress tracking.** Progress on a model, or on a location breakdown where there is no model, connected to billing.
- **Analytics.** Pipelines from raw source data to curated datasets, with dashboards on top.
- **Notifications.** Telling the right people what changed in their design tools, in the chat they already use.
- **Automation.** No-code jobs and prebuilt setups for moving, tagging and connecting construction data.

---

## Open source: Transit Intelligence

[**transit-intelligence**](https://github.com/Shreyas-Agarwal/transit-intelligence) is where I am putting my own time. It is an event-driven platform for modelling, analysing and simulating public transit networks, and the project I am reinvesting most in.

**The idea.** Most transit software is built for passengers. Very little is built for the network itself. A delayed tram does not stay isolated: platforms crowd, following vehicles slip, transfers break, and the disruption spreads. Transit Intelligence treats a network the way modern infrastructure treats a distributed system, as something observable and replayable, with an event timeline, historical replay and a propagation graph.

**The design.**
- Operational state is derived from immutable events, not held as mutable application state, so any past state can be rebuilt by replaying the log.
- A modular monolith with domain-first layout. Modules own their boundaries and talk only through events or typed gRPC and protobuf contracts.
- A temporal graph engine, with edge weights driven by delay, congestion and traversal variance.
- Ingestion of GTFS and GTFS-RT feeds into Redpanda, a crash-recoverable downloader with bounded queues, and OpenTelemetry benchmarks.
- A Parquet medallion pipeline with Python and SQLMesh analytics.
- ADRs for the major decisions, and a governance stack of Conventional Commits, DCO, gitleaks, Vale and Renovate.

**Where it stands.** Pre-1.0. Ingestion runs against static GTFS data, while live GTFS-RT integration and the end-to-end path are still ahead. The repository is public so the architecture and decisions can be read and discussed.

Smaller projects: [go-event-lab](https://github.com/Shreyas-Agarwal/go-event-lab) (concurrency and event-processing benchmarks in Go) and [lakehouse-engineering-lab](https://github.com/Shreyas-Agarwal/lakehouse-engineering-lab) (one system implemented from Pandas through to Spark).

---

## Selected outcomes

| | |
| --- | --- |
| **30 s → 3 s** | Dashboard load time, after moving the analytics engine into the browser |
| **1.5 days** | A multi-provider auth migration, schema refactor included, shipped ahead of a client demo |
| **1 week** | A shared UI library built, published and adopted across three products |
| **1.5%** | Silent data loss caught in a financial pipeline, spanning two fiscal years |

## Technical areas

<p>
  <img src="https://skillicons.dev/icons?i=ts,py,go,react,nodejs,fastapi,postgres,redis,aws,docker,githubactions,linux&theme=dark" alt="TypeScript, Python, Go, React, Node.js, FastAPI, PostgreSQL, Redis, AWS, Docker, GitHub Actions, Linux" />
</p>
<p>
  <img src="https://img.shields.io/badge/DuckDB-FFF000?style=flat-square&logo=duckdb&logoColor=black" alt="DuckDB" />
  <img src="https://img.shields.io/badge/SQLMesh-1f6feb?style=flat-square" alt="SQLMesh" />
  <img src="https://img.shields.io/badge/gRPC-244c5a?style=flat-square" alt="gRPC" />
  <img src="https://img.shields.io/badge/Flyway-CC0200?style=flat-square&logo=flyway&logoColor=white" alt="Flyway" />
  <img src="https://img.shields.io/badge/OpenTofu-FFDA18?style=flat-square&logo=opentofu&logoColor=black" alt="OpenTofu" />
  <img src="https://img.shields.io/badge/Turborepo-EF4444?style=flat-square&logo=turborepo&logoColor=white" alt="Turborepo" />
  <img src="https://img.shields.io/badge/WebAssembly-654FF0?style=flat-square&logo=webassembly&logoColor=white" alt="WebAssembly" />
</p>

| | |
| --- | --- |
| **Data** | DuckDB and DuckDB-WASM, SQLMesh, Parquet, bronze/silver/gold layering, PostgreSQL, Flyway |
| **Backend** | TypeScript, Node, Python, FastAPI, Go, gRPC |
| **Frontend** | React, Web Workers, OPFS caching |
| **Platform** | AWS, Fargate, OpenTofu, GitHub Actions, Turborepo, pnpm workspaces |
| **AI** | MCP servers, agent loops, tool registries, model gateways, evaluation harnesses |
| **Specified and reviewed, not hand-written** | C# desktop and Revit components |
