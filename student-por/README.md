.

# Data Cleaning Report: Student-por.csv
### 1. Introduction

The Student Performance dataset (Portuguese language course – student-por.csv) contains demographic, social, and academic information on students, aimed at analyzing factors influencing academic success. Raw educational datasets often include missing values, duplicates, inconsistent categorical data, and outliers. To ensure meaningful analysis and reliable modeling, data cleaning was performed.

### 2. Methods, Materials, and Results

### Dataset: student-por.csv
Tools Used: Python (Pandas, NumPy, Matplotlib/Seaborn)

Data Cleaning Process and Outcomes:

Loading & Inspection – The dataset was imported, and column types were examined. Several attributes were categorical (e.g., school, sex, address), while others were numeric (e.g., age, grades).

Handling Missing Values – Null values were checked. Where present (e.g., some demographic or guardian information), missing entries were imputed with the mode (for categorical) or median (for numerical).

Removing Duplicates – Duplicate rows representing repeated student records were identified and removed, ensuring each student appeared only once.

Data Type Corrections – Converted categorical attributes (e.g., school, sex, guardian) into numerical codes to support further statistical analysis.

Outlier Detection & Treatment – Outliers in numerical features such as absences and final grades were identified. Unrealistic values were capped to reduce distortion in analysis.

Standardization/Normalization – Continuous variables such as absences and grades (G1, G2, G3) were normalized to ensure comparability across features.

Feature Consistency – Column names were standardized for readability, and categorical entries were cleaned (e.g., consistent spelling of guardian roles).

Final Dataset Shape: (rows × columns) after cleaning, with duplicates removed, missing values handled, and categorical attributes encoded.

### 3. Discussion

Data cleaning revealed common issues in educational datasets: missing demographic details, repeated student records, and extreme outliers in attendance/grades. By imputing missing data and removing duplicates, we preserved dataset integrity without reducing sample size excessively. Encoding categorical variables made the dataset suitable for machine learning tasks.

However, limitations remain: imputed demographic data may not perfectly reflect reality, and normalization may mask meaningful differences in extreme absenteeism cases. Additional preprocessing, such as feature engineering (e.g., risk groups for attendance or study time) and balancing grade distributions, may enhance future modeling.

### 4. Conclusion


The student-por.csv dataset was systematically cleaned to improve consistency and reliability. Missing values were imputed, duplicates removed, categorical variables encoded, and outliers treated. The final dataset is now ready for robust statistical analysis and predictive modeling in the context of student academic performance.
