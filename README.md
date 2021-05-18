# Modeling High School Tennessee Graduation Rates

Can a model accurately predict graduation rates based on demographic information and school financial data? If a model can be created to predict this, at-risk schools 
can be identified and special intervention can take place to raise future graduation rates. Graduation rates in this context means the percentage of students that graduate
on time.

It may also be possible that model schools can be identified.  What is meant by model schools is that even though the predictive model predicted a lower graduation rate 
for a particular school, the school ended up doing far better than anticipated. Other schools can adopt their approach and hopefully achieve similar results.

## Data 

Data was sourced from the Tennessee Department of Education’s website ([LINK](https://www.kaggle.com/andrewmvd/face-mask-detection)). 
Only data from 2018 - 2019 was used. The data used were: Chronic absenteeism, Demographics, Finance, and Graduation rates. These files are in 
Excel format and contain aggregated data. Each row of these files have a School ID and District ID that can be used to identify the school.

## Method

The method I used was to build four models: Multiple Linear Regression, Ridge Regression, Lasso Regression, and Random Forest and choose 
the one that had the smallest mean absolute error. Ridge and Lasso were hyperparameter-tuned using GridSearch. Random Forest was hyperparameter-tuned 
using RandomizedSearchCV, since it has many tunable parameters that could have many different values. The scoring used for tuning was Mean Absolute Error.

## Data Cleaning/Organizing/Preprocessing

Before merging the files, select columns were dropped. After leaving what was necessary, the tables were then merged. After merging, some schools were
dropped if they contained data in the columns that were deemed outliers. Something that would be identified as an outlier would be if a school is all girl/boy
or if a school had a small population size.

## Results

A ridge regression model with a Mean Absolute Error of 2.59%
