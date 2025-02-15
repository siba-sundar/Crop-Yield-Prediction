# Crop Yield Prediction Model

## Description
This project develops a **crop yield prediction model** using **machine learning** techniques. By analyzing historical data, weather patterns, and soil conditions, the model forecasts crop yields, helping farmers and stakeholders make informed decisions to optimize production and manage resources efficiently.

## Problem Statement
With the global population increasing, **efficient agricultural practices** are crucial to ensuring food security. Crop yield prediction helps in **resource planning, reducing crop loss, and mitigating climate-related risks** by providing insights into how various factors influence crop production.

## Approach
### 1. Data Collection & Preprocessing
- Features: **Area, Item, Year, Yield (hg/ha), Rainfall (mm/year), Pesticide Usage (tonnes), Temperature**
- Handling **missing values, duplicates,** and **scaling**

### 2. Data Visualization
- Graphs and **diagrams** to represent processed data insights

### 3. Model Selection
Three machine learning models were implemented:
1. **Linear Regression**
2. **Decision Tree**
3. **K-Nearest Neighbors (KNN)**

### 4. Model Training & Testing
- **80-20 split** for training and testing
- Models trained on the dataset and validated for accuracy

### 5. Evaluation
- Metrics Used: **Mean Squared Error (MSE), Mean Absolute Error (MAE), R-squared (R²), Root Mean Squared Error (RMSE)**
- Performance comparisons via **graphs**

### 6. Prediction
- Sample data passed through the models to generate predictions

## Installation & Usage
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/crop-yield-prediction.git
   cd crop-yield-prediction

