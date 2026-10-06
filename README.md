<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,50:1f6feb,100:58A6FF&height=200&section=header&text=Shreyas%20Agarwal&fontSize=48&fontColor=ffffff&animation=fadeIn&fontAlignY=36&desc=data%20person%20%C2%B7%20systems%20builder%20%C2%B7%20product%20brain&descSize=16&descAlignY=56" width="100%" />
</p>

<p align="center">
  <a href="https://git.io/typing-svg"><img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=500&size=20&pause=1200&color=58A6FF&center=true&vCenter=true&width=640&lines=Data+%E2%86%92+Systems+%E2%86%92+Products+%E2%86%92+Platforms;I+lead+the+build+and+argue+the+roadmap;From+ecosystems+to+distributed+systems;Writing+the+ADR+before+the+code;Probably+overengineering+something+right+now" /></a>
</p>

<p align="center">
  <a href="https://linkedin.com/in/shreyasagarwal01"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" /></a>
  <!-- <img src="https://img.shields.io/badge/Open_to-Senior_%2F_Lead_roles-2ea44f?style=for-the-badge" /> -->
</p>

> I came to software from **computational ecology**, modeling how plant–pollinator networks hold together and how they break under perturbation.
> I still read systems the same way: follow the information, find where it fractures, redesign the flow before the friction becomes normal.

---

## ⚡ In numbers

<table>
  <tr>
    <td align="center" width="33%"><h2>30s → 3s</h2>dashboard load times after I rebuilt the analytics engine to run in the browser</td>
    <td align="center" width="33%"><h2>1.5 days</h2>to ship a multi-provider auth migration, schema refactor included, ahead of a client demo</td>
    <td align="center" width="33%"><h2>400+</h2>commits across 12 repos in the last quarter</td>
  </tr>
  <tr>
    <td align="center"><h2>6 → 1</h2>products running on one shared platform I design end to end</td>
    <td align="center"><h2>1 week</h2>to build, publish and roll a shared UI library out across 3 products</td>
    <td align="center"><h2>1.5%</h2>silent data loss I caught in a financial pipeline, spanning two fiscal years</td>
  </tr>
</table>

---

## 🧭 What I actually do

```mermaid
flowchart LR
  A[🤝 Client conversations] --> B[🧭 Product & roadmap]
  B --> C[🎨 UX & UI design]
  C --> D[🏗️ System design]
  D --> E[⚙️ Build]
  E --> F[☁️ Infra & delivery]
  F --> G[📚 Docs & process]
  G -. feedback .-> A
```

The whole loop, at a small B2B SaaS company:

- 🏗️ **Lead engineer.** System design across the product suite, engineering standards, and guiding the rest of the team.
- 🧭 **Associate PM.** Run client demos, shape features and the roadmap, and own the design language and UI.
- ☁️ **AWS, end to end.** Org and identity, networking, compute, storage, CI/CD.
- 🔄 **Data engineering.** Client data integrations, layered pipelines, and the analytics engines on top.
- 📚 **Docs, process & consulting.** ADRs, design docs, process definition, and business consulting.

---

## 🔒 Built under NDA (described loosely)

<details>
<summary><b>Expand</b></summary>
<br>

- **In-browser analytics engine.** DuckDB-WASM in Web Workers with a two-tier memory + OPFS cache, hierarchy filtering with predicate pushdown. This is where the 30s → 3s comes from.
- **Pipeline DSL.** Declarative specs compiled to SQL and run locally via sqlglot, SQLMesh and DuckDB.
- **Versioned data workflows.** Imports with tree diffs and preview/confirm, draft → publish layers, optimistic concurrency, append-only changelogs, live presence over SSE.
- **LLM agent features.** Provider-agnostic agent loop, tool registry, model gateway with a usage ledger, and a fixture-based eval harness.
- **Multi-product platform.** gRPC service contracts, multi-provider auth, regional deployment topology, tenant isolation at the infrastructure level.
- **Enterprise data integration.** Tolerant parsers for messy source systems, bronze → silver → gold pipelines, run-level observability, desktop agents.
- **Production hardening.** Job reconciliation without an outbox, circuit breakers, thundering-herd and N+1 fixes, metrics.

