# STAT 350 Final Project
Author: Leo Chen & Tianxing Yan
## Abstract 
Our main purpose is to conduct a thorough regression analysis to analyze if there exist a linear relationship between U.S. death rate and a variety of independent variables. A special observation (crazytown) is also added to see if it will have any impact on feature selection and if we can detect it during model validation. At the end of all our analysis, we conclude that:
- Crazytown is identifiable during model validity analysis
- crazytown does impact feature selection, but only for manual stepwise regression
- our final linear regression model satisfies all assumption requirements
- within our variables, the most explanatory for U.S. death rate are unemployment rate, poverty level, per capital income, and number of social security beneficiaries per 1000 residents. 
## Introduction
Death has many contributing factors. In this report, we attempt to analyze U.S. death rate through linear regression analysis using U.S. 2000 census data. We also introduce a special observation (crazytown) into the dataset for special analysis purpose. Throughout this report, we are trying to answer the following five questions:
- is there a linear relationship between the death rate and some of the independent variables? If so, which variables provide the most explanatory power?
- does our linear regression model satisfy all model assumptions?
- is Crazytown identifiable during model validation?
- does crazydown affect feature selection?

The core structure of our analysis is listed below:
1) download and preprocess data, create separate copy and include crazytown
2) feature selection (manual stepwise regression & stepAIC function) for original dataset and new dataset
3) model validation for both models (original and new dataset)
4) cross validation
## Data Description


