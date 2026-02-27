Introduction
This project performs an Exploratory Data Analysis (EDA) on the famous Titanic passenger dataset using Python. Utilizing the powerful data manipulation capabilities of the Pandas library and the mathematical computing power of NumPy, this script extracts, cleans, and analyzes passenger information to uncover fundamental patterns regarding passenger demographics and ticket fares.

2. Titanic Dataset Overview
The Titanic dataset is one of the most widely used datasets in data science and machine learning. It contains real historical information about the passengers who were aboard the RMS Titanic during its tragic maiden voyage. The dataset includes a mix of numerical data (like age and ticket fare) and categorical data (like passenger class and port of embarkation), making it an ideal resource for practicing data cleaning, manipulation, and statistical analysis.

3. Methodology
The analysis follows a structured, step-by-step approach directly implemented in the Python script:

Data Loading & Inspection: The data is imported from a CSV file into a Pandas DataFrame. Initial checks are performed using df.info() and df.head() to understand the data types and view the top rows.

Data Cleaning (Imputation): Missing values are addressed to ensure accurate analysis:

Missing Age values are filled with the average (mean) age of all passengers.

Missing Embarked (port) values are filled with the most frequent port (mode).

Any rows entirely missing Fare data are dropped.

Data Slicing & Reshaping: * Specific subsets of data are extracted using both label-based (.loc) and index-based (.iloc) selection.

The Sex column is renamed to Gender for better readability.

A pivot table is generated to analyze the average fare paid, categorized by both passenger class and gender.

Filtering: The dataset is filtered to isolate specific groups, such as passengers over the age of 30, and sorted from the highest fare to the lowest.

4. Statistical Analysis
The final section of the project leverages the NumPy library to perform a deep-dive statistical analysis specifically on the Fare column. By converting the Pandas Series into a NumPy array, the script calculates the following metrics:

Top 3 Fares: Identifies the three most expensive tickets purchased.

Total Revenue: Calculates the sum of all fares paid by the passengers in the dataset.

Average (Mean) Fare: Determines the typical ticket price.

Median Fare: Finds the exact middle value of all ticket prices, which provides a better understanding of a "typical" fare without being skewed by a few massive outliers.

Standard Deviation: Measures how spread out the ticket prices are from the average, indicating the massive gap between 3rd-class tickets and luxury 1st-class suites.

5. Titanic Dataset (Data Dictionary)
To understand the output of the script, here is what the key columns in the dataset represent:

Survived: Survival status (0 = No, 1 = Yes)

Pclass: Ticket class, acting as a proxy for socio-economic status (1 = 1st/Upper, 2 = 2nd/Middle, 3 = 3rd/Lower)

Name: Full name of the passenger

Sex / Gender: Male or Female

Age: Age of the passenger in years

Fare: The passenger fare (ticket price)

Embarked: Port of Embarkation (C = Cherbourg, Q = Queenstown, S = Southampton)
