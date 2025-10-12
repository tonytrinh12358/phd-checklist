# Statistical Rigor Reference Guide
## How to Report Results Properly in Research Papers

---

## 🎯 **WHEN TO USE THIS GUIDE**

### **Critical Moments:**
- ✅ **Designing experiments** - Plan which tests you'll use BEFORE running experiments
- ✅ **Writing results section** - Look up how to report mean, std, p-value, effect size
- ✅ **Creating tables** - Check proper format for statistical reporting
- ✅ **Responding to reviewers** - When they question statistical validity
- ✅ **Before claiming "significant improvement"** - Verify you have the evidence

### **How to Use:**
1. **Section 1**: Choose the right test for your data type
2. **Section 2**: Calculate effect size (not just p-value!)
3. **Section 3**: Apply corrections if testing multiple hypotheses
4. **Section 4**: Use reporting templates for writing

### **Quick Example:**
```
❌ Wrong: "Our method is better (85.2 vs 83.1)"

✅ Correct: "Our method significantly outperforms baseline
(85.2±0.3 vs 83.1±0.4, p<0.001, d=0.87, n=10 runs)"
```

---

## 📊 CHOOSING THE RIGHT STATISTICAL TEST

### For Comparing Two Methods

| Your Data Type | Distribution | Use This Test | Report These |
|----------------|--------------|---------------|--------------|
| Continuous (accuracy, loss) | Normal | Paired t-test | mean ± std, t-statistic, p-value, Cohen's d |
| Continuous | Non-normal | Wilcoxon signed-rank | median [IQR], W-statistic, p-value, Cliff's delta |
| Binary (success/fail) | - | McNemar's test | proportions, χ², p-value |
| Count data | - | Poisson regression | rate ratio, CI, p-value |

### For Comparing Multiple Methods (>2)

| Your Data Type | Distribution | Use This Test | Post-hoc Test |
|----------------|--------------|---------------|---------------|
| Continuous | Normal | One-way ANOVA | Tukey's HSD |
| Continuous | Non-normal | Kruskal-Wallis | Dunn's test |
| Repeated measures | Normal | Repeated ANOVA | Bonferroni |
| Repeated measures | Non-normal | Friedman test | Nemenyi test |

---

## 🎯 EFFECT SIZE GUIDELINES

### Why Effect Size Matters
p-value only tells you IF there's a difference, not HOW BIG it is.

### Cohen's d (for normal data)
```
d = (mean1 - mean2) / pooled_std
```
- Small: d = 0.2
- Medium: d = 0.5  
- Large: d = 0.8
- Very large: d > 1.2

### Cliff's Delta (for non-normal data)
```
delta = (sum(x1 > x2) - sum(x2 > x1)) / (n1 * n2)
```
- Small: |δ| < 0.147
- Medium: |δ| < 0.33
- Large: |δ| < 0.474

**Always report**: "Our method shows large improvement (d=1.3, p<0.001)"

---

## ✅ REPORTING CHECKLIST

### Basic Requirements
- [ ] **Mean/Median**: Report central tendency
- [ ] **Spread**: Standard deviation or IQR  
- [ ] **Sample size**: How many runs/examples
- [ ] **Significance**: p-value with correction
- [ ] **Effect size**: Cohen's d or Cliff's delta

### How to Write It

❌ **Wrong**: "Our method is better (85.2 vs 83.1)"

✅ **Correct**: "Our method significantly outperforms the baseline (85.2±0.3 vs 83.1±0.4, p<0.001, d=0.87, n=10 runs)"

### Table Format Example
```
Method      | Accuracy        | p-value | Effect Size
------------|-----------------|---------|-------------
Baseline    | 83.1 ± 0.4     | -       | -
Ours        | 85.2 ± 0.3     | <0.001  | d=0.87
Ours (full) | 86.7 ± 0.2     | <0.001  | d=1.23
```

---

## 🔄 MULTIPLE TESTING CORRECTIONS

### When You Need Correction
- Comparing on multiple datasets
- Testing multiple hypotheses
- Multiple pairwise comparisons

### Bonferroni Correction (Conservative)
```
adjusted_α = α / number_of_tests
```
Example: 10 tests, α=0.05 → use α=0.005

