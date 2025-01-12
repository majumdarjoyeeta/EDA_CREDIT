# EDA_CREDIT
Here's a `README.md` file for your EDA Credit App project. This file provides an overview of the project, its objectives, data dictionary, and a brief description of the analysis performed.

```markdown
# EDA Credit App

![Credit Amount EDA Case Study](loan-2.png)

## Introduction
This project involves analyzing loan applications data for approximately 307,000 applications. The primary goal is to perform risk analytics using data wrangling and visualization libraries in Python. The end goal is to derive important insights for the bank to identify the characteristics of bad loan applications (i.e., loans that are delayed or not paid).

## Objectives
- Identify common characteristics of bad loan applications.
- Discover patterns related to applicants with loan difficulties.
- Determine the driving factors or strong indicators of a bad loan application.

## Data Dictionary
Understanding the data is a crucial first step in any Exploratory Data Analysis (EDA). A data dictionary has been provided along with the dataset, which outlines the meaning of each column. It is advised to review this document before starting the EDA.

### Screenshot of Data Dictionary
![Data Dictionary](image.png)

The dictionary can also be imported into a Jupyter notebook for reference.

## EDA - Credit Applications
The flow of the entire case study is as follows:

1. **Data Wrangling**
   - Data loading
   - Data shape
   - Data types
   - 5-point summary (describe)
   - Data preprocessing
     - Missing values
     - Outlier check
     - Correlation check
     - Feature engineering
     - Normalization, encoding (only required at ML model stage)

2. **Univariate Analysis**

3. **Bivariate/Multivariate Analysis**

4. **Final Insights**

## Importing Libraries
```python
import warnings
warnings.filterwarnings('ignore')

# Importing core libraries
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

%matplotlib inline   

pd.set_option('display.float_format', lambda x: '%.3f' % x)

# Changing default figure size using rcParams
plt.rcParams["figure.figsize"] = (10, 5)
plt.style.use('ggplot')
```

## Data Wrangling
### Loading the Data
```python
credit_data = pd.read_csv("application_data.csv")
credit_data.head(20)
```
- The data is at the Loan ID level (SK_ID_CURR).
- It contains a mix of quantitative and qualitative variables.
- There are several flags and considerable missing values.

### Inspecting Data
- Shape of the data: 307,511 loan applications and 122 fields for each application.
- 5-point summary to understand the range, mean, and median for each variable.

### Data Cleaning
- Columns with more than 45% missing values are removed.
- Missing values are imputed where necessary (e.g., using mode or median).

### Feature Engineering
- Continuous variables are binned into categories for better analysis.

## Univariate Analysis
Univariate analysis focuses on one variable at a time to find patterns. Various visualizations (e.g., bar plots, pie charts) are used to analyze the distribution of loan applications by different categorical variables such as occupation type, organization type, and income type.

## Bivariate & Multivariate Analysis
Bivariate analysis examines the relationship between two variables, while multivariate analysis involves more than two variables. Various visualizations (e.g., box plots, pair plots) are used to explore these relationships.

## Final Insights
The analysis reveals several driving factors for loan defaults:
- Lower education levels correlate with higher chances of loan default.
- Certain occupations, such as laborers and sales staff, show significant default rates.
- Applicants on maternity leave and unemployed individuals have high default rates.
- Income levels and annuity amounts also play a role in loan default probabilities.

## Conclusion
This EDA provides valuable insights into the characteristics of loan applicants and the factors contributing to loan defaults. The findings can help banks and financial institutions make informed decisions regarding loan approvals and risk management.

## Dataset
The dataset used for this analysis is `application_data.csv`, which contains the total data for the loan applications.
```

### Notes:
- Make sure to replace the image paths (`loan-2.png` and `image.png`) with the correct paths where your images are stored.
- You can add more sections or details as needed based on your project requirements.
- Ensure that the code snippets are properly formatted in your Markdown file for better readability.
