Task 1: Data Cleaning & Preprocessing
📝 Project Overview

This project focuses on cleaning and preprocessing the Customer Personality Analysis dataset from Kaggle.
The goal is to prepare the raw dataset for further analysis or modeling by handling missing values, fixing inconsistent formats, standardizing text, converting data types, and ensuring data quality.

This task is part of a structured learning program designed to help build strong data cleaning skills using Python (Pandas).

📂 Dataset Used

Dataset Name: Customer Personality Analysis
Source: Kaggle
File: marketing_campaign.csv (tab-separated values)

✔ Raw Dataset Location
data/raw/customer_personality_raw.csv

✔ Cleaned Dataset Location
data/cleaned/customer_personality_cleaned.csv

🛠 Tools & Technologies

Python 3

Pandas Library

Jupyter Notebook / VS Code (any environment)

GitHub for version control

🚀 Steps Performed in Data Cleaning
1️⃣ Loaded the raw dataset

Used Pandas with proper separator (sep="\t") because the file is tab-separated.

2️⃣ Standardized column names

Converted to lowercase

Removed spaces

Added underscores
Example: Year_Birth → year_birth

3️⃣ Removed duplicate rows

Ensures clean, unbiased data.

4️⃣ Handled missing values

Only the income column had missing values (24 missing)

Filled missing income values using the median

5️⃣ Standardized text columns

Converted string columns to:

lowercase

trimmed spaces

Columns standardized:

education

marital_status

6️⃣ Fixed inconsistent marital status values

Mapped unusual categories like:

absurd, yolo → single
(if present in dataset version)

7️⃣ Converted date column

Converted:

dt_customer → datetime format


Also created:

dt_customer_dd_mm_yyyy


for consistent date display.

8️⃣ Corrected data types

Ensured numeric columns are integers/floats:

income → int

numeric columns checked and fixed

9️⃣ Detected outliers

Flagged outliers in income using:

IQR (Interquartile Range) method
Created new column:

income_outlier (True/False)

🔟 Saved the cleaned dataset

Stored as:

data/cleaned/customer_personality_cleaned.csv

📁 Repository Structure
task1-data-cleaning/
│
├── data/
│   ├── raw/
│   │   └── customer_personality_raw.csv
│   └── cleaned/
│       └── customer_personality_cleaned.csv
│
├── scripts/
│   └── data_cleaning.py
│
├── README.md
└── summary.md

📜 Files Included

data/raw/ → Original dataset

data/cleaned/ → Cleaned dataset

scripts/data_cleaning.py → Full cleaning code

README.md → Documentation (this file)

▶️ How to Run the Script

Install Pandas:

pip install pandas


Run the script:

python scripts/data_cleaning.py


Cleaned file will appear in:

data/cleaned/


✅ Task Successfully Completed ✔

