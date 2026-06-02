# Qinghe Site Selector — AI-Powered Retail Location Intelligence

> **Chinese version of [Smart Site Selector](https://github.com/jonhnsonzz/smart-site-selector).** An AI-powered retail location evaluation tool leveraging the Huff Gravity Model, 2SFCA accessibility analysis, and XGBoost revenue prediction.

**每年30%的门店因选址错误亏损倒闭，平均损失15-40万。** Qinghe Site Selector quantifies site selection risk with AI, turning gut-feel decisions into data-backed choices.

**[Try the Demo](https://jonhnsonzz.github.io/qinghe选址宝/)** | Fully Open Source

---

## The Problem

| Traditional Approach | Qinghe Site Selector |
|:---|:---|
| "This street looks busy enough" | Huff Gravity Model quantifies consumer attraction |
| "A few competitors nearby, not sure if saturated" | 2SFCA supply-demand ratio measures area saturation |
| "3 hours of spreadsheet calculations for P&L" | 30-second automated P&L report |
| "Manual competitor counting" | Auto-fetch surrounding competitors via Amap POI |
| "Gut-feel decisions, learn the hard way" | AI composite score + explainable recommendations |

---

## Features

### 📊 Smart Site Scoring
Composite 100-point score based on Huff Gravity Model + supply-demand accessibility analysis + ML prediction. Tells you directly: **go or no-go**.

### 💰 Automated P&L Estimation
Enter area/rent/unit price — get a full P&L report in 30 seconds:
- Monthly fixed cost breakdown
- Break-even point (revenue / foot traffic)
- Three-scenario analysis (pessimistic / neutral / optimistic)
- Predicted payback period

### 🗺️ Competitor Analysis
Auto-fetch same-category competitors within 1km radius:
- Competitor count + average rating
- Distance distribution visualization
- Competition intensity radar

### 🎯 AI Site Recommendations
Natural-language assessment with quantified rationale for each recommendation — not just the conclusion, but **why**.

---

## Quick Start

### Option 1: Online Demo (Recommended)
👉 **[https://jonhnsonzz.github.io/qinghe选址宝/](https://jonhnsonzz.github.io/qinghe选址宝/)**

> Demo version uses simulated data. Configure an Amap API key to switch to real data sources.

### Option 2: Local Deployment

```bash
git clone https://github.com/jonhnsonzz/qinghe-site-selector.git
cd qinghe-site-selector

# Open in browser (Chrome recommended)
open index.html
# or
python -m http.server 8080
# Visit http://localhost:8080
```

### Option 3: Configure Amap Data (Optional)

```javascript
// Replace YOUR_AMAP_KEY in index.html
// 1. Apply for a Web Service API Key at Amap Open Platform (free: 1000 calls/day)
// 2. Replace YOUR_AMAP_KEY below

<script src="https://webapi.amap.com/maps?v=2.0&key=YOUR_AMAP_KEY"></script>
```

---

## Methodology

This project combines globally validated site selection models:

- **Huff Gravity Model (1963)** — Quantifies consumer store selection probability; core to ESRI/McDonald's systems
- **MCI Multi-Factor Competition Model** — Generalized Huff variant; distinguishes strong/weak competitive relationships
- **2SFCA (Two-Step Floating Catchment Area)** — Regional saturation assessment
- **XGBoost Revenue Prediction** — 40+ dimension composite prediction (Phase 2)

See the [full research report on site selection methodology](https://feishu.cn/docx/BfkndZ0Rmo9C1uxBx87cfjmGnhd) (Chinese).

---

## Tech Stack

| Layer | Technology | Notes |
|:---|:---|:---|
| Frontend | Vanilla HTML/CSS/JS | Zero dependencies, single-file runnable |
| Maps | Amap JS API | POI search + route planning |
| Models | Huff / MCI / 2SFCA | Classic spatial analysis models |
| Prediction | XGBoost | Revenue prediction (rule engine for MVP) |
| Deployment | GitHub Pages | Free hosting, one-click deploy |

---

## Data Sources

| Source | Purpose | Status |
|:---|:---|:---:|
| Amap POI | Competitor location/rating | Requires API key |
| National Bureau of Statistics population data | Regional population density | Built-in |
| Simulated data | Feature demonstration | ✅ Available |

> **Amap API Free Tier**: 1,000 POI queries/day for individual developers — sufficient for small-scale use and demos.

---

## Product Roadmap

| Phase | Feature | Status |
|:---|:---|:---:|
| MVP | Single category + P&L + competitor scoring | ✅ Complete |
| v1.1 | Real Amap POI + multi-category support | 🔨 In development |
| v1.2 | XGBoost revenue prediction model | 📋 Planned |
| v2.0 | Enterprise + API + multi-store comparison | 📋 Planned |

---

## Comparison

| Product | Target User | Price | China-Ready | AI Prediction |
|:---|:---|:---|:---|:---|
| **Qinghe Site Selector** | Small independent businesses | Free/Low-cost | ✅ Dedicated | ✅ Built-in |
| ESRI BAO | Large enterprises | $100K+/year | ⚠️ Expensive | ✅ |
| Placer.ai | Mid-chain stores | $30-100K/year | ❌ No | ✅ |
| Yingshang/Krypton | Commercial real estate | Negotiable | ✅ | ⚠️ |

---

## License

MIT License — Stars ⭐ and contributions welcome!

---

**Qinghe Site Selector** | Turning every site selection decision into a data-backed choice.
