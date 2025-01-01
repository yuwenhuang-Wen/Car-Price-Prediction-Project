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

#### The EDA aims to help determine if all features are included in the modeling, so there are analysis are based on the questions of:
- What are the correlations between the numeric features and car price?
- How positively / negatively are the 5 basic car features (wheelbase, carlength, carwidth, carheight, curbweight) correlated to the price?
- What are the relationships between price and each negatively correlated numeric feature?
- How are the prices distributed among the symboling levels?

### Overfit Inspection 

- Applied 10-fold cross validation to inspect if models are too fit.


### Findings

1. Feature Improtance
   - Even some features are less
   - maybe should exclude...
2. Data Observation
   - Including encoded and scaled categorical data improved the predicting results than only modeling by numeric data
   - 
3. Models Performance
