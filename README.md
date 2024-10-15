# Efficient-Calorie-Estimation-with-PySpark

## Overview
This project analyzes Fitbit user data to derive meaningful insights about activity levels, sleep patterns, and calorie expenditure. Using machine learning models, it predicts calories burned and demonstrates how Apache Spark can be leveraged for scaling the analysis to larger datasets.

### Key Goals:
- Predict calorie expenditure using machine learning models.
- Explore how sedentary behavior influences sleep and caloric burn.
- Demonstrate scalability by implementing the analysis in Apache Spark for handling large datasets.

## Datasets
The datasets used for this analysis include daily activity and sleep data, focusing on variables such as:
- **Sedentary Minutes**: Time spent in sedentary activities.
- **Total Steps**: Total steps taken by users in a day.
- **Total Minutes Asleep**: Overall sleep duration.
- **Calories**: Total calories burned.

## Problem Statement
The primary objective of this project is to develop an efficient and accurate predictive model for estimating calorie expenditure based on user activity and sleep data. This analysis aims to:
1. **Utilize Large-Scale Data Processing**: Leverage PySpark’s distributed computing capabilities for large datasets.
2. **Identify Key Patterns**: Analyze the influence of steps, active minutes, and sleep duration on calorie burn.
3. **Develop Predictive Models**: Create models to predict daily calorie burn using features such as sedentary minutes, steps, and sleep data.
4. **Explore Sedentary Behavior Insights**: Investigate how sedentary behavior impacts caloric expenditure and overall health.

## Project Structure
### 1. **Data Loading**
   - Loaded daily activity and sleep data into Pandas DataFrames for initial exploration.

### 2. **Data Preprocessing**
   - The data was split into training, validation, and test sets using an 80-20 split.
   - The features were scaled using `MinMaxScaler` for better model performance.

### 3. **Exploratory Data Analysis (EDA)**
   - Basic statistics were calculated for key variables like `SedentaryMinutes`, `TotalSteps`, and `Calories`.
   - Visualizations (boxplots and countplots) were created to explore patterns and outliers.

### 4. **Model Building**
   Multiple machine learning models were built to predict calories burned:
   - **Linear Regression**: Achieved an accuracy of 74.79%, with a Mean Absolute Error (MAE) of 571.5923.
   - **Random Forest Regressor**: Outperformed Linear Regression with an accuracy of 77.49%.
   - **XGBoost Regressor**: Demonstrated strong accuracy (78.23%) but slightly underperformed compared to Random Forest.
   - **Gradient-Boosted Trees (GBT)**: Further improved model performance, achieving the highest accuracy.
   - **Scaling with Apache Spark**: A Random Forest model was implemented in Spark, achieving 76.7% accuracy, demonstrating the capability to scale for larger datasets.

### 5. **Model Evaluation**
   - In the local environment, Random Forest achieved the highest accuracy (80.47%) after hyperparameter tuning.
   - In the distributed PySpark environment, the Random Forest model achieved 76.79% accuracy, slightly lower but still effective for larger datasets.

## Key Findings
- Users with higher sedentary minutes tend to have different sleep patterns compared to less sedentary users.
- The Random Forest model is highly effective in predicting calorie expenditure.
- Apache Spark allows the analysis to scale efficiently without significant performance loss.


