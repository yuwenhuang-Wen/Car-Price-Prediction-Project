# Car Price Analysis

### Project Overview

This project aims to predict car prices using various regression models. The dataset consists of features such as make, model, year, mileage, engine size, and more. Key metrics used to evaluate model performance are RMSE and R-Squared.

### Data Source

Car Price Data: The dataset used for this project is the "CarPrice.csv" file, containing several features and price of each cars sales.

### Tools

- Excel -- [Downlaod Link](https://www.kaggle.com/datasets/hellbuoy/car-price-prediction/data?select=CarPrice_Assignment.csv)
- Python

### Data Preparation

- Data laoading and inspection
- Checked missing values
- Exploratory Data Analysis (EDA)
- Encoded categorical data into numeric values, then scaled

### EDA

#### The EDA aims to help determine if all features are included in the modeling, so there are analyses aim to answer the questions of:
- How many columns and rows are there?
- What are the numeric and categorical features in the dataset?
- Are there missing values?
- What are the correlations between price and the numeric features and which to exclude?
- According to the feature improtance analysis, which features(numeric & categorical) are less powerful in predicting price, and which to exclude?

### Overfit Inspection 

- Applied 10-fold cross validation to inspect if models are too fit.


### Findings

1. EDA
   - Correlation Coefficient Value
     - most of the numeric features have absolute value of correlation coefficient above 0.6
     - there are 4 features have correlation absolute value < 0.1

   - Feature Improtance (can handle both numeric & categorical)
     - Results from correlation values and feature importance showed some differences
     - the 2 least important features were excluded in modeling
       
4. Data Observation
   - Including encoded and scaled categorical data significantly improved the predicting results than only modeling by numeric data
   - Excluding the least correlated/ important features usually had worser measuring metrics score in training set, but better ones in testing set
     
5. Models Performance
   - Linear regression models have highest rmse scores and lowest R-square value
   - Tried Ridge and Lasso regression models, both methods does not show significant improvement than the linear models
   - Tree-based models, Decision Tree and Random Forest, made the most improvement in lowering rmse and raising R-squared scores
     
