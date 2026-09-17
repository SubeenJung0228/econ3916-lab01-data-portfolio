# The Data Portfolio — Big Mac Index Analysis

## Objective
This project applies purchasing power parity theory to The Economist's Big Mac Index panel dataset to quantify currency valuation gaps and evaluate the structural, methodological, and data-quality challenges inherent in cross-country economic measurement.

## Methodology
- Loaded a 57-country, 45-period panel dataset (2000-04 to 2026-07) from The Economist's public Big Mac Index repository, including a 54-country cross-section for July 2024
- Computed implied PPP exchange rates and currency valuation percentages relative to the US dollar using pandas
- Classified the dataset's structure across cross-sectional, time-series, and panel dimensions to determine appropriate analytical approaches for each research question
- Conducted a missingness audit across the panel, identifying incomplete country coverage and diagnosing the underlying mechanism (e.g., classifying Russia's 2022 exit as Missing Not At Random, driven by geopolitical sanctions rather than random data loss)
- Built visualizations, including a cross-sectional valuation bar chart and a multi-decade time-series comparison, to illustrate persistence and variation in currency misalignment

## Key Findings
- The Swiss franc emerged as the most persistently overvalued currency in the sample, trading at +41.8% above fair value in the July 2024 cross-section
- The Japanese yen showed sustained undervaluation across every decade in the dataset, pointing to structural rather than cyclical currency mispricing
- Missing-data analysis revealed that panel attrition is not random: countries exit the index primarily due to geopolitical and economic crises, meaning naive listwise deletion would bias aggregate valuation estimates toward understating true global currency dispersion
