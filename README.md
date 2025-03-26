# Healthcare Solutions Inc. Drug Efficacy Analysis Report

## Table of Contents
- Project Name
- Project Background
- Project Goals
- Data Structure & Initial Checks
- Executive Summary
- Insights Deep Dive
- Recommendations
- Technical Details
- Assumptions and Caveats

---

## Project Name  
**Healthcare Solutions Inc. Drug Efficacy Analysis**  
This analysis evaluates the efficacy of two drugs (Drug A and Drug B) and three dosage levels (50mg, 100mg, 150mg) to determine optimal treatment protocols.

---

## Project Background  
Healthcare Solutions Inc. has operated in the pharmaceutical industry for 12 years, specializing in developing and optimizing therapeutic regimens. The company’s business model focuses on data-driven decisions to improve patient outcomes while minimizing costs. Key metrics include patient recovery time and dosage effectiveness.  

In 2023, the company collected data from 20 patients to compare Drug A (mean recovery time: 6.25 days) and Drug B (mean recovery time: 7.55 days), alongside dosage responses. The dataset includes recovery times for each drug and three dosage levels, aiming to identify statistically significant differences.

---

## Project Goals  
1. **Compare Drug A vs. Drug B**: Determine if one drug significantly reduces recovery time.  
2. **Dosage Optimization**: Identify the most effective dosage (50mg, 100mg, or 150mg) based on recovery time.  
3. **Statistical Validation**: Use t-tests and ANOVA to ensure findings are robust and actionable.  

---

## Data Structure & Initial Checks  
The dataset contains **20 patient records** with the following columns:  
- **Patient_ID**: Unique identifier (1–20).  
- **Drug_A_Time**: Recovery time (days) for Drug A (mean: 6.25, std: 1.07).  
- **Drug_B_Time**: Recovery time (days) for Drug B (mean: 7.55, std: 1.10).  
- **Dosage_50mg**, **Dosage_100mg**, **Dosage_150mg**: Recovery times for each dosage (mean: 6.5, 6.25, 5.25 days respectively).  

**Key Considerations**:  
- No missing values detected.  
- Small sample size (n=20) limits generalizability.  

---

## Executive Summary  
**Key Findings**:  
1. **No Significant Difference Between Drugs**: Drug A and Drug B showed similar efficacy (p-value: 0.9997).  
2. **Dosage Matters**: 150mg dosage significantly outperformed 50mg (p=0.001) and 100mg (p=0.016).  
3. **Optimal Dosage**: 150mg had the shortest mean recovery time (5.25 days).  


---

## Insights Deep Dive  

### Category 1: Drug Efficacy  
- **Insight 1**: Drug A (6.25 days) vs. Drug B (7.55 days) showed no statistically significant difference (t=-3.79, p=0.9997).  
- **Insight 2**: High variability in Drug B’s recovery times (std=1.10) suggests inconsistent patient responses.  

### Category 2: Dosage Impact  
- **Insight 1**: 150mg dosage reduced recovery time by 1.25 days compared to 50mg (p=0.001).  
- **Insight 2**: 100mg and 50mg showed no significant difference (p=0.439).  


---

## Recommendations  
1. **Prioritize 150mg Dosage**: Implement 150mg as the default dosage due to its superior efficacy.  
2. **Re-evaluate Drug B**: Investigate why Drug B underperforms despite higher mean recovery time.  
3. **Expand Sample Size**: Conduct a larger study to validate findings and reduce variability.  

---

## Technical Details  
**Tools Used**:  
- **Python**: For data manipulation (pandas), statistical tests (scipy, pingouin), and visualization (matplotlib).  
- **Jupyter Notebook**: Reproducible analysis workflow.  

---

## Assumptions and Caveats  
1. **Normality Assumption**: t-tests and ANOVA assume normally distributed data, which was not explicitly verified.  
2. **Small Sample Size**: Results may not generalize to broader populations.  
3. **No Covariates**: Patient demographics (age, weight) were not included in the analysis.  
