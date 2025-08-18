

# Student Performance Dataset (`student_por.csv`)

## Description
The `student_por.csv` dataset contains information about students’ performance in Portuguese language classes, including demographic, social, and academic features. It is commonly used for data analysis and machine learning tasks related to student outcomes.

## Dataset Features
- **Demographic data:** age, gender, family background
- **Academic performance:** grades, study time, failures
- **Social factors:** extracurricular activities, internet access, family support

## Data Cleaning Process
The dataset was cleaned to ensure accuracy, consistency, and usability for analysis. The following steps were performed:

1. **Data Inspection**
   - Reviewed all columns for missing values, inconsistencies, and duplicates.
   - Verified that numeric and categorical values had correct data types.

2. **Handling Missing Values**
   - Filled missing numeric values using the mean or median.
   - Filled missing categorical values using the mode or a placeholder such as "Unknown".

3. **Standardization**
   - Unified categorical values (e.g., consistent lowercase, spelling, and formatting).
   - Ensured numeric values were within expected ranges.

4. **Encoding Categorical Variables**
   - Converted categorical features into numeric form using one-hot encoding or label encoding for machine learning compatibility.

5. **Removing Duplicates**
   - Identified and removed duplicate rows to prevent data redundancy.

6. **Final Verification**
   - Reviewed the cleaned dataset to ensure all corrections were applied.
   - Saved the cleaned dataset as `student_por_cleaned.csv` for analysis.

## Outcome
The cleaned dataset is accurate, consistent, and ready for statistical analysis or machine learning modeling. Cleaning ensures that the dataset produces reliable and meaningful insights.

Cleaning student-por.csv is basically about making sure the data is complete, consistent, and ready for analysis or modeling.

### : Conclusion 

The cleaning process of the student-por.csv dataset ensured that the data is consistent, accurate, and ready for analysis. Missing values and duplicate records were checked and handled appropriately. Categorical attributes (such as school, sex, address, famsize, studytime, etc.) were encoded into numerical formats, while numerical features (such as age, absences, G1, G2, and G3) were validated to remove invalid or extreme values. Data types were corrected, and inconsistent entries were standardized.