### Holm-Bonferroni (Less Conservative)
1. Sort p-values: p₁ ≤ p₂ ≤ ... ≤ pₘ
2. Find largest k where: pₖ ≤ α/(m-k+1)
3. Reject H₁, ..., Hₖ

### False Discovery Rate (Benjamini-Hochberg)
Best for many comparisons:
1. Sort p-values  
2. Find largest k where: pₖ ≤ (k/m) × α
3. Reject H₁, ..., Hₖ

**Report as**: "p-values corrected using Bonferroni/Holm/FDR"

---

## 📈 CONFIDENCE INTERVALS

### For Means (Normal Distribution)
```
CI = mean ± t_(α/2,df) × (std/√n)
```

### For Proportions
```
CI = p ± z_(α/2) × √(p(1-p)/n)
```

### For Differences
```
CI_diff = (mean1-mean2) ± t_(α/2) × SE_diff
```

**Report as**: "Improvement: 2.1% [95% CI: 1.8-2.4%]"

---

## 🎲 RANDOM SEEDS & REPRODUCIBILITY

### Minimum Standards
- **Seeds**: Report at least 3-5 different random seeds
- **Report**: Mean and standard deviation across seeds
- **Code**: Fix and report the exact seeds used

### How to Report
"Results averaged over 5 runs with seeds {42, 123, 456, 789, 2024}"

### What Requires Multiple Seeds
- Neural network training
- Random data splits
- Stochastic algorithms
- Bootstrap sampling

---

## 📝 WRITING TEMPLATES

### In Abstract
"Our method achieves 85.2% accuracy, significantly outperforming baselines (p<0.001)"

### In Results
"Table 2 shows our method significantly improves over all baselines (p<0.05, Bonferroni corrected). The improvement is substantial with large effect sizes (d>0.8) across all metrics."

### In Tables
- Always include ± for uncertainty
- Bold best results
- Use † for statistical significance
- Include sample sizes

### Statistical Significance Notation
- `*` p < 0.05
- `**` p < 0.01  
- `***` p < 0.001
- `†` Not significant

---

## ⚠️ COMMON MISTAKES TO AVOID

### 1. Wrong Test Choice
❌ Using t-test on non-normal data
✅ Check normality first (Shapiro-Wilk test)

### 2. Missing Corrections
❌ Multiple comparisons without correction
✅ Always correct when testing >1 hypothesis

### 3. P-hacking
❌ Testing until p<0.05
✅ Decide tests before seeing results

### 4. Ignoring Effect Size
❌ "Significant improvement (p=0.049)"
✅ "Small but significant improvement (p=0.049, d=0.21)"

### 5. Wrong Percentage Calculation
❌ Improvement = (new-old)/new × 100
✅ Improvement = (new-old)/old × 100

---

## 🐍 Python Code Templates

### Basic Statistical Test
```python
from scipy import stats
import numpy as np

# Normality test
_, p_normal = stats.shapiro(data)

if p_normal > 0.05:
    # Use t-test
    t_stat, p_value = stats.ttest_rel(method1, method2)
    # Calculate Cohen's d
    d = np.mean(method1 - method2) / np.std(method1 - method2)
else:
    # Use Wilcoxon
    w_stat, p_value = stats.wilcoxon(method1, method2)
    # Calculate Cliff's delta
    # ... (use cliffs_delta library)
```

### Multiple Testing Correction
```python
from statsmodels.stats.multitest import multipletests

# Bonferroni correction
rejected, p_adjusted, _, _ = multipletests(
    p_values, method='bonferroni'
)
```

### Confidence Intervals
```python
import scipy.stats as st

# 95% CI for mean
ci = st.t.interval(
    0.95, len(data)-1,
    loc=np.mean(data),
    scale=st.sem(data)
)
```

---

## 📚 REFERENCES FOR STATISTICAL TESTS

1. **General Guide**: Demšar (2006) - "Statistical comparisons of classifiers"
2. **Effect Sizes**: Lakens (2013) - "Calculating and reporting effect sizes"
3. **Multiple Testing**: Benjamini & Hochberg (1995) - "Controlling false discovery rate"
4. **ML-Specific**: Dietterich (1998) - "Statistical tests for comparing algorithms"

---

*Remember: Statistical rigor adds credibility. When in doubt, be conservative.*
