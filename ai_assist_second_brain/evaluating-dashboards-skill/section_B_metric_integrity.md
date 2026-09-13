# Metric Integrity

Ensure every KPI is behaviorally defined, temporally consistent, and analytically distinct.

## Principle

Metrics are contracts. If they are vague or inconsistent, trust degrades and debates replace decisions.

---

## Detailed Checks

### 1. Behavioral Definition Clarity

Each KPI must specify:

- Entity (user, account, session)
- Action (specific event)
- Time window
- Denominator

Red flags:
- “Engagement” without defined event set.
- “Adoption” without feature usage criteria.
- “Activation” without milestone clarity.

---

### 2. Window Consistency

Verify:

- Rolling windows vs calendar windows clearly labeled.
- No mixing “last 30 days” with “QTD” in adjacent charts.
- Cumulative metrics visually separated from period metrics.

Red flags:
- 7-day rolling DAU next to total lifetime users.
- Revenue cumulative since launch plotted next to monthly churn.
- Weekly retention plotted against monthly acquisition.

---

### 3. Leading vs Lagging Structure

Drivers (leading):
- Onboarding completion
- Feature adoption
- Engagement frequency

Outcomes (lagging):
- Revenue
- Retention
- Churn
- LTV

Red flags:
- Feature clicks plotted next to ARR with no structural grouping.
- Lagging KPI visually dominant while drivers hidden.

---

## Expanded Example Failures

- “Active accounts” defined differently across charts.
- Same metric labeled differently in separate widgets.
- Retention defined as 30-day in one chart, 28-day in another.
- Engagement plotted without normalization by user base.