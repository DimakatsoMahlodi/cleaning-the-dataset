### 1. Understand the Data
Check what each column means (age, sex, school, failures, absences, grades like G1, G2, G3).

Know which are categorical (e.g., sex, school) and which are numerical (e.g., age, absences, grades).

### 2. Find and Fix Missing Values
Look for missing data (NaN, blanks, or unusual placeholders).

If missing values are few, remove those rows.

If many missing, fill them with:

The average or median for numbers (e.g., age, absences).

The most common category for categorical fields (e.g., sex, school).

### 3. Remove Duplicate Rows
Check for any exact duplicate student records and remove them.

### 4. Correct Data Types
Make sure numbers are stored as numbers.

Categories like sex or address are stored as categories or strings.

Grades (G1, G2, G3) should be numeric.

### 5. Handle Outliers and Inconsistent Values
Check for impossible ages (like 5 or 100).

Check if any numeric values are unrealistic (e.g., negative absences).

Fix or remove those rows.

### 6. Clean Categorical Data
Make sure categories are consistent, e.g.:

M vs Male → pick one style.

U for urban and R for rural, make sure they’re consistent.

Convert categorical labels into numbers if you want to use ML models.

### 7. Normalize or Scale Numerical Columns (Optional)
For features like study time, absences, or grades, scale or normalize if needed.

And this dataset have 649 rows and 33 columns

### 8. Final Checks
No missing values.

No duplicates.

All columns have proper types.

Values are realistic and consistent.

Cleaning student-por.csv is basically about making sure the data is complete, consistent, and ready for analysis or modeling.


