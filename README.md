# seo-leader-projects

Workspace for three connected projects on AI search behavior in Vietnamese commercial markets, building toward a unified portfolio thesis: **the apparatus that explains AI search mechanically — built for the Vietnamese market, by an AI lead at SEONGON.**

This directory is a workspace, not a single repository. Each subdirectory below is its own git repository and its own GitHub project, deliberately. They share data infrastructure and a common thesis, but ship independently with their own audiences, milestones, and value propositions.

## The three projects

### [vn-aio-atlas](./vn-aio-atlas) — the empirical study **(in progress, draft v0.2)**

The first scaled empirical study of AI Overview behavior in Vietnamese commercial search. Backed by 244,000 query-result observations and 1.4M citation events from December 2025 through April 2026 across 264 client projects.

**Live now:**
- 📊 Interactive dashboard: [vn-aio-atlas-dashboard-production.up.railway.app](https://vn-aio-atlas-dashboard-production.up.railway.app) (per-vertical filtering, EN/VI translation toggle)
- 📄 Full report: [REPORT.md (English)](./vn-aio-atlas/report/REPORT.md) / [REPORT_vi.md (Tiếng Việt)](./vn-aio-atlas/report/REPORT_vi.md)
- 📈 10 findings: [FINDINGS.md](./vn-aio-atlas/FINDINGS.md)
- 💾 Code + data infrastructure: [github.com/hdviettt/vn-aio-atlas](https://github.com/hdviettt/vn-aio-atlas)

**What it is:** authority. The study makes SEONGON the canonical reference on VN AI search before any tooling exists.

### [vn-aio-predictor](./vn-aio-predictor) — the predictive tool

A free web tool that predicts whether a given URL would be cited in Google's AI Overview for a given query. Trained as a tabular classifier on 154,000 positive citation examples from the Atlas's underlying dataset.

**What it is:** the product layer. Free tier captures leads; the underlying predictions inform SEONGON's enterprise GEO retainer.

### [vn-aio-simulator](./vn-aio-simulator) — the generative artifact

A small Vietnamese-capable LLM fine-tuned on 154K real Google AI Overview generations. Given a query, it produces what AIO would likely write — for SEO operators to evaluate content drafts against simulated output before publishing.

**What it is:** the breakout demo. The viral artifact. The thing that gets you on conference stages because nobody else can build it.

## Sequencing

The projects build on each other and ship in order:

```
vn-aio-atlas   ──→ vn-aio-predictor ──→ vn-aio-simulator
  (~10 weeks)        (~8 weeks)           (~9 weeks)
   authority         monetization          virality
```

Total runway: approximately 6 months end-to-end. Each project credentials the next.

## Data

All three projects draw from SEONGON's internal SERP-scraping pipeline (DataForSEO-backed, running across 264 active client projects). The dataset:

- 244,323 keyword-level result records (Supabase master, Railway mirror)
- 80,264 distinct Vietnamese commercial queries
- 154,428 captured AI Overview generations
- ~1.4M AIO citation events
- ~720M characters of AIO-generated text
- 5 months of longitudinal coverage (Dec 2025 – Apr 2026)

Brand coverage spans Vinamilk, Techcombank, VIB, VPBank, HDBank, ACB, MB, Prudential, Vinmec, Medlatec, Tâm Anh, Hồng Ngọc, GHTK, Viettel Post, Decathlon, FPT Shop, and dozens more across banking, healthcare, retail, e-commerce, FMCG, education, logistics, and construction.

All public outputs use anonymized aggregations only. Raw client data is never published.

## Status

| Project | Status |
|---|---|
| [vn-aio-atlas](./vn-aio-atlas) | **Draft v0.4** — publication-grade dashboard with sidebar nav, display typography, key-stat callouts; 12 findings (F9 now includes has_price showing -49% effect — a new headline); full report (EN+VI) published; deploy guard + cite-this-study + print stylesheet shipped. Awaiting SEONGON legal clearance. |
| [vn-aio-predictor](./vn-aio-predictor) | Planning. Begins after Atlas reaches v1.0. |
| [vn-aio-simulator](./vn-aio-simulator) | Planning. Begins after Predictor reaches v1.0. |

## About

Workspace led by Hoang Duc Viet (AI lead at [SEONGON](https://seongon.com), a Vietnamese SEO agency). The dataset is SEONGON's; the methodology, tooling, and publications are mine. Each project's commercial dimension (lead-gen tool, retainer product, conference demo) connects back to SEONGON's go-to-market.

Personal site: [hoangducviet.work](https://hoangducviet.work).
