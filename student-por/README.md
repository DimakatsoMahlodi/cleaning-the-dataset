
# Data Cleaning Report: Student-por.csv

### 1. Introduction

The Student Performance dataset (Portuguese language course – student-por.csv) contains demographic, social, and academic information about students, aimed at analyzing factors influencing academic success. Raw educational datasets often include missing values, duplicates, inconsistent categorical data, and outliers. To ensure meaningful analysis and reliable modeling, systematic data inspection and cleaning were performed.

### 2. Methods & Materials

#### Dataset: student-por.csv
Tools Used: Python (Pandas, NumPy, Matplotlib, Seaborn)

Data Cleaning Steps:

Loading & Inspection – Imported dataset, checked shape, column names, and data types.

Missing Values Check – No missing values were detected across any column.

Duplicate Check – No duplicate rows were found.

Data Type Corrections – Categorical variables (school, sex, guardian, etc.) were verified and prepared for encoding.

Outlier Inspection – Histograms of absences and grades (G1, G2, G3) revealed some extreme values. No formal outlier capping or removal was performed in this version of the cleaning process.

Feature Consistency – Column names were standardized and categorical entries checked for consistency.

### 3. Results

Missing Values: None detected → dataset contains 0 null values.

Duplicates: None detected → dataset contains 0 duplicate rows.

Outliers: Extreme values noted in absences (up to 75 days). These were retained for analysis, though they may be considered for treatment in future preprocessing.

Final Dataset Shape: 649 rows × 33 columns (unchanged).

Results Summary Table
Step	Result
Missing values	0 detected
Duplicates	0 detected
Outliers	Extreme values noted, no capping done
Final dataset shape	649 rows × 33 columns

### 4. Discussion

The dataset required minimal cleaning. No missing values or duplicates were detected, confirming high initial quality. Outlier inspection revealed some extreme absenteeism cases and unusually high grade entries, but no adjustments were made in this version to preserve original data integrity.

While the dataset is analysis-ready, limitations remain. Retained extreme values may distort statistical summaries and modeling outcomes. In future iterations, preprocessing such as outlier capping, feature engineering (e.g., attendance groups), or class balancing could enhance the robustness and generalizability of predictive models.

### 5. Conclusion

The student-por.csv dataset was inspected and found to be clean, consistent, and reliable. No missing values or duplicates required treatment, and categorical features were validated for consistency. Although extreme values remain in the absences variable, the dataset is suitable for exploratory data analysis (EDA) and predictive modeling in the context of student academic performance.




