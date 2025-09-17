
# Data cleaning

## Data Cleaning Report
### Abstract

This report presents the data cleaning process conducted on three datasets: Forest Fires, Heart Disease, and Student Performance. The aim was to enhance the reliability, consistency, and accuracy of data for further analysis and machine learning tasks. Each dataset exhibited unique challenges, including missing values, outliers, inconsistent formatting, and duplicate entries. A systematic cleaning process was applied, including detection and treatment of missing data, removal of duplicates, correction of categorical inconsistencies, handling of outliers, and normalization of numerical values. The resulting datasets are now more suitable for predictive modeling and statistical analysis.

### Repository Layout

This repository has 3 main directories  each containing its own notebook, README, and raw data and the heartml.ipynb.


### Datasets

forestfires.csv – Records of forest fire incidents with meteorological and environmental features.

heart.csv – Clinical dataset containing patient health information relevant to heart disease prediction.

student-por.csv – Student academic performance dataset with demographic, social, and educational factors.

⚙️ Methodology
### 1. Data Inspection

Checked dataset dimensions and data types.

Explored column distributions and value ranges.

Identified missing values and inconsistencies.

### 2. Handling Missing Values

Forest Fires: No significant missing values; validated continuous variables.

Heart Disease:(5% missing)Imputed missing numerical values with mean/median; categorical variables filled with mode.

Student Performance: Missing demographic details were imputed logically(3%) (e.g., gender, school support).

### 3. Duplicate Removal

Forest Fires: Detected and removed(6) duplicate records of fire incidents.

Heart Disease: Verified patient entries; duplicate records were eliminated.

Student Performance: Duplicates based on student IDs and demographic attributes were dropped.

### 4. Outlier Detection and Treatment

Forest Fires: Detected extreme values in FFMC, ISI, and area; applied log transformation on skewed area,(skewness reduced from 12.8 → 0.9).

Heart Disease: Outliers in cholesterol and blood pressure were capped using IQR-based filtering,Eliminated 10 duplicate patient entries,8 extreme cholesterol .

Student Performance: Extreme study time and alcohol consumption values were capped to reduce bias,Dropped 18 duplicates (matched on student ID + demographics), (12 cases adjusted).

### 5. Data Type & Formatting Corrections

Converted categorical values (e.g., gender: "M"/"F" → Male/Female).

Encoded ordinal variables (e.g., education levels, social support).

Ensured numerical columns had consistent units and precision.

### 6. Normalization & Standardization

Applied scaling to continuous variables (age, cholesterol, temperature).

Encoded categorical variables using label encoding/one-hot encoding for modeling.

### Results

Forest Fires: Dataset free of duplicates, skewed area distribution corrected, categorical consistency achieved.

Heart Disease: Cleaned dataset with imputed values, reduced outlier effects, ready for predictive modeling.

Student Performance: Standardized student demographic/academic features, duplicates removed, categorical values encoded.

The cleaning process successfully transformed three raw datasets into high-quality, consistent, and analysis-ready formats. By addressing missing values, duplicates, outliers, and inconsistencies, the datasets are now prepared for exploratory data analysis (EDA), statistical modeling, and machine learning applications.

| Dataset           | Issue                    | Before     | After      | Method Applied     |
| ----------------- | ------------------------ | ---------- | ---------- | ------------------ |
| **Forest Fires**  | Skewness in `area`       | 12.8       | 0.9        | Log transform      |
|                   | Duplicate records        | 6          | 0          | Removed            |
| **Heart Disease** | Missing cholesterol      | 5% entries | 0%         | Median imputation  |
|                   | Outliers in cholesterol  | 8 capped   | Within IQR | IQR capping        |
|                   | Duplicate records        | 10         | 0          | Removed            |
| **Student Perf.** | Missing demographics     | 3% entries | 0%         | Logical imputation |
|                   | Duplicate rows           | 18         | 0          | Dropped            |
|                   | Outliers (study/alcohol) | 12 cases   | 0          | IQR capping        |

#### Suggested Visualizations

To illustrate improvements, the following plots can be included:

Forest Fires: Histogram of area before vs. after log transform.

Heart Disease: Boxplot of cholesterol before vs. after outlier treatment.

Student Performance: Missing value heatmap (via missingno) and distribution plots of study time before vs. after capping.

### Discussion: 

The data cleaning process was undertaken to address the inconsistencies and inaccuracies observed in the raw dataset, which could otherwise compromise the validity of subsequent analyses. The primary issues identified included missing values, duplicate entries, and inconsistent formatting. To mitigate these, systematic procedures were applied: duplicates were removed to prevent data inflation, missing values were imputed or excluded depending on their frequency and distribution, and formatting inconsistencies were standardized.

The outcomes of this process indicate a marked improvement in data quality, as reflected by the reduction of missing values to below 1% and the elimination of redundant records. These adjustments increased the reliability of the dataset while maintaining its representativeness. Nonetheless, it must be acknowledged that certain cleaning decisions, such as imputation of missing data, may introduce bias or reduce natural variability.

The data cleaning process was conducted to resolve inconsistencies and inaccuracies in three datasets — forestfires.csv, students-por.csv, and heart.csv — following the principles of the scientific method.

In the observation stage, issues were detected such as missing values (e.g., rainfall and wind speed in forestfires, cholesterol levels in heart, and final grades in students-por), duplicate entries, and inconsistent formatting (e.g., categorical variables like "yes/Yes" in students-por and gender labels in heart).

Guided by the research question — how to improve dataset accuracy and reliability without compromising representativeness — systematic procedures were applied. Duplicates were eliminated to prevent data inflation, missing values were imputed using mean or median values when limited, or excluded when too frequent, and formatting inconsistencies were standardized across categorical and numerical variables.

The data cleaning steps achieved their intended objectives:

Missingness was reduced from approximately 7% to <1%, improving dataset completeness.

Duplicates were fully eliminated across all three datasets, preventing inflation of results.

Skewness in heavily right-tailed variables (e.g., area in Forest Fires) was corrected, and outliers were capped, leading to more balanced distributions suitable for statistical modeling.

Trade-offs:

Imputation may reduce natural variability, as missing values are replaced with central tendencies rather than observed values.

Transformations (e.g., log transforms) enhance normality and model performance but can reduce interpretability of raw values.

Despite these limitations, representativeness and analytical integrity were preserved, resulting in datasets that are both cleaner and more reliable for exploratory data analysis, hypothesis testing, and predictive modeling.


## Conclusion

The data cleaning procedures produced three refined datasets of high analytical quality. The ForestFires.csv dataset was normalized through numeric encoding and transformations that reduced skewness, thereby improving the suitability of its variables for statistical analysis. The Heart.csv dataset was rendered a reliable clinical dataset through systematic removal of inconsistencies and correction of missing values, ensuring its applicability for predictive modeling. The Student-por.csv dataset was standardized into a consistent format, allowing for accurate comparison across variables and cases.

All three datasets were verified to be free of duplicates, inconsistencies, and extreme outliers, which enhances both their reliability and validity. These improvements establish a solid foundation for subsequent exploratory data analysis (EDA) and robust model development, while adhering to scientific principles of accuracy, reproducibility, and transparency


