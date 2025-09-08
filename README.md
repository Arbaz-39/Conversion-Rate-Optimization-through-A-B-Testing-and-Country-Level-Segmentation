Problem Statement:
A company introduced a new landing page with the expectation that it would increase 
user conversion rates compared to the existing page. However, rolling out a new design
globally is costly and risky without statistical evidence of improvement. The goal of 
this project is to evaluate whether the new landing page truly leads to higher conversions.

Objective:
Compare conversion rates between control group (old page) and treatment group (new page).
Use statistical methods (hypothesis testing, bootstrap resampling, two-proportion z-test, 
and confidence intervals) to test for significance.
Merge additional country-level data to explore whether treatment effects vary across US, UK, and Canada.
Provide a business recommendation on whether to roll out the new landing page globally.

Methodology
1. Data Cleaning:
Removed mismatched rows where treatment users saw old pages or control users saw new pages.
Dropped duplicates and ensured unique user IDs.

2. Exploratory Data Analysis (EDA):
Checked group distribution (balanced between treatment & control).
Calculated baseline conversion rates.

3. Hypothesis Testing:
H₀ (Null Hypothesis): Conversion rate (treatment) = Conversion rate (control).
H₁ (Alternative Hypothesis): Conversion rate (treatment) ≠ Conversion rate (control).

4. Bootstrap Resampling:
Simulated 10,000 samples of conversion rate differences.
Plotted sampling distribution to approximate the null distribution.

5. Confidence Intervals:
Constructed 95% CI for treatment–control conversion difference.
CI included 0, meaning no statistically significant effect.

6. Two-Proportion Z-Test:
Performed z-test on conversion rates.
P-value > 0.05 → fail to reject the null hypothesis.

7. Country-Level Analysis:
Merged countries.csv to segment users by US, UK, CA.
Conducted separate z-tests for each country.
Found no country showed statistically significant improvement in conversion.

8. Visualization:
Histograms of bootstrap sampling distribution.
Bar plots of conversion rates by group and country.

Key Results:
Overall Conversion Rate
Control: 12.04%
Treatment: 11.88%
Observed Difference: –0.16%
95% Confidence Interval: [–0.39%, +0.08%] → includes zero.
Two-Proportion Z-Test: p-value = 0.1899 → not significant.

Country Analysis:
US: slight drop in treatment vs control.
UK: almost identical performance.
CA: slight drop in treatment vs control.
None statistically significant.

Business Recommendation:
The new landing page does not provide a statistically significant improvement over the old page.
Conversion differences are minimal and within random variation.
Global rollout is not recommended.

Suggested next steps:
Test new design variations with larger samples.
Explore segmented experiments (e.g., device type, new vs returning users).
Consider improving page speed, content relevance, or personalization.


