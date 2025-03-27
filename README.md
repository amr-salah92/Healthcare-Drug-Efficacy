# Healthcare Solutions Inc. Drug Efficacy Analysis Report

## Table of Contents  
- [Project Name](#project-name)  
- [Project Background](#project-background)  
- [Project Goals](#project-goals)  
- [Data Structure & Initial Checks](#data-structure--initial-checks)  
- [Executive Summary](#executive-summary)  
- [Insights Deep Dive](#insights-deep-dive)  
  - [Drug Efficacy](#drug-efficacy)  
  - [Dosage Impact](#dosage-impact)  
- [Recommendations](#recommendations)  
- [Technical Details](#technical-details)  
- [Assumptions and Caveats](#assumptions-and-caveats)  

---

## Project Name  
**Healthcare Solutions Inc. Drug Efficacy Analysis**  
This analysis evaluates the efficacy of two drugs (Drug A vs. Drug B) and three dosage levels (50mg, 100mg, 150mg) to determine optimal treatment protocols.

---

## Project Background  
Healthcare Solutions Inc. specializes in data-driven therapeutic optimization. This study examines the effectiveness of Drug A and Drug B by analyzing recovery times and dosage effects on patients.

---

## Project Goals  
1. **Compare Drug A vs. Drug B**: Identify which drug leads to shorter recovery times.  
2. **Dosage Optimization**: Determine the most effective dosage (50mg, 100mg, or 150mg).  
3. **Statistical Validation**: Conduct statistical tests to confirm findings.  

---

## Data Structure & Initial Checks  
The dataset includes the following variables:  
- **Patient_ID**: Unique identifier.  
- **Drug_A_Time**: Recovery time for Drug A.  
- **Drug_B_Time**: Recovery time for Drug B.  
- **Dosage_50mg**, **Dosage_100mg**, **Dosage_150mg**: Recovery times for each dosage level.  

**Key Checks**:  
- No missing values were found.  
- Normality tests (Shapiro-Wilk, Kolmogorov-Smirnov) were performed.  

---

## Executive Summary  
**Key Findings**:  
1. **Drug A vs. Drug B**: Drug A showed significantly shorter recovery times than Drug B (p < 0.05).  
2. **Dosage Impact**: 150mg dosage led to the shortest recovery times.  
3. **Statistical Significance**: Pairwise comparisons with Bonferroni correction confirmed significant differences between dosages.  

---

## Insights Deep Dive  

### Drug Efficacy  
- Drug A significantly reduced recovery time compared to Drug B.  
- Normality tests confirmed the validity of t-tests.  

### Dosage Impact  
- 150mg dosage resulted in the shortest recovery time, significantly outperforming 50mg and 100mg.  
- Bonferroni-corrected pairwise tests confirmed statistical significance.  

---

## Recommendations  
1. **Adopt Drug A**: Given its superior efficacy.  
2. **Use 150mg Dosage**: This dosage led to optimal recovery times.  
3. **Further Research**: Conduct larger trials to validate findings.  

---

## Technical Details  
**Tools Used**:  
- **Python**: pandas for data manipulation, scipy/pingouin for statistical tests.  
- **Jupyter Notebook**: For reproducible analysis.  

**Statistical Tests**:  
- Wilcoxon test for Drug A vs. Drug B.  
- One-way ANOVA for dosage comparison.  
- Bonferroni-corrected pairwise comparisons.  

---

## Assumptions and Caveats  
1. **Normality rejection**: Statistical tests rejects normality, validated by Shapiro-Wilk and KS tests.  
2. **Sample Size Limitations**: Results may not generalize to a larger population.  
3. **Study Design Considerations**: Future research should explore repeated measures for enhanced reliability.  

