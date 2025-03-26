# Healthcare Solutions Inc. Drug Efficacy Analysis Report

## Table of Contents  
- [Project Name](#project-name)  
- [Project Background](#project-background)  
- [Project Goals](#project-goals)  
- [Data Structure & Initial Checks](#data-structure--initial-checks)  
- [Executive Summary](#executive-summary)  
- [Insights Deep Dive](#insights-deep-dive)  
  - [Drug Efficacy](#category-1-drug-efficacy)  
  - [Dosage Impact](#category-2-dosage-impact)  
- [Recommendations](#recommendations)  
- [Technical Details](#technical-details)  
- [Assumptions and Caveats](#assumptions-and-caveats)  


## Project Name  
**Healthcare Solutions Inc. Drug Efficacy Analysis**  
This analysis evaluates the efficacy of two drugs (Drug A vs. Drug B) and three dosage levels (50mg, 100mg, 150mg) to determine optimal treatment protocols.

---

## Project Background  
Healthcare Solutions Inc. specializes in optimizing therapeutic regimens using data-driven approaches. In 2023, the company collected recovery time data from 20 patients to compare Drug A (mean: 6.25 days) and Drug B (mean: 7.55 days), alongside dosage responses. The goal is to identify statistically significant differences to improve patient outcomes.

---

## Project Goals  
1. **Compare Drug A vs. Drug B**: Determine if one drug significantly reduces recovery time.  
2. **Dosage Optimization**: Identify the most effective dosage (50mg, 100mg, or 150mg).  
3. **Statistical Validation**: Use paired t-tests and ANOVA to ensure robust conclusions.  

---

## Data Structure & Initial Checks  
The dataset includes **20 patients** with the following variables:  
- **Patient_ID**: Unique identifier (1–20).  
- **Drug_A_Time**: Recovery time for Drug A (mean: 6.25, std: 1.07).  
- **Drug_B_Time**: Recovery time for Drug B (mean: 7.55, std: 1.10).  
- **Dosage_50mg**, **Dosage_100mg**, **Dosage_150mg**: Recovery times for each dosage (mean: 6.5, 6.25, 5.25 days).  

**Key Checks**:  
- No missing values.  
- Small sample size (n=20) limits generalizability.  

---

## Executive Summary  
**Key Findings**:  
1. **Drug A Outperforms Drug B**: Drug A showed significantly shorter recovery times (p=0.001).  
2. **Dosage Efficacy**: 150mg dosage had the shortest recovery time (5.25 days) and was statistically superior to 50mg (p=0.001) and 100mg (p=0.016).  
3. **No 50mg vs. 100mg Difference**: These dosages showed similar efficacy (p=0.439).  



---

## Insights Deep Dive  

### Category 1: Drug Efficacy  
- **Insight 1**: Drug A reduced recovery time by 1.3 days compared to Drug B (t=-3.58, p=0.001).  
- **Insight 2**: Drug B exhibited higher variability (std=1.10), suggesting inconsistent responses.  

### Category 2: Dosage Impact  
- **Insight 1**: 150mg reduced recovery time by 1.25 days vs. 50mg (p=0.001) and 1.0 day vs. 100mg (p=0.016).  
- **Insight 2**: 100mg showed no advantage over 50mg (p=0.439).  



---

## Recommendations  
1. **Adopt Drug A**: Prioritize Drug A due to its statistically significant efficacy advantage.  
2. **Standardize 150mg Dosage**: Implement 150mg as the default dosage for optimal recovery times.  
3. **Expand Study**: Conduct a larger trial to validate results and reduce variability.  

---

## Technical Details  
**Tools Used**:  
- **Python**: pandas for data manipulation, pingouin/scipy for statistical tests.  
- **Jupyter Notebook**: Reproducible analysis workflow.  

**Key Tests**:  
- Paired t-test (Drug A vs. Drug B).  
- One-way ANOVA (dosage comparison).  
- Bonferroni-corrected pairwise tests.  

---

## Assumptions and Caveats  
1. **Normality Assumption**: Tests assume normality, which was not formally verified.  
2. **Small Sample Size**: Results may not generalize to broader populations.  
3. **Design Limitations**: Dosage data structure (independent vs. repeated measures) was not explicitly confirmed.  
