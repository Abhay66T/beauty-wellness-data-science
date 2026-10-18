# Analysis plan

## Goal
Understand factors associated with online beauty product conversion and repeat purchase.

## Required inputs
- Product/session funnel events with timestamps
- Orders with pseudonymous customer IDs (if retention analysis is needed)
- Product catalogue and price/discount data
- Review rating/count fields, where available
- Marketing source/campaign and spend, where available
- Stock status and returns/cancellations, where available

## Work stages
1. Define event and KPI denominators.
2. Validate access permissions and remove or pseudonymise direct identifiers.
3. Audit data types, missingness, duplicates, timestamps, category labels, and joins.
4. Create a documented analysis-ready dataset.
5. Produce descriptive summaries and funnel/category/channel charts.
6. Compare segments with uncertainty intervals and appropriate statistical tests.
7. If data volume and labels are suitable, test an interpretable predictive baseline with time-aware validation.
8. Translate findings into testable recommendations and an experiment plan.

## Guardrails
- Do not upload personal data or secrets to this public repository.
- Correlation is not causation.
- Avoid medical or sensitive inferences.
- Document sample sizes, exclusions, assumptions, and limitations.
