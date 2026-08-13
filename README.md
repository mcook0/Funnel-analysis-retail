# E-Commerce Funnel Analysis | Excel · Power BI · Data Cleaning · Business Intelligence

> Identified **$680K+ in at-risk revenue** across 5,000 orders by mapping
> the full order lifecycle and pinpointing where — and why — customers
> were dropping off before delivery.

---

## Executive Summary

Using Excel and Power BI, I analyzed order and product data from an
e-commerce business and built a dashboard to track orders through the
fulfillment funnel. After identifying that the largest revenue
opportunities are to reduce the 29% order drop-off rate from returns
and cancellations, and to grow underperforming categories beyond
Electronics, I recommend that the business team implements a few
adjustments that will lead to higher revenue and stronger margins:

1. Investigate and fix the root causes of returns and cancellations
2. Launch mid-year promotional campaigns to reduce December dependency
3. Invest in Clothing and Home & Kitchen to reduce category concentration risk

## Business problem

An e-commerce business was seeing steady order volume but shrinking
margins. Leadership needed to understand whether the problem was in
acquisition, fulfillment, product mix, or customer behavior — and where
to focus first to stop the revenue leak.

**How can the business recover lost revenue and build a more resilient
order funnel without increasing customer acquisition costs?**

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

1. **Fix the 29% drop-off rate before spending on acquisition** — investigate
   whether returns and cancellations are driven by product quality, inaccurate
   listings, or fulfilment delays. A 10% improvement recovers ~$68K annually
   at zero acquisition cost.

2. **Diversify category revenue** — shift promotional budget toward Clothing
   and Home & Kitchen to reduce Electronics dependency and build a more
   resilient funnel.

3. **Launch a mid-year campaign** — a Q2–Q3 promotional push would fill the
   flat revenue months and reduce December dependency without needing
   new customers at the top of the funnel.
---

## Limitations & next steps

- **No return reason codes** — capturing why customers cancel or return is
  the single highest-value data improvement to answer the business question
- **No customer acquisition cost data** — adding CAC would reveal whether
  fixing retention is cheaper than replacing lost customers
- **Static dataset** — connecting Power BI to a live source would allow
  real-time funnel monitoring
- **No product-level breakdown** — identifying which SKUs drive the most
  drop-off would sharpen recommendation #1 significantly
---

## Deliverables

├── data/
│ ├── orders.csv
│ ├── products.csv
│ ├── orders_powerbi.csv
│ └── products_powerbi.csv
├── excel/
│ └── funnel_analysis_excel_only.xlsx
├── powerbi/
│ ├── funnel_analysis.pbix
│ └── funnel_analysis_dashboard.pdf
└── README.md
---

## How to view

| File | How to open |
|------|-------------|
| `.xlsx` | Microsoft Excel or Google Sheets |
| `.pbix` | [Power BI Desktop](https://powerbi.microsoft.com/desktop) — free |
| `.pdf` | Any PDF viewer — no software needed |