</details>

---

## 🌱 In the open

<table>
  <tr>
    <td>
      <b><a href="https://github.com/Shreyas-Agarwal/transit-intelligence">🚇 transit-intelligence</a></b><br>
      Real-time public transit observability on GTFS / GTFS-RT.<br><br>
      📡 Realtime feed ingestion → Redpanda<br>
      🔁 Crash-recoverable downloader with bounded queues and OpenTelemetry benchmarks<br>
      🥉→🥈 Parquet medallion pipeline, Python + SQLMesh analytics<br>
      🛡️ Full governance stack: Conventional Commits + DCO, gitleaks, Vale, Renovate
    </td>
  </tr>
</table>

🧪 **Labs:** [go-event-lab](https://github.com/Shreyas-Agarwal/go-event-lab) (concurrency & event-processing benchmarks) · [lakehouse-engineering-lab](https://github.com/Shreyas-Agarwal/lakehouse-engineering-lab) (one system, Pandas → Spark)

---

## 🛠️ Stack

<p>
  <img src="https://skillicons.dev/icons?i=ts,py,react,nodejs,express,fastapi,postgres,redis,kafka,aws,docker,githubactions,linux" />
</p>
<p>
  <img src="https://img.shields.io/badge/DuckDB-FFF000?style=flat-square&logo=duckdb&logoColor=black" />
  <img src="https://img.shields.io/badge/SQLMesh-1f6feb?style=flat-square" />
  <img src="https://img.shields.io/badge/gRPC-244c5a?style=flat-square" />
  <img src="https://img.shields.io/badge/Flyway-CC0200?style=flat-square&logo=flyway&logoColor=white" />
  <img src="https://img.shields.io/badge/Turborepo-EF4444?style=flat-square&logo=turborepo&logoColor=white" />
  <img src="https://img.shields.io/badge/WebAssembly-654FF0?style=flat-square&logo=webassembly&logoColor=white" />
</p>

---

## 💬 Things I say too often

<table>
  <tr>
    <td align="center" width="50%">
      <br>🧩<br><br>
      <b><i>"Most scaling problems are<br>coordination problems in disguise."</i></b>
      <br><br>
    </td>
    <td align="center" width="50%">
      <br>🩹<br><br>
      <b><i>"Temporary workarounds are<br>architecture nobody reviewed."</i></b>
      <br><br>
    </td>
  </tr>
  <tr>
    <td align="center">
      <br>📝<br><br>
      <b><i>"Write the ADR<br>before you write the code."</i></b>
      <br><br>
    </td>
    <td align="center">
      <br>🌋<br><br>
      <b><i>"Systems fracture long<br>before infrastructure breaks."</i></b>
      <br><br>
    </td>
  </tr>
</table>

<p align="center">
  <sub>────────── ✦ ──────────</sub>
</p>

<h3 align="center"><i>"Good systems reduce cognitive load.<br>Great systems disappear into the workflow."</i></h3>

---

## 📈 The receipts

<p align="center">
  <img src="https://streak-stats.demolab.com?user=Shreyas-Agarwal&theme=tokyonight&hide_border=true&background=0D1117&ring=58A6FF&fire=58A6FF&currStreakLabel=58A6FF" width="80%" />
</p>

<p align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=Shreyas-Agarwal&theme=tokyo-night&hide_border=true&bg_color=0D1117&color=58A6FF&line=1f6feb&point=ffffff&area=true" width="100%" />
</p>

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=Shreyas-Agarwal&show_icons=true&count_private=true&include_all_commits=true&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=58A6FF&icon_color=58A6FF" width="49%" />
</p>

<p align="center">
  <img src="https://img.shields.io/github/followers/Shreyas-Agarwal?style=for-the-badge&logo=github&label=Followers&color=1f6feb" />
  <img src="https://komarev.com/ghpvc/?username=Shreyas-Agarwal&style=for-the-badge&color=58A6FF&label=Profile+views" />
</p>

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:58A6FF,50:1f6feb,100:0d1117&height=110&section=footer" width="100%" />
</p>
