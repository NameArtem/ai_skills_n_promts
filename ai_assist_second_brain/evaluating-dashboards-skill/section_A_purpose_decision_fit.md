# Purpose & Decision Fit

Help users ensure every dashboard exists to answer one explicit decision at a defined cadence, with metrics that trigger action.

## Principle

Dashboards are operational instruments. They exist to influence a recurring decision at a specific cadence.

If the decision is unclear, the dashboard will default to passive reporting.

---

## Detailed Checks

### 1. Single Decision Test

Ask:
- Can the primary purpose be written as a single question?
- Does the dashboard title reflect that question?
- Would two different stakeholders describe its purpose the same way?

Red flags:
- Titles like “Executive Overview,” “Marketing Snapshot,” or “Product Dashboard.”
- Multiple large KPI tiles that imply different strategic narratives.
- Metrics grouped by function instead of decision (e.g., “Revenue,” “Traffic,” “Bugs,” all side-by-side).

---

### 2. Decision Horizon Alignment

Check cadence consistency:

Daily dashboard should:
- Emphasize anomalies
- Highlight exceptions
- Surface operational drivers

Quarterly dashboard should:
- Emphasize trends
- Show progress against goals
- Focus on outcomes, not inputs

Red flags:
- Showing hourly ad spend on a quarterly strategy dashboard.
- Displaying 3-year retention curves in a daily standup view.
- Mixing system uptime (operational) with ARR growth (strategic).

---

### 3. Trigger Condition Presence

For each primary KPI:

- Is there a target?
- Is there a tolerance band?
- Is there an intervention threshold?

Red flags:
- KPI tile shows “Retention = 84%” with no indicator of whether that’s good.
- Teams reviewing dashboards weekly but never changing plans.
- Targets exist in OKRs but not on the dashboard.

---

## Expanded Example Failures

- “Growth Dashboard” mixing acquisition, churn, NPS, and engineering velocity.
- Board slide screenshot reused as operational dashboard.
- Marketing dashboard including both campaign CTR and 3-year customer LTV.
- KPI tile with green up-arrow but no definition of acceptable range.