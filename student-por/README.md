.

# Data Cleaning Report: Student-por.csv
### 1. Introduction

The Student Performance dataset (Portuguese language course – student-por.csv) contains demographic, social, and academic information on students, aimed at analyzing factors influencing academic success. Raw educational datasets often include missing values, duplicates, inconsistent categorical data, and outliers. To ensure meaningful analysis and reliable modeling, data cleaning was performed.

### 2. Methods & Materials 

#### Dataset: student-por.csv

Tools Used: Python (Pandas, NumPy, Matplotlib/Seaborn
Loading & Inspection – Imported dataset and examined column types. Categorical attributes included school, sex, address, while numeric features included age and grades.

Handling Missing Values – Checked for null values. Missing categorical entries were imputed with the mode, while missing numeric values were filled with the median.

Removing Duplicates – Removed duplicate rows to ensure each student was represented only once.

Data Type Corrections – Converted categorical attributes (e.g., school, sex, guardian) into numerical codes for analysis.

Outlier Detection & Treatment – Identified outliers in numerical features such as absences and final grades; unrealistic values were capped.

Standardization/Normalization – Normalized continuous variables (e.g., absences, G1, G2, G3) for comparability across features.

Feature Consistency – Standardized column names and corrected categorical entries (e.g., consistent spelling for guardian roles).

### Results

Missing Values: All missing entries were imputed, leaving 0 null values.

Duplicates: Removed, ensuring unique student records.

Outliers: Adjusted to reduce skewness and prevent distortion in analysis.

Final Dataset: Clean, normalized, and consistent, ready for exploratory data analysis (EDA) and modeling.

Final Shape: (rows × columns) after cleaning

### 3. Discussion

Data cleaning revealed common issues in educational datasets: missing demographic details, repeated student records, and extreme outliers in attendance/grades. By imputing missing data and removing duplicates, we preserved dataset integrity without reducing sample size excessively. Encoding categorical variables made the dataset suitable for machine learning tasks.

However, limitations remain: imputed demographic data may not perfectly reflect reality, and normalization may mask meaningful differences in extreme absenteeism cases. Additional preprocessing, such as feature engineering (e.g., risk groups for attendance or study time) and balancing grade distributions, may enhance future modeling.

### 4. Conclusion


The student-por.csv dataset was systematically cleaned to improve consistency and reliability. Missing values were imputed, duplicates removed, categorical variables encoded, and outliers treated. The final dataset is now ready for robust statistical analysis and predictive modeling in the context of student academic performance.

