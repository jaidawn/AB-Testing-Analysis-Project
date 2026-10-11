 🛒 A/B Testing: Checkout Redesign Experiment
A/B Testing Analysis using Python — Evaluates an experiment's control and treatment groups to measure conversion performance, validate random assignment, and derive data-driven insights for business decision-making. Uses Python, Pandas, NumPy, and statistical hypothesis testing.

# 📌 Project Overview

This project analyzes an e-commerce checkout redesign using **A/B testing and statistical hypothesis testing** to determine whether the new checkout experience improves user conversion and generates a positive business impact.

#The experiment compares two groups:

- Control Group: Users who experienced the original checkout.
- Treatment Group: Users who experienced the redesigned checkout.

Using Python, I evaluated experiment integrity, conversion rates, average order value, revenue per user, statistical significance, and performance across customer segments to develop a data-driven launch recommendation.

🎯 Business Objectives

- Validate the integrity of the experiment and user assignments.
- Measure conversion rates for the control and treatment groups.
- Compare average order value and revenue per user.
- Determine whether the observed conversion difference is statistically significant.
- Analyze experiment performance by device and visitor type.
- Estimate the potential monthly revenue impact.
- Recommend whether to launch, reject, or retest the redesigned checkout.

## 🛠️ Tools & Technologies

- Python — Data analysis and statistical calculations
- Pandas — Data cleaning, manipulation, grouping, and aggregation
- NumPy — Numerical calculations
- SciPy — Statistical hypothesis testing
- Matplotlib / Seaborn — Data visualization, where applicable
- Jupyter Notebook — Exploratory analysis and documentation

## 🔍 Project Workflow

### 1. Data Cleaning & Experiment Validation
- Loaded and inspected both datasets.
- Identified users assigned to both control and treatment groups.
- Removed ambiguous user assignments from the analysis.
- Identified orders placed before or at assignment time.
- Checked for orders from unassigned users.
- Verified the experiment's approximately 50/50 allocation.

### 2. KPI Calculation
Calculated the primary and supporting business metrics:

- **Conversion Rate:** Percentage of assigned users who placed at least one valid order.
- **Average Order Value (AOV):** Average value per valid order.
- **Revenue per User:** Total valid revenue divided by assigned users.
- **Total Revenue:** Sum of valid order values.

### 3. Statistical Hypothesis Testing
Compared conversion rates using a two-proportion z-test.

- **Null Hypothesis (H₀):** The control and treatment conversion rates are equal.
- **Alternative Hypothesis (H₁):** The control and treatment conversion rates are different.
- **Significance Level:** 5% (α = 0.05).
- Calculated the p-value and 95% confidence interval for the conversion-rate difference.

### 4. Segment Analysis
Evaluated conversion performance across:

- **Device:** Desktop, mobile, and tablet.
- **Visitor Type:** New and returning visitors.

Applied multiple-testing correction to segment-level comparisons to reduce the risk of false-positive findings.

### 5. Revenue Impact Estimation
Estimated the potential monthly revenue impact using the experiment's conversion-rate confidence interval, projected monthly user volume, and treatment-group average order value.

The results are presented as a range to reflect uncertainty rather than as a guaranteed revenue forecast.

### 6. Business Recommendation
Combined the statistical findings, segment results, and revenue estimates to recommend whether the redesigned checkout should be launched, rejected, or modified and retested.

## 📊 Key Results

| Metric | Control | Treatment |
|---|---:|---:|
| Assigned users | 15,339 | 15,377 |
| Converted users | 1,113 | 1,185 |
| Conversion rate | 7.26% | 7.71% |
| Average order value | 63.50 | 64.57 |
| Revenue per user | 5.13 | 5.54 |

*Values are based on the cleaned analysis and may be rounded.*

### Overall Experiment Findings

- **Absolute conversion uplift:** +0.45 percentage points.
- **Z-statistic:** Approximately 1.50.
- **P-value:** Approximately 0.134.
- **95% confidence interval:** −0.138 to +1.039 percentage points.
- **Statistical conclusion:** The overall conversion improvement is not statistically significant at the 5% level.

Although the treatment group recorded a higher observed conversion rate, the experiment does not provide sufficient evidence to conclude that the redesign improves conversion across the overall population.

### Segment-Level Findings

- **Desktop:** Conversion increased by approximately 2.27 percentage points, with a statistically significant result after multiple-testing correction.
- **Mobile:** Conversion decreased by approximately 1.32 percentage points, with a statistically significant result after multiple-testing correction.
- **Tablet:** Conversion decreased, but the result was not statistically significant after correction.
- **New visitors:** No statistically significant conversion improvement was detected.
- **Returning visitors:** The observed improvement was not statistically significant after multiple-testing correction.

Segment results should be interpreted carefully, particularly when several comparisons are performed.

### Estimated Monthly Revenue Impact

The estimated monthly revenue impact ranges from approximately **−2,610.64 to +21,219.71** in the dataset's currency units, based on the current projection assumptions.

Because the range includes both negative and positive outcomes, the financial impact remains uncertain.

## 💡 Business Recommendation

### Recommendation: Change and Retest

A full rollout is not recommended based on the current evidence.

The treatment shows a promising improvement on desktop but a negative result on mobile. The overall conversion difference is not statistically significant, and the estimated revenue impact remains uncertain.

## 📚 Key Learnings

- Validating A/B test assignment integrity before measuring outcomes.
- Cleaning experimental data without introducing selection bias.
- Calculating user-level conversion and revenue metrics.
- Applying two-proportion z-tests and interpreting confidence intervals.
- Performing device-level and visitor-level segment analysis.
- Accounting for multiple comparisons.
- Translating statistical results into practical business recommendations.

This project demonstrates the application of Python-based experimentation, statistical analysis, and business decision-making to an e-commerce problem.
