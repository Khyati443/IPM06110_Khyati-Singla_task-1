README – Energy Consumption Forecasting with Pattern Discovery
Overview
This project analyzes smart home energy consumption data to identify usage patterns and forecast future energy demand. The pipeline combines unsupervised learning (clustering) with supervised machine learning models to improve prediction accuracy.
Dataset
The dataset Energy Consumption Dataset for Smart Homes contains timestamp-based records of appliance electricity usage including:
Ventilador
PC
AC
Lampara
TV
Each row represents energy usage at a specific time.
Workflow
1. Data Loading
The dataset is loaded using Pandas from an Excel file.
2. Data Preprocessing
Timestamp is converted into datetime format.
New time-based features are extracted:
Hour
Day
Month
Total energy consumption is calculated by summing appliance usage.
3. Exploratory Analysis
A correlation matrix is generated using Seaborn to understand relationships between variables.
4. Feature Extraction
Energy consumption patterns are derived by grouping data by hour and calculating:
Average consumption
Variance
Peak consumption
5. Clustering
K-Means clustering is applied to group hours with similar consumption behavior.
Clusters help identify different energy usage patterns.
6. Data Preparation for Prediction
Features used for prediction:
Appliance usage
Hour of the day
Data is split into training (80%) and testing (20%) sets.
7. Machine Learning Models
Two supervised regression models are trained:
Random Forest Regressor
Gradient Boosting Regressor
These models predict total energy consumption.
8. Model Evaluation
Model performance is evaluated using:
RMSE (Root Mean Squared Error)
MAE (Mean Absolute Error)
R² Score
9. Feature Importance
F-Score analysis identifies statistically important predictors.
Random Forest feature importance shows which appliances contribute most to energy consumption.
10. Visualization
The pipeline generates:
Correlation heatmap
Cluster visualization
Feature importance graph
Actual vs predicted energy consumption plot
Outcome
The project helps utility providers:
Identify energy consumption patterns
Segment usage behaviors using clustering
Predict future energy demand using machine learning models.
