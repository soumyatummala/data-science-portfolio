# Credit Card Fraud Detection Dashboard

**Live dashboard:** https://public.tableau.com/views/FraudDetectionDashboard_17865105407440/CreditCardFraudMonitoringDashboard?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link

## Overview
Analyzed 284,807 credit card transactions (492 fraudulent, ~0.17% fraud
rate) using Tableau to identify patterns in when and how fraud occurs.
Built with attention to a key challenge in fraud data: extreme class
imbalance, and the risk of drawing conclusions from small sample sizes.

## Key Findings
- **Fraud rate is not linear with transaction amount.** Rather than
  increasing steadily with amount, fraud rate peaks in the mid-range
  ($250–$1,000) and is actually lower in the highest amount bracket —
  suggesting fraudulent transactions may be deliberately sized to avoid
  scrutiny thresholds banks apply to large purchases.
- **Class imbalance is severe** — legitimate transactions outnumber
  fraudulent ones roughly 578 to 1, which shapes how any downstream
  model or alerting system would need to be evaluated (accuracy alone
  would be a misleading metric here).
- **Transaction volume follows a clear daily cycle** — low overnight,
  rising sharply during daytime hours — useful context for distinguishing
  unusual timing from normal patterns.

## Method notes
- Built a `Risk Bucket` calculated field (Low/Medium/High, based on
  transaction amount) and validated it by confirming fraud rate actually
  increased across buckets, rather than assuming the buckets were
  meaningful by construction.
- Checked sample size behind each bucket before trusting a rate —
  one early amount-bin spike turned out to be backed by a reasonably
  large sample (n=3,069) and held up; this habit of checking counts
  before drawing conclusions was applied throughout.
- Truncated the x-axis on the amount-bucket chart (excluding a long,
  sparse tail above $2,500) to keep the chart readable without hiding
  the underlying pattern.

## Tools & Methods
Tableau (calculated fields, binning, axis scaling for skewed data).

## Dashboard
![dashboard screenshot](screenshots/fraud_dashboard.png)
