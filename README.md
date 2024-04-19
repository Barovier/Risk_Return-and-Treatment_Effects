# Product Sales and Stock Analysis

## Overview

This repository contains code and instructions for analyzing both product sales data and stock data using R. The analysis aims to provide insights into sales performance, risk assessment, and stock market relationships.

### Product Sales Analysis

The product sales analysis focuses on understanding the impact of a software update on the sales volume of Company ABC's products, TechPad and ElectroTab. It includes data classification, mean calculation, estimation of Difference-in-Differences (DiD), and linear regression analysis.

### Stock Analysis

The stock analysis involves examining the performance, risk, and relationship of selected stocks (AAPL, GM, TSLA, and XOM) with the market (GSPC). It covers monthly returns, risk assessment, average return, cumulative return, and beta analysis.

## Dataset

### Product Sales Dataset

The product sales dataset "product_sales.csv" contains monthly sales data for TechPad and ElectroTab, along with an indicator for pre- and post-update periods.

- **month**: Month of the sale
- **product**: Name of the product (TechPad or ElectroTab)
- **sales_volume**: Number of units sold in that month
- **post_update**: Indicates whether the data was collected before (0) or after (1) the software update

### Stock Datasets

Multiple CSV files are provided for each stock (AAPL, GM, TSLA, XOM) and the market index (GSPC), containing historical stock data.

## Questions and Solutions

### Product Sales Analysis

- **Group Classification**: Classify sales data into four groups based on the product and update status.
- **Mean Calculation in R**: Calculate the mean sales volume for each group using R.
- **Estimation of Difference-in-Differences**: Estimate the DiD using mean values.
- **Estimation of DiD Using Linear Regression**: Perform a linear regression analysis to estimate the DiD.

### Stock Analysis

The stock analysis covers various aspects including:

- **Monthly Returns**: Calculate simple monthly returns for selected stocks.
- **Risk Assessment**: Determine the riskiest and least risky stocks based on standard deviation of returns.
- **Average Return**: Compute the average monthly return for each stock.
- **TSLA Performance**: Compare TSLA's performance with the market.
- **Cumulative Return**: Calculate the cumulative return for each stock.
- **Beta Analysis**: Perform beta analysis to determine riskiness compared to the market.

## Conclusion

Both analyses provide valuable insights into product sales performance and stock market dynamics. The findings can be used for decision-making and strategic planning purposes.

---

**README**

**Analysis of mtcars Dataset**

This README provides an overview of the analysis performed on the `mtcars` dataset in R. The analysis focuses on understanding the relationship between a vehicle's fuel efficiency (measured in miles per gallon, mpg) and the number of cylinders it has. The analysis is divided into two main parts: 

**A. Linear Regression Analysis**
- The first part involves creating two separate datasets: one comparing cars with 4 cylinders to those with 6 cylinders (dataset1), and the other comparing cars with 4 cylinders to those with 8 cylinders (dataset2).
- Linear regression models are applied to each dataset to compute the difference estimator for the impact of cylinder number on fuel efficiency.
- The results of the regression analysis are provided, including coefficients, standard errors, t-values, p-values, and other relevant statistics.

**B. Comparison of Average MPG**
- The second part computes the average miles per gallon for cars with 4, 6, and 8 cylinders, respectively.
- The average MPG values are compared across the different cylinder groups, and commentary is provided on which group exhibits the lowest average fuel efficiency.

**Code Organization:**

- **Linear Regression Analysis (Part A):**
  - The R code begins by loading the necessary libraries (`dplyr` and `datasets`) and the `mtcars` dataset.
  - The `cyl` variable in the `mtcars` dataset is converted to a factor.
  - Two separate datasets (`dataset_small_cyl` and `dataset_large_cyl`) are created to compare cars with 4 cylinders to those with 6 cylinders and 8 cylinders, respectively.
  - Linear regression models (`lm`) are fitted to each dataset (`model_small_cyl` and `model_large_cyl`).
  - The summary of each regression model is printed, displaying coefficients, standard errors, t-values, p-values, and other statistics.

- **Comparison of Average MPG (Part B):**
  - The average MPG values for cars with 4, 6, and 8 cylinders are computed using the `mean()` function.
  - Results are printed, displaying the average MPG for each cylinder group.

**Results:**

- **Part A: Linear Regression Analysis**
  - For cars with 6 cylinders, the regression model yields a significant negative effect on MPG with a coefficient of -6.921 (p-value: 0.00129).
  - For cars with 8 cylinders, the regression model shows a substantial negative impact on MPG with a coefficient of -11.564 (p-value: 3.45e-08).
  - Both models demonstrate high statistical significance, with adjusted R-squared values of 0.4547 and 0.7293 for the 6-cylinder and 8-cylinder datasets, respectively.

- **Part B: Comparison of Average MPG**
  - The group with 4 cylinders has the highest average MPG (26.66).
  - The group with 6 cylinders has a lower average MPG (19.74) compared to the 4-cylinder group.
  - The group with 8 cylinders has the lowest average MPG (15.1) among the three groups.

**Conclusion:**

- In terms of fuel efficiency, cars with 4 cylinders tend to have the highest average miles per gallon, while cars with 8 cylinders have the lowest.
- The analysis provides valuable insights into the relationship between cylinder number and fuel efficiency in the `mtcars` dataset.
