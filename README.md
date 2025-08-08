# cleaning the dataset 
data cleaning  is the process of fixing or removing  incorrect ,corruped , duplicate or incomplete data within a dataset .
clean data is critical for accurate analysis model training and decision making .
## table of content 
.[Project overview](#project-overview)

.[Loading the dataset](#loading-the-dataset)

.[Inspecting the dataset](#inspecting-the-dataset)

.[Handling missing values](#handling-missing-values)

.[Removing duplicates](#removing-duplicates)

.[Fixing data types](#fixing-data-types)

.[Renaming or dropping columns](#renaming-or-dropping-columns)

.[Standardizing text entries](#standardizing-text-entries)
## Project overview
1.i used Google Colab because is an ideal tool for data cleaning .

2.It runs Python code directly in your browser.

3.It has no setup everything is pre-installed.

4.It allows importing data from your computer or Google Drive.

5.It supports key libraries like pandas, which is essential for data manipulation.
so we are cleaning the three data which is are: 

-.student-por[1].csv

-.heart.csv

-.forestfires[1].csv
### Loading the dataset
>Before cleaning you must load the dataset into your workspace

>A dataset is usually stored in .csv, .xlsx or other formats.

>pandas is a Python library that reads these files into a DataFrame, which is a table-like structure.

>In Colab, data can come from your local machine or from Google Drive
>import pandas as pd

# Load a CSV file
df = pd.read_csv("data.csv")

# Show the first few rows
print(df.head())

### Inspecting the dataset
Before cleaning, you need to understand what’s wrong with the data.

1.Looking at the first few rows to get a sense of the content.

2.Checking the shape (how many rows and columns).

3.Looking for missing values, incorrect types, or weird entries.

4.Checking for duplicate rows.

5.Understanding the structure of the data is key before modifying it.
### Handling Missing Values
>Missing data is a common issue. The theory behind handling it depends on the reason it’s missing.

>Remove missing values: If only a few rows are missing data, deleting them is usually safe.

>Impute (fill in) missing values

>For numerical columns: use the mean, median, or mode.

>For categorical columns: use a placeholder like "Unknown" or the most common category.

 >Models and algorithms usually cannot process null values and will give errors or bad results.
### Removing Duplicates
Duplicate data can happen due to repeated entries during data collection or merging.

Why do remove  them?

They distort analysis, cause bias, and waste resources.

Removing duplicates ensures that each data point is counted only once

###  Fixing Data Types
Sometimes columns are:

Recognized as text when they’re actually numbers or dates.

Recognized as numbers when they’re IDs and shouldn’t be used for math.

Why do we fix data types?

Correct data types ensure that operations (like math, filtering, or grouping) behave correctly.

For example, you can’t calculate the mean of a column unless it’s recognized as numeric.
### Standardizing Text Entries
Sometimes the same value appears in different forms (e.g., "yes", "Yes", "YES").

You need to:

Convert text to lowercase.

Strip extra spaces.

Replace inconsistent spellings.

because the

Consistent text is easier to filter, group, and analyze.
### Conclusion
Data cleaning is like tidying up before you cook a meal.
If your ingredients (data) are messy, your recipe (analysis/model) will fail.
In Google Colab, tools like pandas make this process efficient, and the cloud-based platform means you can collaborate and run code from anywhere.


