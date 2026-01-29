# Final Project: Data-Driven Insights on Elderly Mental Health & Social Isolation

## 1. Project Overview
This project explores the relationship between **social isolation** and **mental health outcomes** among the elderly population (aged 65+) in the United States. Using the **NHANES (National Health and Nutrition Examination Survey)** dataset, the analysis applies various statistical methods to determine how living arrangements influence depressive symptoms.

## 2. Dataset
The analysis utilizes the following NHANES components, merged via the common identifier **`SEQN`**:
* **Demographics:** To identify age (65+) and living arrangements (Household Size).
* **Questionnaire (PHQ-9):** To assess depressive symptoms across 9 standardized categories.
* **Examination & Labs:** To explore physical health markers such as BMI and Glucose levels.

---

## 3. Methodology
To meet the project requirements, the following statistical techniques are applied:

### I. Exploratory Data Analysis (EDA)
* **Descriptive Statistics:** Summarizing mean, median, and SD for BMI, Glucose, and PHQ-9 scores.
* **Data Cleaning:** Handling "Zero-inflation" (30% of participants reported a PHQ-9 score of 0).
* **Visualizations:** Using histograms for distributions and boxplots for outlier detection.

### II. Hypothesis Testing
* **Null Hypothesis ($H_0$):** There is no significant difference in average PHQ-9 scores between elderly individuals living alone and those living with others.
* **Test Method:** Independent Samples t-test and Mann-Whitney U test (due to non-normal distribution).

### III. Correlation Analyses (Required 5 Types)
1.  **Pearson:** Age vs. PHQ-9 Total Score.
2.  **Spearman:** Household Size (Ordinal) vs. PHQ-9 Score.
3.  **Point-Biserial:** Isolation Status (Binary) vs. Fruit Consumption (Continuous).
4.  **Phi Coefficient:** Isolation Status (Binary) vs. Presence of Symptoms (Binary).
5.  **Kendall’s Tau:** Household Size vs. Metabolic markers (e.g., Glucose).

---

## 4. Preliminary Results & Discussion

### Binary Analysis (Isolation vs. Presence of Symptoms)
A preliminary cross-tabulation was conducted to compare the presence of depressive symptoms (PHQ-9 score $\ge$ 1) between those living alone and those living with others.

**Key Findings (Row Percentages):**
* **Living with others:** 64.1% reported at least one symptom.
* **Living alone:** 63.2% reported at least one symptom.
* **Phi Coefficient:** **0.0084**



### Interpretation
The initial **Phi Coefficient of 0.0084** indicates a **negligible correlation** between simply living alone and the *presence* of depressive symptoms. These findings suggest that for the elderly population, **physical living arrangements alone may not be a primary driver of mental health status**. Factors such as social support quality, economic status, or physical health may play a more significant role than the binary "living alone" status.

---

## 5. Next Steps
To further investigate these findings, the project will move to:
1.  **Point-Biserial Correlation:** Analyzing the severity of symptoms (continuous PHQ-9 score) rather than just presence/absence.
2.  **Clinical Cut-off Analysis:** Re-evaluating the data using a PHQ-9 score of $\ge$ 10 (Moderate Depression) as the threshold.
3.  **Stratification:** Examining the data by Gender and Income to identify high-risk subgroups.
