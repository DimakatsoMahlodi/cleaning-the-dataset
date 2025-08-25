# Data cleaning

## Data Cleaning Report
### Abstract

This report presents the data cleaning process conducted on three datasets: Forest Fires, Heart Disease, and Student Performance. The aim was to enhance the reliability, consistency, and accuracy of data for further analysis and machine learning tasks. Each dataset exhibited unique challenges, including missing values, outliers, inconsistent formatting, and duplicate entries. A systematic cleaning process was applied, including detection and treatment of missing data, removal of duplicates, correction of categorical inconsistencies, handling of outliers, and normalization of numerical values. The resulting datasets are now more suitable for predictive modeling and statistical analysis.

### Repository Layout

data/raw/ → Stores the original untouched datasets (forestfires.csv, heart.csv, student-por.csv).

notebooks/ → Includes Jupyter notebooks (.ipynb) showing the entire workflow of data cleaning, with explanations and code.

reports/ → Contains dataset-specific cleaning reports (Introduction, Methods & Materials + Results, Discussion, Conclusion).

README.md → High-level overview of the project (datasets used, cleaning objectives, repo layout, and usage instructions).

this repository has 3 main directories  each containing its own notebook, README, and raw data


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

Heart Disease: Imputed missing numerical values with mean/median; categorical variables filled with mode.

Student Performance: Missing demographic details were imputed logically (e.g., gender, school support).

### 3. Duplicate Removal

Forest Fires: Detected and removed duplicate records of fire incidents.

Heart Disease: Verified patient entries; duplicate records were eliminated.

Student Performance: Duplicates based on student IDs and demographic attributes were dropped.

### 4. Outlier Detection and Treatment

Forest Fires: Detected extreme values in FFMC, ISI, and area; applied log transformation on skewed area.

Heart Disease: Outliers in cholesterol and blood pressure were capped using IQR-based filtering.

Student Performance: Extreme study time and alcohol consumption values were capped to reduce bias.

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



### Discussion: 

Data cleaning is one of the most important and time-consuming stages in any data science workflow. It transforms raw, messy data into a reliable and consistent format suitable for analysis or modeling. The process is not just about “fixing errors” — it involves making judgment calls, balancing data quality with preserving useful information.

### Why Data Cleaning Matters

Raw data often contains missing values, duplicates, outliers, or inconsistencies that can distort results.

Clean data improves model accuracy, reliability of insights, and reproducibility of research.

In some domains (health, finance, environment), poor cleaning decisions can lead to serious misinterpretations.


## Conclusion

The data cleaning process resulted in three high-quality datasets:

ForestFires.csv: Normalized with numeric encodings and reduced skewness.

Heart.csv: A clean and reliable clinical dataset suitable for predictive modeling.

Student-por.csv: A consistent student performance dataset with uniform formatting.

All three datasets are now free from duplicates, inconsistencies, and outliers, making them well-prepared for exploratory data analysis (EDA) and model development.


