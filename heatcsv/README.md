1. Understand the Data First
Look at the columns — e.g. age, sex, chol, trestbps, cp (chest pain type), target (disease or not).

Check column meanings from the dataset description (so you know which ones are categorical, numerical, etc.).

This helps you know what kind of cleaning each column needs.

2. Remove or Fix Missing Values
Find missing data — empty cells, NaN, or weird placeholders like ? or -1.

Decide what to do:

If there are only a few missing rows → you can drop them.

If many values are missing → replace with:

Mean/median (for numbers)

Most frequent value (for categories)

Or use statistical imputation.

3. Handle Duplicates
Check if any rows are exactly the same → drop duplicates to avoid bias.

4. Correct Data Types
Make sure:

Numbers are stored as numeric types (not text).

Categories are stored as category/text type.

Dates (if any) are in proper date format.

5. Handle Outliers
Find unusual values that don’t make sense (e.g., age = 250, chol = 0).

Either:

Remove them.

Or replace them with more reasonable values.

6. Standardize Categorical Data
Make sure categories are consistent:

Male / male / M → unify to one format.

Map categorical values to numbers if needed (e.g., chest pain types 1, 2, 3, 4).

7. Scale Numerical Values (Optional)
If using ML models that care about scale, normalize or standardize columns like chol, trestbps, etc.

8. Final Check
No missing values.

No duplicates.

All columns have correct types and consistent values. with 303 rows and 14 columns.


Data looks realistic.

TO conclude i can say heart.csv is a dataset about heart health stored in a csv file.
So the exambles its contains patiens and their health. like  paitints age, sex, cholestrol, blood pressure, etc.