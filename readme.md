# Crop Yield Prediction

## Problem Definition

The goal of this project is to develop a crop yield prediction model using machine learning techniques. The model will forecast crop yields based on historical data, weather patterns, and other relevant features.

## Why This Problem?

With an ever-growing global population, efficient agricultural practices are vital to meet the rising food demands. Crop yield prediction models support farmers and agricultural stakeholders by providing insights into future yields, helping in resource planning and management.

## Approach

To build the crop yield prediction model, the following approach was implemented:

1. **Data Collection and Preprocessing**:
   - The dataset includes features such as Area, Item, Year, Yield (hg/ha), average rainfall (mm/year), pesticide usage (tonnes), and average temperature.
   - Data was preprocessed to handle missing values, duplicates, and other inconsistencies.

2. **Data Visualization**:
   - After data collection and preprocessing, the processed data was represented in the form of graphs and diagrams for better understanding.

3. **Model Selection**:
   - Three models were chosen for this task:
     1. Linear Regression
     2. Decision Tree
     3. K-Nearest Neighbours (KNN)

4. **Model Training and Testing**:
   - The dataset was split into training and testing sets (80-20 split). The models were trained on the training set and validated on the test set to evaluate their performance.

5. **Evaluation**:
   - To measure the accuracy of the predictions, the following metrics were calculated: Mean Squared Error (MSE), Mean Absolute Error (MAE), R-squared (R²), and Root Mean Squared Error (RMSE).

6. **Prediction**:
   - After evaluation, sample data were passed to the three models, and predictions were made.

## Data Collection and Preprocessing

```python
import pandas as pd
import numpy as np
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LinearRegression
from sklearn.tree import DecisionTreeRegressor
from sklearn.neighbors import KNeighborsRegressor
from sklearn.metrics import mean_squared_error, mean_absolute_error, r2_score
from sklearn.compose import ColumnTransformer
from sklearn.preprocessing import OneHotEncoder, StandardScaler
import matplotlib.pyplot as plt
import seaborn as sns

# Load the dataset
df = pd.read_csv('./yield_df.csv')

# Display the first few rows of the dataset
df.head()

# Drop the S.No column
df.drop('S.No', axis=1, inplace=True)

# Check for null values
print(df.isnull().sum())

# Check for duplicate values and drop them
df.drop_duplicates(inplace=True)
