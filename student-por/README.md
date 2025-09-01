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

The data cleaning process revealed several quality issues typical of educational datasets, namely missing demographic attributes, duplicate student records, and extreme outliers in attendance and grade distributions. To address these, missing values were imputed to preserve dataset completeness, duplicates were removed to ensure data integrity, and categorical variables were encoded to enable their integration into machine learning tasks. These steps collectively improved the dataset’s consistency and analytical readiness.

Despite these improvements, limitations remain. Imputed demographic data are based on assumptions that may not accurately represent the true population, and normalization of extreme absenteeism cases risks obscuring meaningful educational patterns. Future preprocessing, such as feature engineering to create risk categories (e.g., attendance groups or study time levels) and balancing skewed grade distributions, is necessary to enhance model robustness and generalizability.

### 4. Conclusion


The student-por.csv dataset was systematically cleaned to improve consistency and reliability. Missing values were imputed, duplicates removed, categorical variables encoded, and outliers treated. The final dataset is now ready for robust statistical analysis and predictive modeling in the context of student academic performance.


