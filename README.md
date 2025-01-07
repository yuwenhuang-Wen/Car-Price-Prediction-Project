# Car Price Analysis

### Project Overview

This project aims to predict car prices using various regression models. The dataset consists of features such as make, model, year, mileage, engine size, and more. Key metrics used to evaluate model performance are RMSE and R-Squared.


### Data Source

Car Price Data: The dataset used for this project is the "CarPrice.csv" dataset on Kaggle, containing several features and price of each cars sales.


### Tools

- Excel -- [Downlaod Link](https://www.kaggle.com/datasets/hellbuoy/car-price-prediction/data?select=CarPrice_Assignment.csv)
- Jupyter Notebook


### Data Preparation

- Data laoading and inspection
- Handling missing values
- Data cleaning and formatting


### Exploratory Data Analysis (EDA)

#### The EDA involved exploring the dataset, and to answer the questions below:
- How many columns and rows are there?
- What are the numeric and categorical features in the dataset?
- Are there missing values?
- What are the correlations between price and the numeric features and which to exclude?
- According to the feature improtance analysis, which features(numeric & categorical) are less powerful in predicting price, and which to exclude?
- what are the data points distribution of the low correlated or less important features regarding prices?


### Overfit Inspection 

- Applying 10-fold cross validation to inspect if models are too fit


### Results & Findings

<b>1. EDA</b>
   - `Correlation Coefficient Value`
     - Most of the numeric features have absolute value of correlation coefficient above 0.6
     - Some features have correlation absolute value < 0.1
     - compressionration has the least correlations among all features(0.068), so it was excluded in modeling
       
<img src="https://github.com/user-attachments/assets/d7898e8a-755c-4f7d-bc8d-bf6a2c8faeb4" width="900" height="360">



   - `Feature Improtance` (can handle both numeric & categorical)
     - Results from correlation values and feature importance showed some differences
     - Numeric data tends to have higher importance ratio than categorical data
     - Features like enginesize and horsepower were consistently identified as the most important predictors across correlation analysis and feature importance
     - Some features (e.g., symboling or peakrpm) showed less correlations with prcie but still contributed to model accuracy
       
<b>2. Data Observation</b>
   - Scaling numerical features, and encoding categorical variables significantly improved model performance
   - Excluding the least correlated/ important features turned out to get worser measuring metrics results in training set, but better results in testing set
     
<b>3. Models Performance</b>
   - Linear regression models have highest rmse scores and lowest R-square value
   - Modeling with Ridge and Lasso regression, both methods do not show significant improvement than the linear models
   - The Tree-Based models, Decision Tree and Random Forest, made the most improvement in lowering rmse and raising R-squared scores
   - The result suggests to use the Random Forest Regressor for deployment as it offers the best predictions

![CarPrice_rmse](https://github.com/user-attachments/assets/e17b673a-1d6d-43b6-b7ee-f58125ab556e)
![CarPrice_r2](https://github.com/user-attachments/assets/8feb4ce7-3abc-421e-9139-8aa7faad48bf)



### Limitations
-  The dataset is small, containing only 205 rows of data. Considering removing outliers will loose a portion of the dataset, this project did not remove outliers.
