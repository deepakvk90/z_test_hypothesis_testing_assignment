# Z-Test Hypothesis Testing: Operational Cost Reduction Analysis

## Repository Description

> Statistical analysis using one-sample Z-test to evaluate whether corporate cost-saving measures achieved a target operational cost reduction of more than 8%, based on departmental sample data.

---

## Overview

This project applies **one-sample Z-test hypothesis testing** to assess the effectiveness of cost-saving initiatives implemented across departments of a multinational corporation. The analysis determines whether the average percentage reduction in operational costs significantly exceeds the company's benchmark target of **8%**.

---

## Problem Statement

A multinational corporation implemented a series of cost-saving measures across its departments. A sample dataset (`operational_costs_data.csv`) captures the percentage reduction in operational costs per department post-implementation. The goal is to statistically test whether the average cost reduction achieved is greater than **8%**.

---

## Dataset

**File:** `operational_costs_data.csv`

| Column | Description |
|---|---|
| `department_id` | Unique identifier for each department |
| `cost_reduction_pct` | Percentage reduction in operational costs post-implementation |

- **Sample Size:** 100 departments
- **Population Mean (pre-measures):** 7%
- **Population Standard Deviation:** 3

---

## Methodology

### Hypotheses

| | Statement |
|---|---|
| **H₀ (Null)** | Average operational cost reduction ≤ 8% |
| **Hₐ (Alternative)** | Average operational cost reduction > 8% |

### Test: One-Sample Z-Test (Right-Tailed)

The Z-test was chosen because:
- The population standard deviation is **known**
- The sample size is **large (n = 100)**

### Steps

1. **Data Import** — Load and explore the dataset
2. **Hypothesis Definition** — Formulate null and alternative hypotheses
3. **Test Statistic Calculation** — Compute sample mean, standard error, and Z-score
4. **Critical Value Determination** — Find Z-critical at α = 0.05
5. **Decision Making** — Compare Z-score vs Z-critical and draw conclusions

---

## Results

| Metric | Value |
|---|---|
| Sample Mean | 7.2562% |
| Standard Error | 0.30 |
| Z-Score | 0.85 |
| Z-Critical (α = 0.05) | 1.645 |
| Decision | **Fail to Reject H₀** |

### Conclusion

Since the calculated Z-score (**0.85**) is less than the critical Z-value (**1.645**), there is **insufficient statistical evidence** to conclude that the cost-saving measures reduced operational costs beyond the 8% target at the 5% significance level.

---

## Technologies Used

| Library | Purpose |
|---|---|
| `pandas` | Data loading and manipulation |
| `numpy` | Numerical computations |
| `scipy.stats` | Statistical functions (Z-critical value) |
| `matplotlib` | Data visualization |
| `seaborn` | Enhanced visualizations |

---

## Project Structure

```
├── z_test_hypothesis_testing_assignment.ipynb   # Main analysis notebook
├── operational_costs_data.csv                   # Dataset
└── README.md                                    # Project documentation
```

---

## How to Run

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/your-repo-name.git
   cd your-repo-name
   ```

2. **Install dependencies**
   ```bash
   pip install pandas numpy scipy matplotlib seaborn jupyter
   ```

3. **Launch the notebook**
   ```bash
   jupyter notebook z_test_hypothesis_testing_assignment.ipynb
   ```

---

## Key Concepts

- **Z-Test:** A parametric hypothesis test used when the population standard deviation is known and the sample size is large (n ≥ 30).
- **Standard Error:** Measures the precision of the sample mean estimate — calculated as σ / √n.
- **P-value / Critical Value Approach:** A right-tailed test at α = 0.05 uses a Z-critical of 1.645.
- **Type I Error (α):** The probability of incorrectly rejecting a true null hypothesis, set at 5%.

---

## Author

*Deepak Vishwakarma*
