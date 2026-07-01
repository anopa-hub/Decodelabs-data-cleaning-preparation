# Data Cleaning Project 01 -- Decodelabs Internship

![Python](https://img.shields.io/badge/Python-Data%20Cleaning-blue)
![Pandas](https://img.shields.io/badge/Pandas-Analysis-green)
![NumPy](https://img.shields.io/badge/NumPy-Data%20Processing-blueviolet)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-orange)
![DecodeLabs](https://img.shields.io/badge/Internship-DecodeLabs-red)


## Project Overview
This project focuses on cleaning and preparing a raw business dataset for further analysis and reporting.

The objective was to identify and handle data quality issues such as:
- Missing Values
- Duplicate records
- Data type inconsistencies
- Outliers
- Invalid data entries

The final cleaned dataset is ready for Exploratory Data Analysis (EDA), visualization, and business intelligence applications.

---

# Project Objectives

- Understand dataset structure
- Perform data quality assessment
- Identify missing values
- Detect duplicate records
- Validate data types
- Analyze outliers
- Create a cleaned dataset
- Prepare data for further analytics

---

# Tools and Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Jupyter Notebook
- GitHub

---

# Project Structure

```text
decodelabs-data-cleaning-preparation/
|
|--- dataset/

|    |--- Raw_dataset.xlsx
|    |--- CleanedData.xlsx
|
|--- notebook/

|    |--- data_cleaning.ipynb
|
|--- report/

|    |--- Data_Cleaning_and_preparation_Report.pdf
|    |--- Project_Excel_Report.pptx
|
|--- README.md
```

---

# Data Cleaning Process

## 1. Dataset Loading

- Imported dataset using Pandas
- Checked rows and columns
- Examined overall dataset structure

---

## 2. Data Inspection

Performed:

```python
df.info()
df.shape
df.describe()
```

Purpose:

- Understand column types
- Verify dataset dimensions
- Generate statistical summary

---

## 3. Missing Value Analysis

Used:

```python
df.isnull().sum()
```

Findings:

- Missing values detected in selected columns
- Appropriate treatment applied based on data type

Actions:
- Numerical columns -> Median Imputation
- Categorical columns (`CouponCode`) -> Replaced blank fields with `'None'` identifier

![Missing Values](screenshots/missing_values_after_cleaning.png)
---

## 4. Duplicate Record Check

Used:

```python
df.duplicated().sum()
```

Purpose:

- Identify repeated records
- Prevent biased analysis

Result:

- Duplicate records were checked and handled appropriately.

![Duplicates](screenshots/duplicates_check.png)
---

## 5. Data Type Validation

Verified all column data types using:

```python
df.dtypes
```

Purpose:

- Ensure numerical fields remain numeric
- Ensure date fields remain datetime format
- Maintain data consistency

---

## 6. Outlier Analysis

Outliers were analyzed using boxplots.

Example:

```python
plt.boxplot(df["Quantity"])
```

Variables analyzed:

- Quantity
- Unit Price

Observation:

- No significant outliers were observed, indicating that the values fall within a reasonable business range and do not require treatment.

![Outliers](screenshots/quality_outliers.png)
---

## 7. Final Validation

Performed final quality checks:

```python
df.isnull().sum()
df.duplicated().sum()
df.info()
```

Result:

✔️ Missing values handled

✔️ Duplicate records checked

✔️ Data Types validated

✔️ Dataset prepared for analysis.

---

# Key Findings

- Dataset structure was successfully validated.
- Missing values were identified and treated.
- Duplicate records were checked and resolved.
- Data types were verified and standardized.
- Outlier analysis was performed using visualization techniques.
- Final dataset was prepared for further analytical tasks.

---

# Deliverables

All final clean files, tracking scripts, and presentation summaries can be accessed through these direct links:
* 📊 **Cleaned Output Matrix:** [CleanedData.xlsx](./dataset/CleanedData.xlsx)
* 📓 **Jupyter Engineering Script:** [data_cleaning.ipynb](./notebook/data_cleaning.ipynb)
* 📄 **Analytical Project Report:** [Data_Cleaning_and_preparation_Report.pdf](./report/Data_Cleaning_and_preparation_Report.pdf)
* 📉 **Executive Slide Presentation:** [Project_Excel_Report.pptx](./report/Project_Excel_Report.pptx)

---
# Business Impact

The data cleaning process improved dataset quality and reliability by:

- Eliminating duplicate records
- Handling missing values systematically
- Validating data consistency
- Improving readiness for analytics workflows
- Supporting accurate business decision-making

A clean dataset reduces analytical errors and improves the quality of future reporting, dashboarding, and machine learning projects.

---
# Outcome

The dataset was successfully cleaned and validated.

The final cleaned dataset is suitable for:

- Exploratory Data Analysis (EDA)
- Data Visualization
- Dashboard Development
- Business Intelligence Reporting
- Machine Learning Preparation.

---

# AUTHOR

**Anopa Yokeswaran**  
Data Analyst Intern - Decodelabs Internship Program  
GitHub Profile: [anopa-hub](https://github.com)  
Project Repository: [decodelabs-data-cleaning-preparation](https://github.com/Decodelabs-data-cleaning-preparation)

