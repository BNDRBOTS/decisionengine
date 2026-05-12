# PHX 2026 · Forensic Revenue Engine + THA SHYT

A zero‑hallucination revenue modeling tool for Phoenix‑based coaching businesses.  
Built by [BNDR LLC](https://bndrllc.com).

## Overview

The Revenue Engine projects monthly net profit, LTV, CAC, and funnel metrics using real‑world market data (CPCs, search volumes, adoption rates).  
Coaches and consultants can adjust pricing, acquisition budget, channel mix, infrastructure, and client lifespan to instantly see bottom‑line impact.  

The integrated **THA SHYT Decision Engine** scores consulting offers on 8 dimensions (Value, Money, Now, Simplicity, Scale, Ease, Fun, Automation), weighted by confidence, producing a normalized Market‑Fit Multiplier.

## Features

- **Live P&L breakdown** – gross revenue, acquisition, opex, capex, true net.  
- **Funnel topology** – traffic → leads → MQLs → meetings → clients, with conversion ratios.  
- **Zero‑sum channel sliders** – auto‑balance SEO, ads, social spend while updating traffic forecasts.  
- **AI Intake simulation** – toggles between human‑preferred (85%) and automated intake impact on conversion.  
- **Market snapshot** – Phoenix income baseline, job growth, CPC assumptions.  
- **THA SHYT Decision Engine** – scored, ranked consulting ideas with confidence‑weighted scoring.  
- **System diagnostics** – automatic gates for market‑fit, LTV:CAC ratio, throughput limits, capital burn.  
- **DeepSeek AI Insight** – optional one‑click strategic pivot (key stored in session).  
- **Onboarding walkthrough** and mandatory disclaimer before first use.  
- **Accessible** – programmatic labels, ARIA radiogroups, aria‑expanded, inert panels.  
- **Responsive** – works on mobile, tablet, and desktop.

## Tech Stack

- Plain HTML, CSS (Tailwind via CDN), vanilla JavaScript  
- No frameworks, no build step  
- Optional DeepSeek API integration for AI‑powered strategic insights  

## Quick Start

1. Clone or download the repository.  
2. Open `index.html` in any modern browser.  
3. Agree to the disclaimer, then click through the onboarding guide.  
4. Adjust sliders and segmented controls – results update immediately.

## Configuration

All market data resides in the `CONFIG` object inside the `<script>` tag.  
You can update CPCs, search volumes, infrastructure costs, etc., without touching logic.  
```js
const CONFIG = {
  cpc: { seo: 2.96, social: 1.50, ads: 6.40 },
  coaching: { humanPref: 85, soloCeiling: 5 },
  // ...
};

## Onboarding & Disclaimer

First‑time visitors must accept a legal disclaimer.  
An optional step‑by‑step tour explains each control panel; users can skip at any time.

## Legal Disclaimer

This tool is for informational and educational purposes only.  
It does **not** constitute financial, legal, or business advice.  
BNDR LLC assumes no liability for decisions made based on its output.  
By using the tool, you accept all associated risks.

## Author

**BNDR LLC** – [bndrllc.com](https://bndrllc.com)  
© 2026 All rights reserved.
