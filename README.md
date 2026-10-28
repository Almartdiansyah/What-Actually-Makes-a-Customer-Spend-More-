# What-Actually-Makes-a-Customer-Spend-More-

**Customer Spending Analysis | Correlation | Multiple Linear Regression**

## Project Overview

This project investigates which customer factors are significantly associated with annual spending and translates statistical findings into actionable campaign recommendations.

The analysis addresses a key business question: **Which customer behavior and profile factors should the business prioritize to increase customer spending?**

## Focus

- **Correlation Analysis:** Examine relationships among six candidate predictors: age, income, tenure, session time, promotional engagement, and bounce rate.
- **Multicollinearity Assessment:** Use Variance Inflation Factor (VIF) to assess overlap among predictors.
- **Multiple Linear Regression:** Identify statistically significant predictors of annual customer spending while controlling for other variables.
- **Driver Prioritization:** Rank predictors using standardized regression coefficients.
- **Business Recommendations:** Translate model findings into prioritized campaign actions.

## Tools

- **Statistical Analysis:** Pearson Correlation, Multiple Linear Regression, Hypothesis Testing
- **Model Diagnostics:** Variance Inflation Factor (VIF), p-values, F-test, Adjusted R²
- **Business Analysis:** OBIPR Framework, Root Cause Analysis, Data-Driven Decision Making

## Key Output

### 1. Final Regression Model

**Sample size:** 299 customers

- Adjusted R²: 0.927
- F-statistic: 760.6
- Overall model significance: p < 0.001
- Final predictors: 5
- All final predictor p-values < 0.05
- All final predictor VIF values < 4

The final model explained approximately 92.7% of the observed variation in annual customer spending, after adjusting for the number of predictors.

### 2. Annual Spending Prediction Formula

```text
Spending = 2,590,241
         + 0.036 × Income
         + 64,576 × Tenure
         + 6,342 × Session Time
         + 136,148 × Promo
         - 49,209 × Bounce Rate
```

*Note: Interpret coefficients according to the original dataset's units and variable coding. Predictions are valid within the model's applicable data range.*

### 3. Ranked Spending Drivers

| Rank | Predictor | Standardized Beta | Interpretation |
|---|---|---:|---|
| 1 | Session Time | 0.42 | Strongest positive association |
| 2 | Promo | 0.29 | Second-strongest positive association |
| 3 | Bounce Rate | -0.22 | Negative association |
| 4 | Tenure | 0.10 | Modest positive association |
| 5 | Income | 0.06 | Weakest positive association |

Age was excluded from the final model because it did not meet the 5% significance threshold in the initial iteration (p = 0.069).

### 4. Business Recommendations

Based on the regression findings, the proposed campaign priorities are:

1. **Reduce Bounce Rate:** Investigate and address friction that causes customers to leave sessions early.
2. **Optimize Promotions:** Test minimum-purchase thresholds instead of relying solely on flat discounts.
3. **Build Customer Loyalty:** Introduce a tiered loyalty program to encourage repeat engagement.
4. **Increase Session Time:** Test relevant content, recommendations, and gamification to encourage meaningful engagement.

## Business Impact

The analysis provides a statistically supported basis for prioritizing campaign experiments rather than allocating budget based on simple correlations alone.

However, regression identifies conditional associations, not causal effects. Each recommendation should be validated through controlled A/B testing before scaling campaign investment.

## Key Takeaway

**Session time was the strongest positive predictor of annual spending, while bounce rate showed a negative association.** Income was statistically significant but had the weakest standardized coefficient among the five retained predictors.

The findings suggest prioritizing customer engagement experiments while validating their actual incremental impact through A/B testing.
