# Procurement & Supplier Performance Analytics

### Turning procurement transactions into defensible supplier decisions

**Excel · Power Query · PivotTables · Advanced Formulas · Procurement
Analytics**

> **The cheapest supplier is not always the lowest-cost supplier.**\
> This project evaluates supplier performance beyond quoted
> prices---combining delivery reliability, quality, cost, and lead-time
> consistency to identify operational and financial exposure.

**Project snapshot**

    Purchase-order lines   Analyzed spend   Suppliers   Risk tiers
  ---------------------- ---------------- ----------- ------------
               **7,000**        **₹562M**      **19**        **4**

*Independent portfolio project using simulated procurement data. Results
represent analytical findings, not realized business savings.*

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

**Important:** The defect-adjusted cost comparison is a modeled
analytical view, not a fully measured total cost of ownership. It does
not include all possible return, rework, disruption, or warranty costs.

## How I built it

**01 --- Prepare and validate the data**\
Used **Power Query** to clean and de-duplicate purchase-order records,
standardize supplier/material identifiers, and apply KPI-specific
validity checks. The quality audit identified **374 lines (5.3%)** with
missing or unmatched supplier IDs and a **213-day lead-time outlier**.
Exclusions and limitations are disclosed rather than silently removed.

**02 --- Develop decision-oriented KPIs**\
Calculated supplier-level delivery reliability, defect performance,
price variance, spend share, and lead-time reliability. Connected
line-level transactions to supplier-level reporting with Excel formulas,
including **SUMPRODUCT** and **INDEX-MATCH**.

**03 --- Build an explainable supplier scorecard**\
Designed a four-factor scoring model with editable weights and
floor/target normalization. Suppliers were segmented into **Strategic
(6)**, **Preferred (7)**, **Watchlist (3)**, and **High Risk (3)**. The
weights and scoring thresholds are **analyst-defined assumptions**, not
industry-certified standards.

**04 --- Test concentration and robustness**\
Applied supplier spend concentration analysis and tested alternative
**delivery-focused** and **quality-focused** weighting scenarios.
Compared supplier ranks to assess sensitivity before making
recommendations.

**05 --- Communicate decisions**\
Delivered a one-page executive dashboard with **KPI cards, PivotCharts,
slicers, conditional formatting, and formula-driven commentary**,
supported by a decision brief and a data-quality report.

## Dashboard preview

![Procurement and supplier performance
dashboard](screenshots/executive_dashboard.png)

*Add a screenshot named `executive_dashboard.png` to the `screenshots/`
folder. The image above will display after it is uploaded.*

### Dashboard views

-   Procurement spend and monthly trends
-   Supplier spend and performance rankings
-   Supplier risk classification
-   Pareto / spend concentration
-   Risk watchlist and executive recommendations

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

## Tools & methods

  -----------------------------------------------------------------------
  Area                                Implementation
  ----------------------------------- -----------------------------------
  Data preparation                    Excel Power Query; validation,
                                      de-duplication, ID matching

  Analysis                            Excel formulas; SUMPRODUCT,
                                      INDEX-MATCH; supplier KPIs

  Scoring                             Four-component normalized model;
                                      editable weights and thresholds

  Risk analysis                       Four-tier segmentation;
                                      overdue-order exposure;
                                      defect-adjusted cost

  Robustness                          Scenario reweighting; rank
                                      correlation and rank movement

  Reporting                           PivotTables, PivotCharts, slicers,
                                      KPI cards, executive dashboard
  -----------------------------------------------------------------------

## Explore the project

  ----------------------------------------------------------------------------------
  File / folder                                  What it contains
  ---------------------------------------------- -----------------------------------
  `dashboard/Procurement_Analytics_Final.xlsx`   Working Excel model, dashboard, and
                                                 supporting analyses

  `screenshots/`                                 Dashboard, scorecard,
                                                 concentration, and sensitivity
                                                 previews

  `documentation/`                               Methodology, data-quality
                                                 decisions, and business insights
  ----------------------------------------------------------------------------------

**To explore:** Download the workbook and open it in **Microsoft Excel
desktop**. GitHub does not reproduce the full interactive
PivotChart/slicer experience.

## Scope, assumptions & limitations

-   **Data provenance:** Simulated procurement records; findings
    demonstrate an analytical method, not results from a live
    organization.
-   **Spend scope:** Reported spend and supplier shares refer to the
    eligible analytical population; excluded or unmatched records are
    tracked separately.
-   **Scoring:** Floor/target anchors, weights, and tier cutoffs are
    configurable modeling choices. A tier is a **review signal**, not an
    automatic supplier-approval decision.
-   **Open-order exposure:** Overdue order value indicates commitments
    requiring follow-up, **not a realized financial loss**.
-   **Defect costs:** Estimated defect value is used as a cost proxy; it
    does not establish full cost of poor quality.
-   **Refresh:** Validate query refresh, dependent formulas,
    PivotTables, and dashboard outputs after any source-data change.

------------------------------------------------------------------------

### Project takeaway

**A supplier score is useful only when decision-makers can explain what
it rewards---and what it might hide.** This project connects transparent
data preparation, interpretable scoring, and business-oriented
recommendations so procurement teams can move from reporting metrics to
prioritizing action.

*Portfolio project · Microsoft Excel / Power Query · Simulated dataset*
