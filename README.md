# COVID-19 Data Cleaning Guide
# 1. Handling Missing Values
🔹 Identify missing values using df.isnull().sum()

🔹 Drop irrelevant columns or rows with excessive missing data

🔹 Fill missing values using appropriate methods:

    Forward/Backward fill: df.fillna(method='ffill')
    Mean/Median for numerical data: df['column'].fillna(df['column'].median())
    Mode for categorical data: df['column'].fillna(df['column'].mode()[0])
# 2. Standardizing Date Format
🔹 Convert date columns to a standard format using:
# 3. Handling Duplicates
🔹 Check for duplicates: df.duplicated().sum()

🔹 Remove duplicates if necessary: df.drop_duplicates(inplace=True)
# 4. Correcting Data Types
🔹 Convert numerical values stored as strings:

🔹 Standardize categorical variables (e.g., country names).
# 5. Fixing Inconsistent Data Entries

🔹 Ensure uniform spelling of country/state names (e.g., "USA" vs. "United States")

🔹 Check for incorrect values (e.g., negative case counts)
# 6. Filtering Outliers

🔹 Use box plots or df.describe() to detect outliers

🔹 Decide whether to cap extreme values or remove them
# 7. Ensuring Data Integrity

🔹 Verify total case counts align with subcategories (e.g., sum of states = national total)
🔹 Check for logical inconsistencies (e.g., deaths > confirmed cases)

This process ensures clean, reliable, and accurate COVID-19 data for analysis and visualization. 🚀
