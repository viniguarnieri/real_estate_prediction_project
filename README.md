# Real State Prediction Project

# 1. Business Problem
### Introduction
  The objective of the study is to use a dataset of real estate sales transactions to predict the price-per-unit of a property based on its features. The price-per-unit in this data is based on a unit measurement of 3.3 square meters. Predicting the selling price of a residential property depends on a number of factors, including the property age, availability of local amenities, and location.
  The challenge is to explore and prepare the data, identify predictive features that will help predict the price_per_unit label, and train a regression model that achieves the lowest Root Mean Square Error (RMSE) possible (which must be less than 7) when evaluated against a test subset of data. After that, the trained model should be saved and then used to predict the price_per_unit for the following real estate transactions.

| transaction_date | house_age | transit_distance | local_convenience_stores | latitude | longitude |
| ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | 
| 2013.167 | 16.2 | 289.3248  | 5  | 24.98203  | 121.54348  |
| 2013.000 | 13.6 | 4082.015  | 0  | 24.94155  | 121.50381  |
    
 ## FEATURES
 The data consists of the following variables:

- **transaction_date** - the transaction date (for example, 2013.250=2013 March, 2013.500=2013 June, etc.)
- **house_age** - the house age (in years)
- **transit_distance** - the distance to the nearest light rail station (in meters)
- **local_convenience_stores** - the number of convenience stores within walking distance
- **latitude** - the geographic coordinate, latitude
- **longitude** - the geographic coordinate, longitude
- **price_per_unit** house price of unit area (3.3 square meters)

# 2. Solution Strategy
  My strategy to solve this challenge was:
  
  Step 01. Data Description: My goal is to use statistics metrics to identify data outside the scope of business.
  
  Step 02. Data Filtering: Filter rows and select columns that do not contain information for modeling or that do not match the scope of the business.
  
  Step 03. Exploratory Data Analisys: Explore the data to find insights and better undestand the impact of variables on model training.
  
  Step 04. Data Preparation: Prepare the data so that the Machine Learning models can learn the specific behavior.
  
  Step 05. Feature Selection: Selection of the most significant attributes for training the model.
  
  Step 06. Machine Learning Modeling: Machine Learning model training.
  
  Step 07. Use the model to predict the column 'price_per_unit' of a new dataframe.

# 4. Machine Learning Model Applied
- Tests were made using different algorithms:
    - Linear Regression
    - Decision Tree Regressor
    - Random Forest Regressor
    - Gradient Boosting Regressor
  
# 5. Machine Learning Model Performance
  The chosen algorithm was Random Forest Regression because it showed better results than the others. The Gradient Boosting Regressor was a good model too however it did not better than Random Forest. 
  
| Mean Squared Error  | Root Mean Square Error | R-squared  | 
| ------------- | ------------- | ------------- | 
| 37.5327  | 6.1264  | 0.6797  |

# 6. Results 
  When the model trained was used in the new dataframe the results obtained for the 'price_per_unit' column were the following:
| price_per_unit |
| ------------- | 
| 49.274  |
| 16.641 |
