# Insurance_claims_case_study
## Project Overview

This case study aims to create a comprehensive 360-degree analysis of insurance claim data to derive key insights and identify patterns within claims, customer demographics, and incidents. This project involves data auditing, data cleaning, feature engineering, exploratory data analysis (EDA), and statistical testing. 

---

## Table of Contents
1. [Data Overview](#data-overview)
2. [Data Preparation](#data-preparation)
3. [Analysis Steps](#analysis-steps)
4. [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
5. [Statistical Analysis and Hypothesis Testing](#statistical-analysis-and-hypothesis-testing)
6. [Conclusion and Insights](#conclusion-and-insights)
7. [Setup](#setup)

---

## Data Overview

We are provided with two datasets:
- `claims_data.csv`: Contains detailed claim information such as claim amount, claim date, incident cause, and more.
- `cust_data.csv`: Contains customer details, including demographics like age, gender, and location.

### Goal
To analyze and interpret the data through various analytical steps to answer key business questions about claims trends, customer behavior, and fraud patterns.

---

## Data Preparation

### Step 1: Import and Combine Datasets
- Load both `claims_data.csv` and `cust_data.csv`.
- Merge the datasets on a common key to obtain a unified view.

### Step 2: Data Type Audit
- Check and correct any mismatches between data types and their expected business significance.
  
### Step 3: Data Cleaning
- Convert `claim_amount` to a numeric format by removing the `$` sign.
- Create an alert flag (`1,0`) for injury claims that are unreported to police.
- Remove duplicate customer records, keeping only the most recent observation.

### Step 4: Missing Values
- Impute missing values with mean (for continuous variables) or mode (for categorical variables).

---

## Analysis Steps

### Step 5: Feature Engineering
1. **Customer Age Calculation**: Calculate customer age and categorize them as follows:
   - **Children**: `< 18`
   - **Youth**: `18-30`
   - **Adult**: `30-60`
   - **Senior**: `> 60`
   
2. **Segments Analysis**: Calculate average claim amounts per segment.

3. **Claim Timeline**: Analyze claim amounts based on incidents reported 20+ days before October 1, 2018.

4. **Location and Incident**: Identify adult claims for driver-related issues in TX, DE, and AK.

### Step 6: Visualization
1. **Pie Chart**: Show claim amounts by gender and segment.
2. **Bar Chart**: Compare driver-related claims by gender.
3. **Fraud Analysis**: Visualize age groups with the highest fraudulent claims.
4. **Trend Analysis**: Show monthly total claim amounts over time.
5. **Facetted Bar Chart**: Display average claim amounts by gender and age categories for fraudulent vs. non-fraudulent claims.

---

## Statistical Analysis and Hypothesis Testing

To determine significant insights, we conducted the following tests:
1. **Gender and Claim Amount**: Is there similarity in claim amounts between genders?
2. **Age Category vs. Segment**: Is there a relationship between age category and segment?
3. **Claim Amount Increase**: Has the current year's claim amount significantly increased from the 2016-17 average of $10,000?
4. **Age Group vs. Claim Amount**: Is there a difference in claim amounts across age groups?
5. **Policy Claims vs. Claimed Amount**: Is there a relationship between the number of policy claims and claimed amount?

### Hypothesis Testing Steps:
- Define Null and Alternative Hypotheses.
- Calculate test statistics and p-values.
- Draw conclusions based on p-value significance.

---

## Conclusion and Insights

Summarize the main findings, business implications, and actionable insights derived from the analysis.


