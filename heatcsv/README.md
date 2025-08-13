## 1. Understand the Data First which is heart.csv

Look at the columns — e.g. age, sex, chol, trestbps, cp (chest pain type), target (disease or not).

Check column meanings from the dataset description (so you know which ones are categorical, numerical, etc.).

This helps you know what kind of cleaning each column needs.

The heart.csv dataset was cleaned to ensure accuracy, consistency, and readiness for analysis.
 Missing values in numerical columns such as age, trestbps, chol, thalach, and oldpeak were imputed using the median, while categorical columns like sex, cp, fbs, restecg, exang, slope, ca, and thal were filled using the most frequent category. All categorical variables were verified for valid codes and corrected if necessary.
 
### Outliers 
 Outliers in the age, trestbps, chol, thalach, and oldpeak Numerical features were checked for outliers using both the IQR and Z-score methods; extreme but medically plausible values were retained, while erroneous entries were removed. After cleaning, the dataset contains consistent, valid values across all columns and is ready for exploratory analysis and machine learning modeling.

 The dataset is now fully cleaned, consistent, and prepared for reliable analysis or modeling.

### TO conclude i can say heart.csv is a dataset about heart health stored in a csv file.

So the exambles its contains patiens and their health. like  paitints age, sex, cholestrol, blood pressure, that has 303 rows and 14 columns.
