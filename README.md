# E-Commerce Funnel Analysis | Excel · Power BI · Data Cleaning · Business Intelligence

> Identified **$680K+ in at-risk revenue** across 5,000 orders by mapping
> the full order lifecycle and pinpointing where — and why — customers
> were dropping off before delivery.

---

## Business problem

An e-commerce business was seeing steady order volume but shrinking
margins. Leadership needed to understand whether the problem was in
acquisition, fulfillment, product mix, or customer behavior — and where
to focus first to stop the revenue leak.

---

## Methodology

1. **Data audit** — Ran 18 quality checks across both datasets (orders,
   products) before touching anything. Documented every finding.
2. **Data cleaning** — Resolved a silent null import issue in the `size`
   column caused by pandas misreading `"N/A"` as missing. Zero rows
   dropped, zero values fabricated.
3. **Funnel analysis** — Mapped every order status (Processing → Shipped
   → Delivered vs. Returned / Cancelled) and calculated count, percentage
   share, and revenue impact per stage.
4. **Segmentation** — Broke revenue down by product category, payment
   method, and month to isolate concentration risk and seasonality.
5. **Visualization** — Built an Excel workbook (pivot tables, 6 embedded
   charts) and a Power BI interactive dashboard (slicers, cross-filtering,
   KPI cards) for business stakeholder presentation.

---

## Skills demonstrated

**Data cleaning & validation**
- Null detection and silent type coercion debugging (`keep_default_na`)
- Referential integrity checks (FK validation across joined tables)
- Date sequencing validation (shipping vs. order date logic)
- Defensive whitespace normalization across all string columns

**Analysis techniques**
- Funnel analysis across a multi-stage order lifecycle
- Revenue segmentation by category, status, and time period
- Month-over-month delta calculation
- Concentration risk identification (category revenue share)

**Tools & platforms**
- Excel — pivot tables, conditional formatting, embedded bar / line /
  pie charts, frozen panes, auto-filters
- Power BI Desktop — data modeling, DAX (CALENDAR table), funnel chart,
  donut chart, line chart, slicers, cross-filter interactivity
- pandas — data auditing, type casting, datetime parsing, group
  aggregations

**Soft skills**
- Structured a full data quality log before any analysis
- Translated raw numbers into executive-ready recommendations
- Documented every assumption and decision for reproducibility

---

## Key findings

| Finding | Detail |
|---------|--------|
| Delivery rate | Only **43.3%** of orders reach Delivered |
| Revenue at risk | **29%** of orders lost to returns (14.3%) and cancellations (14.7%) |
| Category concentration | **Electronics = 68%** of total revenue — single-category dependency |
| Seasonality gap | Revenue flat at ~$95–105K/month except December (+21% spike) |
| Payment behavior | All 5 methods split evenly at ~20% — checkout is not the bottleneck |

---

## Recommendations

**1. Investigate the 29% drop-off rate — highest priority**
Nearly 1 in 3 orders never completes. Before spending on acquisition,
identify whether returns and cancellations are driven by product quality,
inaccurate listings, pricing mismatch, or fulfillment delays. A 10%
reduction in churn recovers ~$68K in annual revenue.

**2. Diversify category revenue**
Electronics carrying 68% of revenue is a concentration risk. Clothing
and Home & Kitchen need dedicated promotional investment to build a
meaningful revenue cushion against any Electronics demand softening.

**3. Build a mid-year demand strategy**
11 out of 12 months are flat. A structured Q2–Q3 promotional campaign
would reduce December dependency, smooth cash flow, and improve
annual predictability for inventory planning.

---

## Limitations & next steps

- **No customer demographics** — adding age, location, or acquisition
  channel would allow cohort-level churn analysis
- **No return reason codes** — the dataset flags returns but not why;
  capturing reason codes is the single highest-value data collection
  improvement
- **Static dataset** — connecting Power BI to a live data source would
  enable real-time monitoring of the funnel
- **No cost-of-acquisition data** — combining with CAC would allow full
  unit economics modeling (LTV:CAC ratio)

---

---

## How to view

| File | How to open |
|------|-------------|
| `.xlsx` | Microsoft Excel or Google Sheets |
| `.pbix` | [Power BI Desktop](https://powerbi.microsoft.com/desktop) — free |
| `.pdf` | Any PDF viewer — no software needed |
