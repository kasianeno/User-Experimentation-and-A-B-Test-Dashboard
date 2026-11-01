# User-Experimentation-and-A-B-Test-Dashboard
The goal of the project is to analyze the results of A/B testing using statistical methods in Python and to create a visualization that demonstrates key conversion metrics.

## Stage 1. Statistical significance calculation.

Previously, I analyzed statistical significance using online calculators, which is not very convenient. Therefore, the first and largest stage of the project is to improve the calculation of statistical significance using a Python script.

1. Using SQL and the dataset I worked with, I created my A/B Testing Tool. This tool helped me to extract and aggregate session-level data broken down by A/B test name and group number to power a Tableau dashboard.

2. Created a notebook in Google Colab and calculated statistical significance for the following four metrics:
  add_payment_info / session
  add_shipping_info / session
  begin_checkout / session
  new_accounts / session
3. Calculate significance for the total test, and also the results across all possible breakdowns (by tests, countries, devices, etc.).


## Stage 2. Visualization in Tableau.

1. Visualized the file from Stage 1. The dashboard displays the values of the four main metrics and shows where the changes are statistically significant and where they are not.
2. Added a filter by test number.

[Tableau Dashboard](https://public.tableau.com/views/ABTest_17675349607140/ABTest?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

## Summary

Conducted A/B testing (4 experiments) to optimize the checkout flow.

Identified **statistically significant uplift** of **up to +12.5%** in add_payment_info and **+6–7% across key funnel stages** (Test 1).

Detected **negative impact** in Test 3–4 → conversion **decreased by up to -3.3%** at the checkout stage.

Performed **device-level segmentation** → found **-15.6% drop** in conversion for tablet users.

Discovered variability across countries → identified markets with up **to +95% uplift** (low-base effect)

Validated statistical test assumptions → identified edge cases (NaN p-values) caused by zero-event scenarios

Provided data-driven recommendations → approved rollout for Test 1 and rejected other variants
