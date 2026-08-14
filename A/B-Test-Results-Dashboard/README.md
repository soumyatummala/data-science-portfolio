# A/B Test Results Dashboard

**Live dashboard:** https://public.tableau.com/views/ABTestResultsDashboard_17866728098230/ABTestResultsDashboard?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link

## Overview
Analyzed a marketing A/B test (Control vs. Test campaign) using Tableau,
applying statistical rigor beyond a simple bar comparison — confidence
intervals and significance checking, not just "which bar is taller."

## Key Findings
- **Purchase rate:** Control 0.59% [95% CI: 0.58%–0.60%] vs. Test 0.97%
  [95% CI: 0.96%–0.99%]. The confidence intervals do not overlap,
  indicating the difference is statistically significant, not due to
  chance — Test drove a ~65% relative increase in purchase rate.
- **Click-through rate:** Control 4.9% vs. Test 8.1% — consistent
  directionally with the purchase rate finding, reinforcing that Test's
  advantage isn't isolated to one metric.

## Method notes
- Built calculated fields for conversion rate, sample size, and 95%
  confidence interval bounds using the standard proportion CI formula
  (±1.96 × standard error).
- Visualized confidence intervals as error bars using a dual-axis
  Gantt bar technique — a genuinely fiddly Tableau feature that took
  real iteration to get right (documented here as a learning note,
  since it's a common sticking point).
- Combined two separate campaign CSVs into one table using Tableau's
  Union feature before analysis.

## Tools & Methods
Tableau (calculated fields, dual-axis charts, Gantt bars for confidence
intervals, data union).

## Dashboard
<img width="635" height="751" alt="Screenshot 2026-08-13 at 7 03 21 PM" src="https://github.com/user-attachments/assets/15f8ecdd-8603-4c14-8492-6efd6ff786e3" />
