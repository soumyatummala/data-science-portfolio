# Customer Churn Analysis Dashboard

**Live dashboard:** (https://public.tableau.com/views/CustomerChurnAnalysisDashboard_17865710361500/Dashboard1?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)]

## Overview
Analyzed churn drivers across 7,043 telecom customers using Tableau.
Tested six candidate churn drivers and checked each for confounding
before drawing conclusions, rather than reporting raw correlations
at face value.

## Key Findings
- **Contract type** is the strongest driver — Month-to-month customers
  churn at ~43% vs. ~2.5% for two-year contracts (a 15x+ difference).
- **Tenure** shows a clean, consistent decline in churn as customers
  stay longer — new customers (0-12 months) are the highest-risk group.
- **Lack of tech support** independently increases churn (~42% vs ~15%),
  even after controlling for internet service type.
- **Senior citizens** churn more than non-seniors, and this holds even
  after controlling for contract type — though part of the raw gap is
  explained by seniors skewing toward month-to-month plans.
- **Payment method's** apparent effect (Electronic check showing highest
  churn) is largely explained by its correlation with contract type,
  not an independent driver — a hypothesis I tested and ruled out.

## Tools & Methods
Tableau (calculated fields, binning, cross-tabulation), confound
analysis via segmented comparison.



