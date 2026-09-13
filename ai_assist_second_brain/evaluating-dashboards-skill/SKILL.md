---
name: evaluating-dashboards-for-decision-clarity
description: Help users evaluate and improve dashboards so they drive real decisions instead of passive reporting. Use when someone is designing, reviewing, or refining dashboards for clarity, actionability, and diagnostic strength.
---

# Evaluating Dashboards for Decision Clarity

Help the user review and strengthen dashboards using a decision-first framework grounded in product analytics and practical decision-making.

Dashboards are not summaries — they are decision instruments.

Evaluate in this order:
Purpose → Metric Integrity → Context → Segmentation → Diagnostics → Design → Signal-to-Noise

If tradeoffs exist, prioritize decision clarity and metric integrity over visual polish.

## How to Help

When reviewing a dashboard, move through these lenses in order:

1. **Clarify the decision (Purpose & Decision Fit)**  
   Ask what single decision this dashboard should influence, who uses it, and how often.

2. **Validate metric integrity**  
   Rewrite vague metrics (e.g., “active users,” “engagement”) into clear behavioral definitions. Ensure drivers and outcomes are structurally separated.

3. **Add interpretive context**  
   Strengthen each KPI with trend, delta, target, benchmark, or cohort comparison. Ask: “Compared to what?”

4. **Check segmentation risk**  
   Add meaningful breakdowns (channel, device, cohort, geography, plan tier) to prevent misleading aggregates.

5. **Strengthen diagnostic flow**  
   Ensure that when a top KPI moves, users can see why within one screen.

6. **Improve visual clarity**  
   Remove distortion, inconsistent scales, and decorative elements that distract from the decision.

7. **Increase signal-to-noise**  
   Remove elements that don’t directly support the primary decision.

## Core Principles

### Dashboards exist to drive a single decision
Avoid “overview” pages that mix unrelated metrics or timeframes. Every dashboard should clearly answer one primary question.

### Match time horizon to intent
Daily dashboards focus on inputs and operational health.  
Weekly dashboards focus on execution trends.  
Quarterly dashboards focus on outcomes and strategic progress.  
Do not mix these on one screen.

### Metrics must be behaviorally defined
Replace generic labels with measurable actions.  
Example:  
“Active users” → “Users who completed ≥1 core action in the past 7 days.”  
If a metric cannot be operationally defined, it cannot support confident decisions.

### Every number needs context
Raw numbers invite narrative bias. Every KPI should include:
- A trend
- A period-over-period change
- A target line
- A benchmark
- Or a cohort comparison  

Ask: “Compared to what?”

### Separate drivers from outcomes
Activation, onboarding completion, and feature usage are drivers.  
Revenue, retention, and churn are outcomes.  
Structure dashboards to reflect causal flow, not metric clutter.

### Segment to avoid false signals
Aggregate metrics can hide divergent trends (e.g., Simpson’s paradox).  
Include meaningful breakdowns by:
- Acquisition channel
- Device
- Plan tier
- Geography
- User cohort

### Diagnose before you scroll
If the primary KPI changes, the likely cause should be visible within one screen. Dashboards should reduce investigation time, not create meetings.

### Remove to improve
If a visual does not influence a decision, remove it. Clarity increases by subtraction.

## Questions to Help Users

- "What single decision should this dashboard inform?"
- "Who uses this dashboard, and how often do they act on it?"
- "Which KPIs are drivers versus outcomes?"
- "What would trigger intervention?"
- "Does every KPI have a trend, delta, or target?"
- "If this top metric dropped, could you quickly see why?"
- "What segmentation would most likely change the story?"
- "What could we remove without weakening the decision?"

## Common Mistakes to Flag

- **No clear purpose** - Dashboard reads as a general overview without a core decision.
- **Mixed time horizons** - Daily metrics and quarterly outcomes shown together.
- **Passive KPIs** - Metrics displayed without thresholds, targets, or context.
- **Vague metric labels** - “Engagement,” “usage,” or “quality” without definition.
- **No segmentation** - Aggregates hiding variation across user types.
- **Isolated KPI tiles** - No supporting diagnostics or related breakdowns.
- **Visual clutter** - Decorative charts, excessive decimals, inconsistent scales.
- **Too much information** - Multiple unrelated metrics competing for attention.

## Deep Dive

For expanded evaluation breakdowns, see:

- section_A_purpose_decision_fit.md
- section_B_metric_integrity.md
- section_C_context_comparison.md
- section_D_segmentation_false_signal.md
- section_E_diagnostic_power.md
- section_F_visual_design.md
- section_G_signal_to_noise.md
