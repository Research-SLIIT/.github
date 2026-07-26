<!--
═══════════════════════════════════════════════════════════════════════════════
  ORGANIZATION PROFILE README  ·  Research-SLIIT

  To publish as the org landing page (https://github.com/Research-SLIIT):
    1. Create a PUBLIC repo in the org named exactly:  .github
    2. Save this file as:                              profile/README.md
    3. Commit and push.

  IMAGES: every asset below is an absolute raw.githubusercontent.com URL
  pointing at screenshots/GIFs already committed to the FRONTEND repo on the
  `dev` branch. Nothing needs to be copied into the .github repo, and the
  Frontend repo must stay PUBLIC or every image 404s.

  ⚠ The BACKEND repo is currently PRIVATE, so its raw URLs 404 for anonymous
  visitors — and so do the two "Backend Repository" badge links below. Two
  backend screenshots (Docker stack, Swagger) are therefore commented out
  inline, marked "BACKEND IMAGE". Once the backend repo is made public,
  re-enable them and delete the frontend cell that replaced each one.

  If a branch is renamed, update these bases:
    .../Final-Year-Research_CSE-25-26J-445-Frontend/dev/docs/...
    .../Final-Year-Research_CSE-25-26J-445-Backend/dev-deploy/docs/...
═══════════════════════════════════════════════════════════════════════════════
-->

<div align="center">

<img src="https://raw.githubusercontent.com/Research-SLIIT/Final-Year-Research_CSE-25-26J-445-Frontend/dev/public/logo.png" alt="InvestWise" width="110">

# InvestWise

### Explainable Machine Intelligence for the Colombo Stock Exchange

**Final Year Research Project · CSE-25-26J-445**
*Sri Lanka Institute of Information Technology — Faculty of Computing · 2025/26*

<br>

<p>
<img alt="Services" src="https://img.shields.io/badge/Microservices-13-7c3aed?style=flat-square">
<img alt="Models" src="https://img.shields.io/badge/ML_Models-7_trained-0ea5e9?style=flat-square">
<img alt="Containers" src="https://img.shields.io/badge/Docker-14_containers-2496ED?style=flat-square&logo=docker&logoColor=white">
<img alt="Tests" src="https://img.shields.io/badge/Test_Files-62-f59e0b?style=flat-square">
<img alt="NestJS" src="https://img.shields.io/badge/NestJS-11-E0234E?style=flat-square&logo=nestjs&logoColor=white">
<img alt="Next.js" src="https://img.shields.io/badge/Next.js-16-000000?style=flat-square&logo=nextdotjs&logoColor=white">
<img alt="Python" src="https://img.shields.io/badge/Python-3.11-3776AB?style=flat-square&logo=python&logoColor=white">
<img alt="Kafka" src="https://img.shields.io/badge/Kafka-7.5-231F20?style=flat-square&logo=apachekafka&logoColor=white">
</p>

</div>

---

## 📦 Repositories

<table>
<tr>
<td width="50%" valign="top">

### [⚙️ Backend](https://github.com/Research-SLIIT/Final-Year-Research_CSE-25-26J-445-Backend) · `dev-deploy`

An **Nx monorepo of 13 applications**: REST API gateway, four gRPC microservices, Kafka email consumer, PayHere billing, an SSE orchestration service, **four Python ML inference services**, and the YAML-driven annual-report ETL. Two Docker Compose profiles — 9 containers for core dev, 14 for the full platform. CI/CD to EC2.

`NestJS 11` `TypeScript 5.9` `Nx 21.5` `Python 3.11` `FastAPI` `Flask` `gRPC` `Kafka 7.5` `MongoDB 7` `Redis` `PostgreSQL` `FAISS` `XGBoost` `LightGBM` `CatBoost` `SHAP` `spaCy` `Docker` `GitHub Actions`

</td>
<td width="50%" valign="top">

### [🖥️ Frontend](https://github.com/Research-SLIIT/Final-Year-Research_CSE-25-26J-445-Frontend) · `dev`

A **Next.js 16 App Router** analytics dashboard. Live market data via server-side CORS proxies, SSE-streamed AI pipelines, SHAP visualisations, KaTeX-documented feature engineering, printed model decision trees. 58 shadcn/ui primitives, 35 domain components, 5 Zustand stores, **40 Vitest test files**. Full light/dark parity, mobile-first.

`Next.js 16` `React 19` `TypeScript 5` `Tailwind CSS 4.1` `shadcn/ui` `Radix UI` `Zustand 5` `Recharts` `Framer Motion` `KaTeX` `React Hook Form` `Zod` `Vitest`

</td>
</tr>
</table>

<table>
<tr>
<td align="center" width="16.6%"><h3>13</h3><sub>Nx applications</sub></td>
<td align="center" width="16.6%"><h3>7</h3><sub>Trained models</sub></td>
<td align="center" width="16.6%"><h3>80</h3><sub>REST endpoints</sub></td>
<td align="center" width="16.6%"><h3>62</h3><sub>Test files</sub></td>
<td align="center" width="16.6%"><h3>14</h3><sub>Docker containers</sub></td>
<td align="center" width="16.6%"><h3>~240</h3><sub>Annual reports in ETL</sub></td>
</tr>
</table>

---

## The problem

The Colombo Stock Exchange has ~280 listed companies and almost no analytical tooling built for it. The data exists — filings, quarterly reports, financial news — but three properties break off-the-shelf models: Sri Lankan annual reports have **no consistent layout**, only a minority publish **machine-extractable reports** across a decade, and market-moving news mixes **English with Sinhala and Tamil** transliterations and local company nicknames.

**Our position:** a prediction an investor cannot interrogate is not usable. Every model here ships with its reasoning exposed — SHAP attributions, printed decision trees with real fusion weights, KaTeX feature derivations, retrieved historical precedents. **Explainability is the deliverable, not a feature.**

---

## 🎬 See It Working

<div align="center">

![Full walkthrough](https://raw.githubusercontent.com/Research-SLIIT/Final-Year-Research_CSE-25-26J-445-Frontend/dev/docs/videos/demo-full-walkthrough.gif)

*Sign-in → live market dashboard → all four ML components exercised end to end*

</div>

<table>
<tr>
<td width="25%" align="center">
<img src="https://raw.githubusercontent.com/Research-SLIIT/Final-Year-Research_CSE-25-26J-445-Frontend/dev/docs/videos/demo-risk-analysis.gif" alt="Risk analysis demo"><br>
<b>🩺 Risk Analysis</b><br><sub>6-stage AI pipeline over SSE → Z-Score verdict with SHAP drivers</sub>
</td>
<td width="25%" align="center">
<img src="https://raw.githubusercontent.com/Research-SLIIT/Final-Year-Research_CSE-25-26J-445-Frontend/dev/docs/videos/demo-price-prediction.gif" alt="Price prediction demo"><br>
<b>📈 Price Forecast</b><br><sub>T+5 open price from a 3-model ensemble</sub>
</td>
<td width="25%" align="center">
<img src="https://raw.githubusercontent.com/Research-SLIIT/Final-Year-Research_CSE-25-26J-445-Frontend/dev/docs/videos/demo-dividend.gif" alt="Dividend demo"><br>
<b>💰 Dividend Risk</b><br><sub>Cut probability with 14 features and their formulas</sub>
</td>
<td width="25%" align="center">
<img src="https://raw.githubusercontent.com/Research-SLIIT/Final-Year-Research_CSE-25-26J-445-Frontend/dev/docs/videos/demo-news-sentiment.gif" alt="Sentiment demo"><br>
<b>📰 News Impact</b><br><sub>Two-stage cascade printing its own decision tree</sub>
</td>
</tr>
</table>

<div align="center">

![Market dashboard](https://raw.githubusercontent.com/Research-SLIIT/Final-Year-Research_CSE-25-26J-445-Frontend/dev/docs/screenshots/01-dashboard.png)
**Live market dashboard** — ASPI · S&P SL20 · sector performance · gainers and losers · CSE news pulled live from `cse.lk`

</div>

<table>
<tr>
<td width="50%" align="center">
<img src="https://raw.githubusercontent.com/Research-SLIIT/Final-Year-Research_CSE-25-26J-445-Frontend/dev/docs/screenshots/02-risk-analysis-result.png" alt="Risk analysis"><br>
<sub><b>Projected next-quarter Altman Z-Score</b> — Safe / Grey / Distress</sub>
</td>
<td width="50%" align="center">
<img src="https://raw.githubusercontent.com/Research-SLIIT/Final-Year-Research_CSE-25-26J-445-Frontend/dev/docs/screenshots/04-shap-feature-impact.png" alt="SHAP attribution"><br>
<sub><b>SHAP attribution</b> — which ratios drove the score, and by how much</sub>
</td>
</tr>
<tr>
<td width="50%" align="center">
<img src="https://raw.githubusercontent.com/Research-SLIIT/Final-Year-Research_CSE-25-26J-445-Frontend/dev/docs/screenshots/05-price-prediction.png" alt="Price prediction"><br>
<sub><b>T+5 ensemble forecast</b> with per-day deltas and confidence</sub>
</td>
<td width="50%" align="center">
<img src="https://raw.githubusercontent.com/Research-SLIIT/Final-Year-Research_CSE-25-26J-445-Frontend/dev/docs/screenshots/07-dividend-prediction.png" alt="Dividend prediction"><br>
<sub><b>Dividend cut probability</b> against a tuned 0.822 threshold</sub>
</td>
</tr>
<tr>
<td width="50%" align="center">
<img src="https://raw.githubusercontent.com/Research-SLIIT/Final-Year-Research_CSE-25-26J-445-Frontend/dev/docs/screenshots/11-news-sentiment-analysis.png" alt="Sentiment decision tree"><br>
<sub><b>The model's actual decision tree</b> — stage scores, thresholds, fusion weights</sub>
</td>
<td width="50%" align="center">
<img src="https://raw.githubusercontent.com/Research-SLIIT/Final-Year-Research_CSE-25-26J-445-Frontend/dev/docs/screenshots/12-ai-terminal-stream.png" alt="SSE pipeline stream"><br>
<sub><b>The 6-stage pipeline narrating itself</b> over SSE, live in the browser</sub>
</td>
<!-- BACKEND IMAGE — re-enable once the Backend repo is public, then delete the cell above:
<td width="50%" align="center">
<img src="https://raw.githubusercontent.com/Research-SLIIT/Final-Year-Research_CSE-25-26J-445-Backend/dev-deploy/docs/screenshots/04-docker-stack-running.png" alt="Docker stack"><br>
<sub><b>14 containers</b> across two Docker Compose profiles</sub>
</td>
-->
</tr>
</table>

<details>
<summary><b>More screenshots</b> — SHAP ratios · dividend features · AI narrative · Swagger · light mode · mobile</summary>
<br>
<table>
<tr>
<td width="33%" align="center"><img src="https://raw.githubusercontent.com/Research-SLIIT/Final-Year-Research_CSE-25-26J-445-Frontend/dev/docs/screenshots/19-risk-financial-ratios.png" alt="Financial ratios"><br><sub>AI-extracted financial ratios</sub></td>
<td width="33%" align="center"><img src="https://raw.githubusercontent.com/Research-SLIIT/Final-Year-Research_CSE-25-26J-445-Frontend/dev/docs/screenshots/08-dividend-feature-contributions.png" alt="Feature contributions"><br><sub>Per-feature dividend contributions</sub></td>
<td width="33%" align="center"><img src="https://raw.githubusercontent.com/Research-SLIIT/Final-Year-Research_CSE-25-26J-445-Frontend/dev/docs/screenshots/18-dividend-ai-narrative.png" alt="AI narrative"><br><sub>LLM narrative over the prediction</sub></td>
</tr>
<tr>
<td align="center"><img src="https://raw.githubusercontent.com/Research-SLIIT/Final-Year-Research_CSE-25-26J-445-Frontend/dev/docs/screenshots/09-dividend-comparison.png" alt="Dividend comparison"><br><sub>Multi-company dividend comparison</sub></td>
<!-- BACKEND IMAGE — re-enable once the Backend repo is public, then delete the cell above:
<td align="center"><img src="https://raw.githubusercontent.com/Research-SLIIT/Final-Year-Research_CSE-25-26J-445-Backend/dev-deploy/docs/screenshots/01-swagger-overview.png" alt="Swagger"><br><sub>OpenAPI — 9 endpoint groups, one gateway</sub></td>
-->
<td align="center"><img src="https://raw.githubusercontent.com/Research-SLIIT/Final-Year-Research_CSE-25-26J-445-Frontend/dev/docs/screenshots/16-light-mode.png" alt="Light mode"><br><sub>Full light/dark parity</sub></td>
<td align="center"><img src="https://raw.githubusercontent.com/Research-SLIIT/Final-Year-Research_CSE-25-26J-445-Frontend/dev/docs/screenshots/17-mobile-responsive.png" alt="Mobile"><br><sub>Mobile-first responsive</sub></td>
</tr>
</table>
</details>

---

## 🔬 Four Research Components

Four members, four independently trained and evaluated models, one shared platform.

| | Component | Method | Key result |
|:-:|---|---|---|
| 🩺 | **Financial Distress** | SVR projecting next-quarter **Altman Z-Score** from 9 ratios, explained with a SHAP `KernelExplainer`. Ratios extracted by sending raw PDFs to Gemini's File API rather than parsing them. | Safe / Grey / Distress with per-feature signed attribution |
| 📈 | **Open Price Forecast** | Equal-weight ensemble of **LightGBM + XGBoost + CatBoost** over 28 engineered technical features, 60-day lookback, log-returns clamped at ±0.15 | T+5 open-price path with SHAP feature importance |
| 💰 | **Dividend Cut** | Elastic-net **Logistic Regression** on 14 features engineered from 8 balance-sheet fields; temporal split at 2021, minority class weighted 3× | **82.1 %** accuracy · AUC **0.697** · threshold **0.822** · n=140 |
| 📰 | **News Market-Impact** | **Two-stage XGBoost** cascade over 3072-d embeddings, fused with a financial lexicon, grounded by **FAISS** retrieval; a spaCy + RapidFuzz company gate runs before any paid inference | Impact flag + direction + 4-step decision tree + historical precedents |

<details>
<summary><b>📐 Model specifications</b></summary>

| | Risk | Open Price | Dividend | Sentiment |
|---|---|---|---|---|
| **Algorithm** | SVR | LightGBM + XGBoost + CatBoost | Logistic Regression | XGBoost ×2 + lexicon |
| **Preprocessing** | StandardScaler | 28-feature engineering | 14-feature engineering | `text-embedding-3-large` (3072-d) |
| **Target** | Next-quarter Z-Score | T+5 open price | P(dividend cut) | Impact + direction |
| **Key hyperparameters** | — | equal-weight ensemble | `C=0.05`, `l1_ratio=0.2`, `saga`, `class_weight {0:1, 1:3}`, `max_iter=20000` | Stage 1 threshold `0.30`; fusion `0.6/0.4` when `lex_conf ≥ 0.60`, else `0.7/0.3` |
| **Validation** | — | held-out test set | temporal split, train cutoff 2021 | held-out + lexicon cross-check |
| **Explainability** | SHAP KernelExplainer, k-means background (k=10) | SHAP feature importance | KaTeX feature derivations + LLM narrative | printed decision tree + FAISS precedents |
| **Serving** | Flask · `:5001` | FastAPI · `:5002` | FastAPI · `:8001` | FastAPI · `:8002` |

**Why these choices:** CSE liquidity is thin and volatility regime-dependent, so three price models disagree and average. Only ~19 companies publish extractable reports across 2012–2025, so the dividend model has 140 samples — at the default 0.5 threshold it cried wolf, hence 0.822. The lexicon is precise but brittle and the embedding model general but opaque, so the lexicon leads only when confident (≥ 0.60).

</details>

---

## 🏗 How It Fits Together

Four research tracks share one ingestion layer, one auth boundary, and one API contract — the separation that let them be developed in parallel.

```mermaid
graph TB
    subgraph FE["Frontend · Next.js 16 + React 19"]
        direction LR
        UI1["Market<br/>Dashboard"]
        UI2["Risk<br/>Analysis"]
        UI3["Price<br/>Prediction"]
        UI4["Dividend<br/>Prediction"]
        UI5["News<br/>Sentiment"]
    end

    GW["<b>API Gateway</b> · NestJS · :3400<br/>JWT · RBAC · Subscription tiers · OpenAPI 3"]

    subgraph MESH["gRPC Service Mesh · NestJS"]
        direction LR
        M1["Auth<br/>OTP · OAuth"]
        M2["User<br/>Profiles"]
        M3["Community<br/>Social"]
        M4["Logs<br/>Audit"]
    end

    subgraph ML["ML Inference · Python"]
        direction LR
        R1["<b>Risk</b><br/>SVR + SHAP"]
        R2["<b>Open Price</b><br/>3-model ensemble"]
        R3["<b>Dividend</b><br/>Elastic-net"]
        R4["<b>Sentiment</b><br/>2-stage + FAISS"]
    end

    subgraph ORCH["Orchestration"]
        direction LR
        O1["Financial Health<br/>6-stage SSE pipeline"]
        O2["Payment<br/>PayHere"]
    end

    subgraph ASYNC["Async"]
        K["Kafka"]
        E["Email<br/>consumer"]
    end

    subgraph DATA["Data"]
        direction LR
        D1[("MongoDB")]
        D2[("Redis")]
        D3[("FAISS<br/>244 MB")]
        D4[("PostgreSQL")]
    end

    subgraph ETL["Ingestion"]
        direction LR
        I1["Dividend ETL<br/>~240 annual reports<br/>YAML-pinned extraction"]
        I2["News Scraper<br/>ft.lk RSS<br/>SHA-256 dedup"]
        I3["cse.lk API<br/>live market data"]
    end

    FE -->|"REST + SSE"| GW
    GW --> MESH
    GW --> ML
    GW --> ORCH
    MESH -.-> K --> E
    O2 -.-> K
    O1 --> R1
    MESH --> D1
    ML --> D1
    R3 --> D2
    R4 --> D3
    R2 --> D4
    I1 --> D1
    I2 --> D3
    I3 --> FE
    I3 --> O1

    classDef fe fill:#7c3aed,stroke:#4c1d95,color:#fff
    classDef gw fill:#a855f7,stroke:#6b21a8,stroke-width:3px,color:#fff
    classDef mesh fill:#10b981,stroke:#065f46,color:#fff
    classDef ml fill:#0ea5e9,stroke:#075985,color:#fff
    classDef orch fill:#14b8a6,stroke:#115e59,color:#fff
    classDef async fill:#f59e0b,stroke:#92400e,color:#fff
    classDef data fill:#475569,stroke:#0f172a,color:#fff
    classDef etl fill:#ec4899,stroke:#9d174d,color:#fff

    class UI1,UI2,UI3,UI4,UI5 fe
    class GW gw
    class M1,M2,M3,M4 mesh
    class R1,R2,R3,R4 ml
    class O1,O2 orch
    class K,E async
    class D1,D2,D3,D4 data
    class I1,I2,I3 etl
```

**Four transports, deliberately.** gRPC for the internal NestJS mesh (protobuf contracts make refactors safe) · HTTP/JSON at the Python boundary (an ML service shouldn't need a gRPC toolchain to be testable with `curl`) · Kafka for email (sign-up must never fail because SMTP is down) · SSE for long-running analysis (a 40-second wait becomes visible progress, with no WebSocket infrastructure).

---

## 🚀 Run It Yourself

```bash
# Backend — full stack including all ML services
git clone https://github.com/Research-SLIIT/Final-Year-Research_CSE-25-26J-445-Backend.git
cd Final-Year-Research_CSE-25-26J-445-Backend && git checkout dev-deploy
cp .env.example .env                       # fill in your values
docker compose --profile ml up -d          # 14 containers

# Frontend
git clone https://github.com/Research-SLIIT/Final-Year-Research_CSE-25-26J-445-Frontend.git
cd Final-Year-Research_CSE-25-26J-445-Frontend && git checkout dev
pnpm install && pnpm dev                   # → http://localhost:3000
```

Web app <http://localhost:3000> · Swagger UI <http://localhost:3400/api/v1>

> [!TIP]
> Allocate **≈ 11–12 GB of RAM to Docker** before the first `--profile ml` run — the ML profile loads XGBoost boosters, a 3-model ensemble and a 244 MB FAISS index simultaneously; below that the Python containers are OOM-killed at startup and report unhealthy with no obvious error.
>
> The stack starts **without any LLM API keys**. The dividend and sentiment services fall back to clearly labelled demo modes (every substituted stage marked `demo_mode`, so a demo result can never be mistaken for a real one) and every non-LLM path works fully.

Full setup, environment reference and troubleshooting live in each repository's README.

---

## 👥 The Team

**CSE-25-26J-445** · SLIIT Faculty of Computing · 2025/26

| Research Component | Backend | Frontend |
|---|---|---|
| 🩺 **Financial Risk & Explainability** | `Risk-prediction-ml` · `financial-health-service` | `/risk` · Z-Score gauge · SHAP breakdown |
| 📈 **Open Price Forecasting** | `open-price-prediction-ml` | `/predict` · forecast + delta charts |
| 💰 **Dividend Cut Prediction** | `Dividend-prediction-ml` · `Dividend-ETL` | `/dividend` · feature cards · KaTeX |
| 📰 **News Sentiment & Market Impact** | `sentiment-backend` | `/news` · AI terminal · decision tree |
| 🏗 **Platform & Infrastructure** | `api-gateway` · `auth` · `user` · `community` · `email` · `payment` · `logs` | `AppShell` · auth store · `/admin` · `/pricing` |

*Supervised by the SLIIT Faculty of Computing.*

---

<div align="center">

Released under the **MIT License**. Built for academic research — nothing here constitutes financial advice; the models are research artifacts trained on limited data, and their limitations are documented in each repository.

<br>

[![Backend](https://img.shields.io/badge/⚙️_Backend_Repository-181717?style=for-the-badge&logo=github)](https://github.com/Research-SLIIT/Final-Year-Research_CSE-25-26J-445-Backend)
[![Frontend](https://img.shields.io/badge/🖥️_Frontend_Repository-181717?style=for-the-badge&logo=github)](https://github.com/Research-SLIIT/Final-Year-Research_CSE-25-26J-445-Frontend)

<sub><b>Sri Lanka Institute of Information Technology</b> · Faculty of Computing · Final Year Research Project 2025/26<br>
Colombo Stock Exchange · Explainable Machine Learning · Event-Driven Microservices</sub>

</div>
