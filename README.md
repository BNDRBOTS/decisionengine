# PHX 2026 Forensic Revenue Engine + THA SHYT Decision Engine

A production‑grade, zero‑hallucination dashboard for coaching revenue forensics and consulting offer wedge scoring. Built for GitHub Pages with no backend, fully client‑side.

---

## What this tool does

- **Forensic Revenue Engine** – Simulates a coaching business in Phoenix using attested 2025‑2026 data. You adjust budget, pricing, channels, niche, infrastructure, and it calculates traffic, leads, clients, revenue, costs, and system health checks.
- **THA SHYT Decision Engine** – Scores consulting offer ideas based on eight weighted variables and confidence ratings. It prints a ranked report of your best consulting wedges.

Both tools share the same design language but operate completely independently.

---

## How to use the Revenue Engine

### Left column controls
1. **Pricing Model**
   - `Service Niche` – Pick the coaching audience (Burnout, Executive, Generalist, Health). Changes the market‑fit multiplier.
   - `Package Tier` – Select the pricing level. Floor ($150), Mid ($1,500), Ceiling ($15,000).
   - `Client Lifespan` – Slide to set how many sessions/courses a client buys. The Client LTV updates live.

2. **Capital & Channels**
   - `Monthly Acq Budget` – Slide to set your total monthly ad/SEO spend.
   - `Conversion Scenario` – Conservative (1.87 %), Expected (2.35 %), or Aggressive (5.31 %). Changes the base conversion rate and cost‑per‑click modifier.
   - `Channel Distribution` – Three sliders (SEO, Paid Search, Social) that always add up to 100 %. Sliding one auto‑adjusts the others proportionally.
   - Below each slider you see the actual budget allocation and estimated clicks.

3. **Infrastructure & AI**
   - `Digital Infra` – Freelance, Agency, or Ecommerce. Determines monthly hosting/development costs (opex + amortised capex).
   - `AI Intake Backend` – Toggle on if you use an AI booking bot. It applies a penalty because 85 % of clients still prefer human coaches.

4. **Resolved Contradictions**
   - Static data showing the attested income baseline, job growth band, and active data disputes.

5. **AI Insight (DeepSeek)**
   - Click to enter a session‑only API key. Then click `AI Insight` to ask DeepSeek for a strategic pivot based on the live engine numbers. Key is never stored permanently.

### Right column results
- **True Net P&L** – Big hero number showing monthly profit after budget, infrastructure, and amortised capex. Turns red if negative.
- **KPI cards** – Client LTV, blended CAC, LTV:CAC ratio, and clients per month.
- **Funnel Topology** – Visual bar chart of Traffic → Leads → MQLs → Meetings → Clients. Hover numbers update instantly.
- **Forensic data cards** – Local market data (search volumes, CPC, competitor counts, agency lists, micro‑targeting zones). All numbers come from the `CONFIG` object and can be updated easily.
- **System Diagnostics** – Shows pass/warn/fail gates for market‑fit, LTV:CAC, throughput ceiling, and profitability.

---

## How to use the THA SHYT Decision Engine

Click the `Decision Engine` button in the top header. The panel slides open.

### Scoring a single idea
1. **Fill in the four required fields:**
   - *Buyer* – Who pays (e.g., “Corporate HR director”).
   - *Role/Team* – Who uses the deliverable (e.g., “Internal L&D team”).
   - *Task* – The recurring work (e.g., “weekly coaching intake review”).
   - *Outcome* – How you measure success (e.g., “30% fewer no‑shows”).

2. **Optional evidence** – Paste any notes or data that backs up your scores.

3. **Set the eight variable scores (1–10)** and **eight confidence ratings (0–3, where 0 = unknown)**.
   - V = Value, M = Money, N = Now, L = Simplicity, S = Scale, E = Ease, F = Fun, A = Automation.
   - Confidence ratings judge how sure you are about each score.

4. Click **Score Idea**. The system checks if the four fields are complete and if the domain is valid. If anything is missing, it prints `NEEDS INPUT`. If the domain is out of scope, it prints `INVALID`. If valid, it calculates:
   - Raw score, normalised score, and final confidence‑adjusted score.

5. The result appears in a formatted block showing the score breakdown.

### Building a ranked list
- Click **Add to List** after scoring to append the idea.
- The list ranks valid ideas by `THA_SHYT_final` (highest first). Ties are broken by Scale, then Now, then Value.
- Click **Clear All** to reset the list and clear all input fields.

---

## How to update the data

All perishable numbers live in a single `CONFIG` object at the top of the script. To refresh the data:

1. Open the HTML file.
2. Find the `CONFIG` block (near line 1100).
3. Change any value (e.g., `cpc.seo`, `coaching.totalUSCoaches`, etc.).
4. Update `lastUpdated` to the current date.
5. The freshness badge will automatically show if data is fresh, stale (>90 days), or expired (>180 days).

---

## File structure
/ (repo root)
index.html – Main application
robots.txt – Blocks all crawlers (no‑scrape)
README.md – This file


## Security & privacy
- No data is sent to any server except the DeepSeek API, and only when you explicitly enter a key.
- All calculations run inside your browser.
- `robots.txt` prevents search engines from indexing the page.

---

## Support
For custom consulting offers or integration, contact bndrllc.com.

*BNDR LLC ALL RIGHTS RESERVED*
