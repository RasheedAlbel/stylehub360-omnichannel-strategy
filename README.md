# StyleHub360: The Full Circle Transformation
### Data-Driven Omnichannel Strategy — Business Analytics Case Study

> Bridging the gap between physical retail dominance (NPS +50) and digital lag (NPS +10)
> through churn modeling, customer segmentation, and financial feasibility analysis.

**Author:** Rasheed A. Albel
**Date:** December 2025

---

## Overview

StyleHub360 is a European fashion retailer with **€14.4M EBITDA** and 50 physical
stores, but a struggling digital channel suffering from:

- **60% cart abandonment rate**
- **8.5% stockout rate** (~€3M in lost annual online sales)
- **12-hour inventory sync delays** between POS and ERP systems
- Generic customer segmentation (only 3 tiers) missing behavioral nuance

This project applies data science techniques to diagnose root causes and recommend
a two-pillar transformation strategy with measurable ROI targets.

---

## Business Problem

| Metric            | Physical Stores | Digital Channel |
|-------------------|-----------------|-----------------|
| NPS Score         | +50             | +10             |
| Avg. Delivery     | In-store        | 3.8 days        |
| Stockout Rate     | Low             | 8.5%            |
| Competitor Bench  | —               | TrendFlow: 48h  |

---

## Analytical Methods

### 1. Churn Prediction Model
A logistic regression model identifies the key drivers of customer churn:

| Feature              | Coefficient | Interpretation                          |
|----------------------|-------------|------------------------------------------|
| `slow_delivery_flag` | **+0.11**   | Avg. wait > 4 days → highest churn risk  |
| `nps_score`          | +0.09       | Low NPS correlates with churn            |
| `avg_delivery_days`  | -0.03       | Marginal effect beyond the flag          |
| `loyalty_tier_encoded`| **-0.28** | Higher tier = strongest churn protection |

> **Key insight:** Speed is the biggest risk; loyalty tier is the biggest defense.

### 2. RFM-Based Customer Segmentation (3D K-Means)
Customers are segmented on **Recency, Frequency, and Monetary** scores,
revealing 5 behavioral personas that generic Gold/Silver/Bronze tiers miss:

| Segment            | Strategy                                              |
|--------------------|-------------------------------------------------------|
| **True VIPs**      | Exclusive early access, concierge support             |
| **Steady Shoppers**| Auto-suggest "Complete the Look" bundles at checkout  |
| **Fresh Prospects**| Time-bound second-purchase incentives                 |
| **Hibernating**    | Personalized price-drop alerts on viewed items        |
| **Drifting**       | "We Miss You" re-engagement with inventory clearance  |

### 3. Market Basket Analysis
Exploring association rules ("People who bought Jeans also bought Belts") to
automate cross-sell recommendations and lift AOV from €58 → €66.

---

## Strategy Recommendations

### Pillar 1 — Project Velocity (Operational Fix)
- Deploy a **lightweight API middleware layer** to sync StoreFlow (POS) and
  FinCore (ERP) in real time, replacing the 12-hour batch process
- Implement a **"Green Routing" algorithm** to auto-route orders to the
  nearest store, targeting delivery time < 2 days
- **Expected impact:** Stockout rate reduced from 8.5% → <3%; 15% shipping cost reduction

### Pillar 2 — Smart Style (Personalization)
- Deploy a **SaaS recommendation engine** (e.g., RECOM+) integrated with a
  lightweight Customer Data Platform (CDP)
- Activate behavioral segments with tailored, automated campaigns
- **Expected impact:** AOV uplift from €58 → €66; reduced churn in at-risk segments

---

## Financial Feasibility

| Metric           | Value       |
|------------------|-------------|
| CAPEX Investment | ~€1.2M      |
| Available Liquidity | €8M      |
| Liquidity Buffer | €6.8M       |
| Payback Period   | 18 months   |
| 3-Year ROI       | ~35%        |
| Net Benefit (Y3) | **€15.6M**  |
| Revenue Target   | €24M by 2028|

---

## Implementation Roadmap

| Phase     | Timeline | Key Activities                                     |
|-----------|----------|----------------------------------------------------|
| Foundation| Q1–Q2    | API layer implementation, data cleaning            |
| Pilot     | Q3       | Ship-from-store in 10 flagships, recommendation engine live |
| Scale     | Q4       | Full 50-store rollout, Smart Style launch          |

---

## Risk Mitigation

| Risk                     | Mitigation                                              |
|--------------------------|---------------------------------------------------------|
| Store staff resistance   | Gamification, shared fulfillment incentives             |
| Tech implementation delay| Low-code tools for dashboards; IT focused on API only   |
| Competitive price war    | NPS-focused differentiation; personalization "lock-in"  |

---

## Tech Stack

`Python` · `Pandas` · `NumPy` · `scikit-learn` · `Matplotlib` · `Seaborn`
