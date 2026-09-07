# WHO Water Access: Rural vs. Urban Inequalities

## Overview
This project analyzes global inequalities in access to safely managed drinking water, focusing on the disparity between rural and urban populations. Using nationally representative data collected by the WHO and UNICEF, this report tests whether recent global gains in water access are masking underlying geographic inequalities.

## Methodology
Because the country-level coverage data violated the normality assumptions required for classical parametric testing, the analysis relies on a **Paired Permutation Test** to assess the true difference in proportions.
* Checked assumptions for independence, exchangeability, and equal measurement scale.
* Simulated a null distribution using 100,000 permutations.
* Reshaped and cleaned data using `dplyr` and `tidyr` (`pivot_wider`, `left_join`).

## Key Findings
* **Statistically Significant Gap:** Urban areas have, on average, a 13.05 percentage point higher clean-water coverage rate than rural areas.
* **Zero Permutations Reached Observed:** With a p-value of 0 across 100,000 permutations, there is significant evidence that rural communities are systematically experiencing worse access to safely managed water.
* **Bimodal Tendencies:** Exploratory Data Analysis (EDA) using `ggplot2` revealed bimodal tendencies in global coverage, with a stark divide between near-universal access countries and those struggling to provide basic infrastructure.

## Tools & Libraries
* **Language:** R
* **Libraries:** `tidyverse`, `ggplot2`, `patchwork`, `dplyr`
* **Deliverable:** R Markdown (`github_document`)

## Author Contributions
I developed the `ggplot2` boxplot visualizations for the exploratory data analysis and authored the final results and conclusion sections, translating the output of the paired permutation test into actionable public health insights.
