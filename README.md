# Procurement & Supplier Performance Analytics

### Turning procurement transactions into defensible supplier decisions

**Excel · Power Query · PivotTables · Advanced Formulas · Procurement
Analytics**

> **The cheapest supplier is not always the lowest-cost supplier.**\
> This project evaluates supplier performance beyond quoted
> prices---combining delivery reliability, quality, cost, and lead-time
> consistency to identify operational and financial exposure.

------------------------------------------------------------------------

## The business question

**Which suppliers should procurement retain, develop, monitor, or
review---and what risks are hidden by headline prices and aggregate
performance scores?**

A supplier can appear competitive on unit price while generating
additional costs through defects or unreliable delivery. Similarly, a
strong composite score can obscure weaknesses in individual KPIs.

I built a refreshable Excel decision-support model to connect
transaction-level procurement data with supplier-level performance,
spending exposure, and prioritized management actions.

## What the analysis found

  -----------------------------------------------------------------------
  Finding                 Evidence                Decision implication
  ----------------------- ----------------------- -----------------------
  **Risk is financially   **3 High-Risk suppliers Prioritize
  material**              account for 24% of      corrective-action
                          analyzed spend**        reviews and assess
                                                  contingency sourcing.

  **Exposure extends      **₹177M (31.6%)** of    Monitor supplier
  beyond the highest-risk spend is with Watchlist exposure alongside
  tier**                  or High-Risk suppliers  performance ratings.

  **Open orders need      **₹41M (7.3%)** in      Review overdue
  attention**             open-order value is     commitments and
                          past expected delivery  escalate critical
                                                  orders.

  **Low price can conceal One supplier's          Evaluate
  higher effective cost** **−4.7%** variance to   defect-adjusted cost,
                          standard cost became    not unit price alone.
                          **+0.7%** after adding  
                          estimated defect value  

  **Rankings are          Delivery- and           Use sensitivity
  reasonably stable**     quality-focused         analysis to test
                          scenarios yielded       whether prioritization
                          **rank correlation ≥    depends heavily on
                          0.97** and a **maximum  scoring weights.
                          three-place move**      
  -----------------------------------------------------------------------
## How I built it

**01  Prepare and validate the data**\
Used **Power Query** to clean and de-duplicate purchase-order records,
standardize supplier/material identifiers, and apply KPI-specific
validity checks. The quality audit identified **374 lines (5.3%)** with
missing or unmatched supplier IDs and a **213-day lead-time outlier**.
Exclusions and limitations are disclosed rather than silently removed.

**02  Develop decision-oriented KPIs**\
Calculated supplier-level delivery reliability, defect performance,
price variance, spend share, and lead-time reliability. Connected
line-level transactions to supplier-level reporting with Excel formulas,
including **SUMPRODUCT** and **INDEX-MATCH**.

**03  Build an explainable supplier scorecard**\
Designed a four-factor scoring model with editable weights and
floor/target normalization. Suppliers were segmented into **Strategic
(6)**, **Preferred (7)**, **Watchlist (3)**, and **High Risk (3)**. The
weights and scoring thresholds are **analyst-defined assumptions**, not
industry-certified standards.

**04  Test concentration and robustness**\
Applied supplier spend concentration analysis and tested alternative
**delivery-focused** and **quality-focused** weighting scenarios.
Compared supplier ranks to assess sensitivity before making
recommendations.

**05 Communicate decisions**\
Delivered a one-page executive dashboard with **KPI cards, PivotCharts,
slicers, conditional formatting, and formula-driven commentary**,
supported by a decision brief and a data-quality report.

## Recommended management actions

1.  **Address delivery risk:** Review overdue open orders and establish
    supplier-specific corrective-action plans with measurable delivery
    targets.
2.  **Manage supplier exposure:** Prioritize High-Risk and Watchlist
    suppliers by both performance and spend; evaluate dual-sourcing
    where operationally justified.
3.  **Use defect-adjusted cost comparisons:** Investigate apparently
    low-cost suppliers whose quality losses erode their price advantage.
4.  **Keep the scorecard explainable:** Review individual KPIs,
    normalization anchors, and sensitivity results before changing
    sourcing decisions.
5.  **Improve data controls:** Resolve unmatched supplier IDs,
    investigate outliers, and monitor data completeness in each refresh
    cycle.

  -----------------------------------------------------------------------


### Project takeaway

**A supplier score is useful only when decision-makers can explain what
it rewards---and what it might hide.** This project connects transparent
data preparation, interpretable scoring, and business-oriented
recommendations so procurement teams can move from reporting metrics to
prioritizing action.

