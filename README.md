# Real-Estate-Data-Analysis-Using-Excel


# Terro’s Real Estate Agency - House Pricing Analysis


## Problem Statement

**“Finding out the most relevant features for pricing of a house”**

Terro’s real-estate is an agency that estimates the pricing of houses in a certain locality. The pricing is concluded based on different features / factors of a property. This also helps them in identifying the business value of a property. To do this activity the company employs an “Auditor”, who studies various geographic features of a property like pollution level(NOX), crime rate, education facilities (pupil to teacher ratio), connectivity (distance from highway), etc. This helps in determining the price of a property. 


## Project Objective

The main objective is to determine the most influential factors for pricing a house through EDA and linear regression technique. 

### Goals:
1. Identify the most influential factors for house pricing.
2. Predict property value, based on various factors of a house using built regression model.


## Dataset Overview

The dataset contains information on 506 houses located in Boston, with the following features:

| Feature          | Description                                                               |
|------------------|---------------------------------------------------------------------------|
| `CRIME_RATE`     | Per capita crime rate by town                                             |
| `INDUSTRY`       | Proportion of non-retail business acres per town (percentage)             |
| `NOX`            | Nitric oxides concentration (parts per 10 million)                        |
| `AVG_ROOM`       | Average number of rooms per house                                         |
| `AGE`            | Proportion of houses built before 1940 (percentage)                       |
| `DISTANCE`       | Distance from highways (in miles)                                         |
| `TAX`            | Full-value property-tax rate per $10,000                                  |
| `PTRATIO`        | Pupil-teacher ratio by town                                               |
| `LSTAT`          | Percentage of the lower status population                                 |
| `AVG_PRICE`      | Average house value (in $1000s)                                           |



## Project Workflow

### 1. Data Understanding
- Review the dataset to understand its structure and features.
- Ensure essential features for analysis are present.

### 2. Data Preprocessing
- Convert raw data into a clean, organised, structured format suitable for analysis.

### 3. Data Cleaning
- Identify and remove errors, duplicates, inconsistencies, and missing values.

### 4. Exploratory Data Analysis (EDA)
- Generated descriptive statistics to understand the characteristics of each features in the dataset.
- Plotted histogram to understand the data distribution of dependent variable (AVG_Price).
- Generated covariance matrix to identify direction of the relationship between variables.
- Generated correlation matrix to identify direction and strength of the relationship between variables.

### 5. Regression Modeling
Four regression models were developed:

#### Model 1:
- **Simple Linear Regression**
- Independent Variable: `LSTAT`
- Dependent Variable: `AVG_PRICE`

#### Model 2:
- **Multiple Linear Regression**
- Independent Variables: `LSTAT`, `AVG_ROOM`
- Dependent Variable: `AVG_PRICE`

#### Model 3:
- **Multiple Linear Regression**
- Independent Variables: `CRIME_RATE`,`INDUSTRY`,`NOX`,`AVG_ROOM`, `AGE`,`DISTANCE`,`TAX`,`PTRATIO`, `LSTAT`                                        
- Dependent Variable: `AVG_PRICE`

#### Model 4:
- **Optimized Multiple Linear Regression**
- Uses only statistically significant variables.
- Independent Variables: `INDUSTRY`,`NOX`,`AVG_ROOM`, `AGE`,`DISTANCE`,`TAX`,`PTRATIO`, `LSTAT`                                        
- Dependent Variable: `AVG_PRICE`

### 6. Model Evaluation
The regression models were evaluated using:
1. **Model Fit**
2. **Prediction Accuracy**
   - Metrics: RMSE, MAPE
3. **Assumption Checks**
   - Residual mean should be zero.
   - Residuals should be normally distributed.
   - Residuals should have constant variance.

## Key Insights

1. **Average Price**: The average price of houses in Boston is **$22,533**.
2. **Correlation Analysis**:
   - `LSTAT` is the most influential factor for house pricing, followed by `AVG_ROOM`, `PTRATIO`, `INDUSTRY`, `TAX`, `NOX`, `DISTANCE`, `AGE`, and `CRIME_RATE`.
   - `CRIME_RATE` has the least influence on house pricing.
   - **`LSTAT`**: House prices decrease as the lower-status population percentage increases.
   - **`AVG_ROOM`**: House prices increase as the average number of rooms increases.
4. **Regression Analysis**:
   - `NOX` is the most influential predictor in the regression model, followed by `AVG_ROOM`, `PTRATIO`, `LSTAT`, `DISTANCE`, `INDUSTRY`, `AGE`, and `TAX`.
   - `CRIME_RATE` remains the least influential factor.
   - **`NOX`**: House prices decrease as the NOX factor increase.
   - **`AVG_ROOM`**: House prices increase as the avarage number of rooms increases.
   - **`PTRATIO`**: House prices decrease as the PTRATIO increase.
   - **`LSTAT`** : House prices decrease as the lower-status population percentage increases.
5. **Model Performance**:
   - Regression model accuracy: **69%**.
   - On average, the model prediction is **$5,086** off from the actual house price.
   - On average, the model prediction is **18%** off from the actual house price.


## Tools Used
- **Microsoft Excel** with Data Analysis Toolpak enabled.
