# GoodNews National Bookstore — Sales Performance Dashboard

An interactive Tableau dashboard built to help a marketing manager diagnose a
year-over-year sales decline and identify where to focus recovery campaigns.

<img width="672" height="665" alt="Screenshot 2026-07-12 at 6 04 53 pm" src="https://github.com/user-attachments/assets/dd2847a4-5e31-412f-8616-35a1835bcdbf" />



📊 **[View interactive dashboard on Tableau Public](https://public.tableau.com/views/HanLe_Backup31/Dashboard1)**

## Business Problem

GoodNews National Bookstore has seen a sharp year-over-year sales decline.
The Marketing Manager needs to quantify how severe it is, identify which
customer segments are driving it, and decide what kind of campaign is most
likely to recover revenue — backed by data rather than guesswork.

## Approach

Build an interactive dashboard that lets the Marketing Manager go from a
single question — "why are sales down, and what do we do about it?" — to a
concrete, segment-specific marketing plan, without needing to touch the raw
data herself.

## Steps

**Technical: raw data → dashboard**
1. Started with raw transaction data in Excel ([`T22025A3.xlsx`](./T22025A3.xlsx))
   — roughly 30–40% of the 6,380 records needed cleaning, mainly
   inconsistent formatting and duplicate entries
2. Cleaned the data in Excel:
   - Removed duplicate transaction records
   - Handled missing values — imputed with **mean** for continuous numeric
     fields (e.g. price) or **mode** for categorical fields, depending on
     the variable
   - Standardized formatting: currency, percentages, date fields (DD/MM/YYYY),
     and inconsistent text casing across categorical columns
3. Used **pivot tables** to quickly check the cleaned data: Gross Sales figures reconciled correctly against Quantity ×
   UnitPrice, and discounted amounts matched the applied Discount Rate,
   before trusting the numbers in Tableau
4. Brought the cleaned data into Tableau Desktop and built calculated
   fields 
5. Designed the dashboard layout and chart types around the target
   persona's decision-making flow (see [DESIGN-NOTES.md](./DESIGN-NOTES.md))

**Business: data → insight → recommendation**
1. **Data:** 6,380 transactions across customer segments, product categories,
   locations, and time
2. **Insight:** analyzed the dashboard section by section — overall KPIs,
   segment performance, monthly seasonality, and the 4Ps — to find where
   revenue was lost and why (see [ANALYSIS.md](./ANALYSIS.md))
3. **Recommendation:** turned those insights into a prioritized, segment-by-
   segment 4Ps marketing strategy — who to target, what to offer, and when
   (see [RECOMMENDATIONS.md](./RECOMMENDATIONS.md))

## Results

Built a **4Ps marketing strategy (Place, Product, Promotion, Price)** for
each of the five customer segments, then translated it into a practical
yearly targeting plan so the business knows, month by month, where to spend
its marketing effort:

| When | Focus Segment | Book Focus | Approach |
|---|---|---|---|
| Jan–Feb | Student, Parent | Textbooks, Non-Fiction | Semester-start / school-term push — Student10 & Member15 codes |
| Mar, Jun | Professional | Fiction, Textbook | Quarterly pay-cycle campaign — loyalty perks, not discounts |
| Jul–Aug | Student | Non-Fiction, Textbook | Mid-year "Back to School" bundles |
| Sep | Professional, Parent | Business/self-development, Textbook | Quarterly + term-refresh overlap |
| Oct–Nov | Retiree | Fiction, Non-Fiction | Off-peak premium/curated bundles, loyalty rewards |
| Dec | Professional | Fiction, Textbook | Quarterly pay-cycle campaign |

The intent behind this plan is **profit-conscious, not discount-heavy**:
segments like Professional, Parent, and Retiree show low promotion
reliance in the data, so their campaigns lean on loyalty perks and curated
offers rather than blanket discounts — protecting margin. Only Student,
which responds clearly to promo codes, gets discount-led offers, and only
in the windows tied to their actual buying pattern. This keeps discounting
targeted instead of applied broadly, aiming to retain customers and grow
revenue without eroding profit.

Also produced **3 ready-to-brief campaigns** — *"Learn & Grow"*
(Professional), *"Back-to-School Smart Savings"* (Student), and *"Family
Reading Month"* (Parent) — full detail in
[RECOMMENDATIONS.md](./RECOMMENDATIONS.md).

## Tools & Skills

- **Excel** — data cleaning (deduplication, missing-value imputation,
  formatting standardization), pivot tables for data validation
- **Tableau Desktop** — calculated fields, interactive filters, dashboard
  design
- **Tableau Public** — publishing for live, interactive access

## Repo Contents

| File | What's in it |
|---|---|
| [`README.md`](./README.md) | This page — project overview and business problem |
| [`ANALYSIS.md`](./ANALYSIS.md) | Business insights from the dashboard, by section: Key Metrics, Segment Performance, Monthly Metrics, 4Ps |
| [`RECOMMENDATIONS.md`](./RECOMMENDATIONS.md) | 4Ps marketing strategy and campaign recommendations per segment |
| [`DESIGN-NOTES.md`](./DESIGN-NOTES.md) | Design rationale — target audience/persona, why each chart type was chosen, data ethics considerations |
| [`data-dictionary.md`](./data-dictionary.md) | Description and type of all 29 columns in the dataset |
| [`T22025A3.xlsx`](./T22025A3.xlsx) | Raw transaction data — cleaned before use in Tableau |
| `dashboard.twbx` | Tableau packaged workbook (source file) |
| `screenshot.png` | Static preview of the dashboard |
