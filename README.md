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
All our data originates from the U.S. 2000 census. Since the entire census dataset contains too much information, we hand picked 10 variables to regress against the death rate. The detailed description of each variable is presented below:
![](data%20description.jpg)

The additional data point we introduce is called "Crazytown". There are two goals for introducing this additional datapoint.
1) Can our model validation process identify this new datapoint?
2) Does this new datapoint change our feature selection?

All values of Crazytown are column averages except for death_rate. where the county average is about 10, and we chose Crazytown's death_rate to be 25. All values for Crazytown are shown below:

| | Country average | Crazytown |
| --- | --- | --- |
| death_rate | 10.16246 | 25.00000 |
| population | 99779.15 | 100000.00	|
| num_care_facilities | 11.77083 | 12.00000 |
| per_below_poverty | 14.85669 | 14.86000 |
| per_high_grad | 56.14779 | 56.14779 |
| per_bacherlor_grad | 13.78063 | 13.78000 |
| num_violent_crimes | 501.274 | 501.000 |
| num_property_crimes | 3516.331  | 3516.000	|
| unemploy_rate | 4.731813 | 4.730000 |
| per_cap_income_as_per_national_average | 78.73543 | 78.00000 |
| num_social_security_ben_per_1000_resid | 193.2333 | 193.0000 |



