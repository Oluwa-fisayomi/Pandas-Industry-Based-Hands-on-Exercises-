Pandas Industry-Based Hands-On Exercises

Overview

This project contains a complete set of industry-based Pandas exercises designed to develop practical data analysis skills.

The exercises focus on the complete data-analysis workflow:

Load → Inspect → Understand → Clean → Transform → Analyze → Interpret

The project uses four different datasets from different industries:

1. E-Commerce / Retail
2. Healthcare
3. Banking / Financial Services
4. Energy / Utilities

Each exercise includes hands-on tasks, data cleaning, analysis, business-rule transformations, challenges, and business interpretations.

---

Objectives

The main objectives of this project are to demonstrate the ability to:

- Load datasets using Pandas
- Inspect datasets and understand their structure
- Identify data-quality problems
- Investigate missing values
- Detect unexpected text in numerical columns
- Clean and transform data appropriately
- Create conditional columns
- Use "value_counts()"
- Use "groupby()"
- Calculate averages and summary statistics
- Interpret analytical results
- Translate Pandas outputs into meaningful business insights
- Explain the reasoning behind data-cleaning decisions

---

Technologies Used

- Python
- Pandas
- Jupyter Notebook / Google Colab

---

Project Structure

Pandas_Industry_Based_Exercises/
│
├── Pandas_Industry_Based_Hands_On_Exercises_Complete.ipynb
│
├── customer_sales.csv
├── hospital_patient_data_cleaning_practice.csv
├── banking_customer_transaction.csv
├── energy_consumption.csv
│
└── README.md

---

Exercise 1 — E-Commerce Customer Analysis

Industry

E-Commerce / Retail

Dataset

"customer_sales.csv"

Objective

The objective of this exercise was to inspect and clean customer transaction data before performing basic customer analysis.

The dataset contains information such as:

- Customer ID
- Customer Name
- City
- Age
- Product Category
- Sales
- Order Status

Tasks Completed

Data Loading

- Imported Pandas
- Loaded the dataset
- Investigated the delimiter
- Corrected the delimiter issue
- Displayed the first five records

Dataset Inspection

The dataset was investigated using:

- "head()"
- "shape"
- "info()"
- "describe()"

Data Cleaning

The dataset was investigated for:

- Missing city values
- Text values where numerical values were expected
- Unnecessary records
- Other data-quality problems

Appropriate cleaning techniques were then applied.

Analysis

The following questions were answered:

1. Number of customers in each city
2. Average sales value
3. Most frequently occurring product category
4. Number of completed orders
5. Number of records containing missing information

Challenge

A new column called "Customer_Value" was created using the following rule:

- Sales >= 100,000 → "High Value"
- Sales < 100,000 → "Standard"

The number of High Value customers was then determined.

---

Exercise 2 — Hospital Patient Data Cleaning

Industry

Healthcare

Dataset

"hospital_patient_data_cleaning_practice.csv"

Objective

The objective was to prepare hospital outpatient records for analysis by identifying and handling data-quality problems.

The dataset contains patient-related information including city and visit information.

Tasks Completed

Initial Inspection

The dataset was inspected using:

- "head()"
- "shape"
- "info()"
- "describe()"

Data-Quality Investigation

The following issues were investigated:

- Missing city values
- Unexpected text values
- Potentially unnecessary records
- Numerical columns requiring cleaning
- Inconsistent data

Cleaning decisions were made after investigating the problems rather than immediately deleting records.

Missing Values

Missing values in the City column were replaced with:

"Unknown"

The result was then verified.

Patient Classification

A "Patient_Category" column was created using:

- Visit count >= 5 → "Frequent Patient"
- Visit count < 5 → "Occasional Patient"

Analysis

The following questions were answered:

1. Number of patients by city
2. Number of frequent patients
3. Average patient visit count
4. Number of records with missing information before cleaning
5. Number of records remaining after cleaning

Challenge

A summary table was created containing:

- Patient Category
- Number of Patients
- Average Visits

The results were then interpreted from the hospital's perspective.

---

Exercise 3 — Banking Customer Transaction Analysis

Industry

Banking / Financial Services

Dataset

"banking_customer_transaction.csv"

Objective

The objective was to clean transaction data and use Pandas to understand customer spending patterns.

The dataset contains information such as:

- Customer ID
- Customer Name
- City
- Transaction Type
- Amount
- Account Status

Tasks Completed

Data Inspection

The dataset was investigated for:

- Dataset size
- Column names
- Data types
- Numerical summary statistics

Transaction Amount Investigation

The transaction amount column was examined for:

- Missing values
- Unexpected text
- Invalid records

Data Cleaning

Problematic values were investigated before cleaning.

Each major cleaning decision was considered in terms of:

«What problem was found, and why was it handled this way?»

Transaction Classification

A "Transaction_Category" column was created using:

- Amount >= 100,000 → "Large Transaction"
- Amount < 100,000 → "Regular Transaction"

Business Analysis

The following questions were answered:

1. Number of transactions in each city
2. Average transaction amount
3. Number of large transactions
4. Most frequently occurring transaction type
5. Average transaction amount by transaction type

