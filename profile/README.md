# Arcate

> Autonomous commercial diligence for product bets.

Arcate connects customer calls, support channels, and CRM contract records to rank B2B roadmap bets by deduplicated revenue at risk, separate pre-translated feature wishes from active renewal blockers, route high-ARR renewal threats to human review, and link every roadmap decision back to the exact customer quote.

Founded in Berlin by [Vito Bica](https://github.com/bicavito) and shaped across 25 years of B2B product leadership across European industrial manufacturing, B2B marketplaces, and enterprise SaaS.

- **Website:** [https://arcate.io](https://arcate.io)
- **Industrial Enterprise Benchmark:** [https://arcate.io/benchmark/](https://arcate.io/benchmark/) ([Markdown](https://arcate.io/benchmark/index.md))
- **Manifesto:** [https://arcate.io/manifesto/](https://arcate.io/manifesto/)
- **AEO & Machine-Readable Specs:** [llms.txt](https://arcate.io/llms.txt) | [ai-instructions](https://arcate.io/ai-instructions)

---

## Repository Architecture & Technical Due Diligence Access

Arcate builds commercial decision software for B2B product organizations and Private Equity portfolio teams. Core product repositories under `ArcateHQ` remain private to protect proprietary IP and enforce strict tenant isolation:

| Surface | Visibility | Scope | Status |
|---|---|---|---|
| **Arcate v2 Engine** | `Private` | Proprietary commercial decision engine for customer signal extraction, CRM contract matching, and revenue-weighted roadmap auditing, built across 8 months of R&D evaluating more than 400 studies across AI, econometrics, and decision science. | Active |
| **Arcate Web & Previews** | `Private` | Web application, UI design system, interactive UI previews (*Interactive Workspace Preview (Illustrative B2B SaaS Dataset)*), and public benchmark documentation (`arcate.io`). | Active |
| **`ArcateHQ/.github`** | `Public` | Organization overview, industrial verification benchmark summary, and GDPR/DPA governance documentation. | Public |

**Client Data Isolation:** Customer corpora and CRM exports never enter Git repositories. Every engagement runs in a dedicated single-tenant EU workspace.

**Technical Due Diligence (Private Equity, Venture Capital & Enterprise Security):** Qualified diligence and security teams can request technical architecture and release documentation under a mutual NDA via [vito@arcate.io](mailto:vito@arcate.io).

---

## Public Verification Benchmark (Anonymized Industrial Enterprise)

Full protocol, priority table, and anonymized source quotes: **[https://arcate.io/benchmark/](https://arcate.io/benchmark/)**

- **Subject (Three-Layer Anonymized):** Global Industrial Manufacturing Enterprise (>€3B annual revenue, European HQ), audited across `14` non-overlapping customer and regional channel accounts representing **`€11.81M` (`€11,805,000`)** in verified annual order volume (`314` bilingual transcript segments, `551,039` characters, `1,378` checked statements; in industrial e-commerce, affected order volume measures verified annual orders blocked from online self-service, whereas recurring B2B SaaS audits weight contract ARR exposed to renewal blockers).
- **1. Method Production Outcome (6-Month Engagement Prior to Automated Engine Build):** During a 6-month client engagement prior to building the automated engine, re-prioritizing the online product configurator around deduplicated order volume and exact customer quotes and shipping those changes reduced measured Customer Effort Score (`CES`, `1–5` scale where `1` = minimal customer effort and `5` = extreme effort) from **`3.53` to `1.47` within 6 months** (observational pre/post outcome on the redesigned configurator alongside engineering execution) and freed **`30%` of technical sales engineering capacity**.
- **2. Automated Engine Case-Study & Stability Benchmark (`Arcate v2 Engine`):** Evaluated retrospectively on unlabelled raw transcripts using fixed domain-agnostic codebook rules as a within-corpus case-study and pipeline stability benchmark across the full `1,378-statement` raw corpus against the pre-existing manual Senior Principal PM audit baseline coded line by line by the project lead during the 6-month client engagement prior to building the automated Arcate v2 Engine (external unseen-company generalization remains to be proven in multi-company pilots):
  - **`100% (11 / 11)` Reference Theme Recall:** Captured all `11` reference themes (`6` multi-account blockers, `3` single-account requests, `1` whale-dominated 2-account minor item, `1` wish cluster) from `133` active problem quotes, separated `15` speculative feature wishes (`0` counted as problem votes), and rejected `1,230` neutral context statements (with a mandatory `>=5%` human audit sample to monitor false negatives), compared to **`45.5% (5 / 11)`** recall in single-pass AI summaries (same frontier LLM class at `temperature = 0.0` across four cumulative runs at `45`, `135`, `225`, and `314` segments, degrading from `90.9%` at 45 segments to `45.5%` at 314 segments due to long-context attention decay; Liu et al., *Transactions of the ACL* 2024, `doi:10.1162/tacl_a_00638`).
  - **Why Standard Chunked RAG Workflows Also Fail:** Without deterministic CRM account-ARR deduplication, separation of feature wishes from problem quotes, and decoupling problem size (Step 1) from engineering effort (Step 2), uncalibrated chunked RAG/map-reduce summaries inflate counted volume (`11.89x` in the industrial test), drop rank correlation (`tau_b = 0.6889`), and promote `9` repeat mentions from `1` account and `15` unbacked wishes as top priorities.
  - **`91.7%` Roadmap Agreement:** Reproduced **`91.7%` (`J = 11 / 12 = 0.917`: all 11 customer-reported reference themes recovered alongside `6 / 6` core blockers and all `8` Keep/Add/Cut roadmap cards, while the 12th manual worksheet item was 1 internal editorial content-authoring workflow item outside transcripts)** of the project lead's pre-existing manual Senior Principal PM audit baseline (within-corpus check; Jaccard, *New Phytologist* 1912, `doi:10.1111/j.1469-8137.1912.tb05611.x`).
  - **`100% (148 / 148 Extracted)` Exact Quote Verification:** All `148` extracted quotes across `1,378` checked statements (`133` active problem quotes + `15` separated feature wishes; `1,230` neutral context statements checked via a `>=5%` audit sample) match the raw source transcript character-for-character (`0.0%` quote fabrication). Public quotes apply strict three-layer anonymization across company identity, account volume bands, and internal product, protocol, and equipment identifiers.

### 2027 Roadmap Audit Summary (`Keep`, `Add`, `Cut` Across `€11.81M` Portfolio Scope)

Priority ranks follow affected annual order volume (`#1 €7.70M`, `#2 €5.78M`, `#3 €5.46M`, `#4 €4.65M`, `#5 €4.05M`, `#6 €2.88M`) paired with three-point reference engineering ranges (optimistic / likely / conservative weeks; replaced or signed off by the client's engineering lead during a live portfolio audit):

| Roadmap Bucket | Initiatives | Portfolio Volume & Account Coverage | Reference Engineering Range |
|---|---|---|---|
| **Keep** (`#1, #3, #5`) | 3 planned initiatives confirmed | **`€10.61M` (`€10,605,000`)** across **`12 of 14` accounts** | **`19.5 wks`** (`12–30 wks`) |
| **Add** (`#2, #4, #6`) | 3 multi-account blind spots added | **`€8.66M` (`€8,655,000`)** across **`8 of 14` accounts** (`€0.95M` on `1` net-new account covering all **`13` blocker-affected accounts = `€11.56M`** of `14` audited / `€11.81M`, plus `€7.71M` across `7` overlapping accounts with a second ordering barrier; `1` `€0.25M` account had `0` active blockers) | **`14.0 wks`** (`9–23 wks`) |
| **Cut** (`2 proposals`) | `Chart-View State Persistence` (`6.0 wks`, `4–9 wks`; single-account repeat request) + `AI Auto-Suggestion Assistant` (`16.0 wks`, `11–25 wks`; `15` speculative wishes) | Pushed back (`0` multi-account problem coverage lost) | Saves **`22.0 wks`** (`15–34 wks`), yielding **`-8.0 wks` net engineering savings** (`41.5 -> 33.5 wks`) |

---

## Data Privacy, GDPR / DPA Governance & Co-Pilot Scope

Arcate is operated by **Bica Ventures UG (haftungsbeschränkt)** (Wörther Straße 6, 10435 Berlin, Germany; Amtsgericht Charlottenburg Berlin, HRB 203361 B; Managing Director: Vito Bica).

1. **Art. 28 GDPR DPA (AVV) & Mutual NDA:** Executed prior to any data transfer.
2. **EU Single-Tenant Isolation & Zero Model Training:** Dedicated single-tenant EU workspaces (Frankfurt / EU-Central) with zero AI model training on customer data and zero cross-customer data pooling.
3. **Pseudonymized Onboarding & 12-Month Co-Pilot Scope:** Supports pseudonymized CRM exports (`Account-ID + ARR + Tier` without customer names or personal identifiers) during the initial 10-business-day status-quo onboarding (first ranked draft by the end of week one) at the start of a **12-month Co-Pilot mandate** (including a **12-month single-company portfolio pilot** for Private Equity firms prior to broader portfolio expansion).
4. **Binding Raw Data Deletion Schedule:** Ingestion stops within 5 business days after completion of the 12-month mandate, and all raw customer data is permanently deleted within 30 calendar days.

[Imprint](https://arcate.io/pages/imprint) | [Privacy Policy](https://arcate.io/pages/privacy-policy) | [Terms of Service](https://arcate.io/pages/terms-of-service) | [Cookie Policy](https://arcate.io/pages/cookie-policy)