Challenge

"groupby()" was used to calculate the average transaction amount by city.

The city with the highest average transaction amount was identified and the result was interpreted from a business-analysis perspective.

---

Exercise 4 — Energy Consumption Analysis

Industry

Energy / Utilities

Dataset

"energy_consumption.csv"

Objective

The objective was to clean and analyze electricity consumption data to identify patterns across different customer groups.

The dataset contains:

- Customer ID
- City
- Customer Type
- Monthly Consumption
- Account Status
- Energy Source

Tasks Completed

Data Inspection

The dataset was examined to determine:

- Number of records
- Number of columns
- Data types
- Summary statistics

Data Cleaning

The following issues were investigated:

- Missing city values
- Missing consumption values
- Unexpected text values
- Unnecessary rows

Appropriate cleaning techniques were then applied.

Consumption Classification

A "Consumption_Category" column was created using:

- Consumption >= 500 → "High Consumption"
- Consumption < 500 → "Normal Consumption"

Consumption Analysis

The following questions were answered:

1. Number of customers in each city
2. Average consumption
3. Number of high-consumption customers
4. Average consumption by customer type
5. Number of customers using each energy source

Challenge

A summary table was created containing:

- Customer Type
- Average Consumption
- Number of Customers

The results were interpreted and a recommendation was provided concerning what the energy company should investigate next.

The recommendation is treated as an area for further investigation rather than a final business decision, as required by the exercise.

---

Data Cleaning Approach

A major focus of this project was understanding that data should not simply be deleted whenever an unusual value appears.

The cleaning process involved:

1. Inspecting the dataset
2. Identifying the problem
3. Determining whether the value could reasonably be corrected
4. Applying an appropriate cleaning technique
5. Verifying the result
6. Considering how the cleaning decision affects the analysis

Examples of issues investigated across the datasets included:

- Missing values
- Unexpected text in numerical columns
- Inconsistent values
- Unnecessary/test records
- Duplicate records
- Incorrectly formatted numerical values

Where a numerical value could reasonably be recovered from its formatting, it was cleaned. Values that could not be reliably recovered were handled appropriately rather than being silently treated as valid data.

---

Pandas Concepts Demonstrated

This project demonstrates practical use of:

import pandas as pd

Dataset Inspection

df.head()
df.shape
df.info()
df.describe()

Missing Values

df.isnull().sum()
df.fillna()

Frequency Analysis

df["Column"].value_counts()

Grouped Analysis

df.groupby("Column")

Conditional Classification

Business rules were used to create new columns based on numerical values.

---

Business Analysis Mindset

The project goes beyond simply producing Python outputs.

For each exercise, the analysis considers:

- What does the result mean?
- Why was the data cleaned in this way?
- What pattern can be observed?
- What could the result mean for the organization?
- Is the result an observation or an assumption?
- What should potentially be investigated next?

This approach helps transform raw Pandas outputs into information that can be understood by a business stakeholder.

---

Final Coach Timothy Checkpoint

The completed project addresses the skills listed in the final checkpoint.

Pandas Knowledge

- [x] Load a dataset
- [x] Identify a delimiter problem
- [x] Inspect a DataFrame
- [x] Understand "shape", "info()", and "describe()"
- [x] Identify data-quality problems
- [x] Use "fillna()"
- [x] Remove unnecessary records
- [x] Create conditional columns
- [x] Use "value_counts()"
- [x] Use "groupby()"

Analyst Mindset

- [x] Explain why data was cleaned
- [x] Explain what numerical results mean
- [x] Distinguish observations from assumptions
- [x] Translate Pandas outputs into business questions
- [x] Create a notebook that another person can understand

---

How to Run the Project

Option 1 — Google Colab

1. Open Google Colab.
2. Upload the ".ipynb" notebook.
3. Upload the four CSV files into the same working environment.
4. Open the notebook.
5. Run the cells from top to bottom.

Option 2 — Jupyter Notebook

Install Pandas if necessary:

pip install pandas

Then open the notebook:

jupyter notebook

Make sure the CSV files are located where the notebook expects them.

---

Project Files

File| Description
"Pandas_Industry_Based_Hands_On_Exercises_Complete.ipynb"| Complete executed notebook containing all exercises and challenges
"customer_sales.csv"| E-Commerce customer sales dataset
"hospital_patient_data_cleaning_practice.csv"| Hospital patient dataset
"banking_customer_transaction.csv"| Banking transaction dataset
"energy_consumption.csv"| Energy consumption dataset
"README.md"| Project documentation

---

Conclusion

This project demonstrates the use of Pandas to work with real-world-style datasets across multiple industries.

The exercises cover the full basic analytical workflow, from loading and inspecting raw data to cleaning, transforming, analyzing, and interpreting the results.

The main lesson from the project is that data analysis is not only about writing code and displaying numbers. It is also about understanding the data, making justified cleaning decisions, and communicating what the results mean.

---

Author

Oluwafisayomi

Pandas Industry-Based Hands-On Exercises
