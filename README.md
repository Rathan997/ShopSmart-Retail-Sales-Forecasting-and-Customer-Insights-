# ShopSmart-Retail-Sales-Forecasting-and-Customer-Insights-
🛍️ ShopSmart – Retail Sales Forecasting & Customer Insights
📘 Project Overview
This project performs Exploratory Data Analysis (EDA), Descriptive Statistics, and Predictive Analytics on a Superstore Sales Dataset.
It aims to:

Analyze sales trends over time.

Identify correlations and outliers in the data.

Measure the statistical impact of discounts on sales.

Forecast future sales using ARIMA.

Predict customer repurchase behavior using Machine Learning models.

📂 Dataset
File Used: SuperStore_Sales_Dataset.csv

The dataset should contain (or similar to):

Column	Description
Order Date	Date of each order
Sales	Total sales amount
Discount	Discount applied
Profit	Profit from sale
Quantity	Number of units sold
Customer ID	Unique identifier for customers
Order ID	Unique identifier for orders
⚠️ Column names are automatically cleaned (converted to lowercase and trimmed).
The script dynamically detects key columns even if their names differ slightly (e.g., Order_Date, Sales Amount, etc.).

⚙️ Requirements
Before running the notebook/script, install the following dependencies:

pip install pandas numpy matplotlib seaborn statsmodels scikit-learn scipy
📖 Steps in the Code
1️⃣ Import Libraries
All required libraries for data manipulation, visualization, statistical testing, and machine learning are imported.

2️⃣ Load and Clean Data
Reads the dataset (SuperStore_Sales_Dataset.csv) into a Pandas DataFrame.

Cleans column names (lowercase, trimmed).

Fills missing values for numerical and categorical columns.

Ensures correct data types for numeric and date fields.

3️⃣ Column Detection
Automatically identifies essential columns:

Order Date

Sales

Discount

Profit

Quantity

Customer ID

Order ID

If a column is missing, default values are created (e.g., discount = 0).

4️⃣ Exploratory Data Analysis (EDA)
🕒 Sales Trend Over Time
Plots a line chart of total sales over all available dates.

📅 Monthly Sales Trend
Aggregates data monthly and visualizes trends with a monthly sales line plot.

🔥 Correlation Heatmap
Computes correlations among numeric variables (sales, profit, discount, quantity) and displays them using a heatmap.

🚨 Outlier Detection
Detects outliers using Z-score > 3.

Prints count and percentage of outliers.

Displays a boxplot of numeric variables for visual inspection.

5️⃣ Statistical Analysis
🎯 Discount Impact on Sales
Performs a t-test comparing discounted vs non-discounted sales.

Reports if discounts significantly affect sales based on the p-value.

6️⃣ Time Series Forecasting (ARIMA)
Groups daily sales and converts them to a time series.

Splits into train (80%) and test (20%) sets.

Fits an ARIMA(1,1,1) model to forecast sales.

Plots training, test, and forecast results.

Calculates and prints RMSE for accuracy.

7️⃣ Customer Repurchase Prediction
If customer_id and order_id columns exist:

Calculates number of unique orders per customer.

Defines “repurchase” customers as those with >1 order.

Aggregates average sales, discount, profit, and quantity per customer.

Splits data into train/test sets.

Trains two models:

Logistic Regression

Random Forest Classifier

Evaluates using Accuracy, Recall, and Precision.

Displays a confusion matrix for Random Forest results.

8️⃣ Outputs
Console Outputs:

Missing column handling messages

Outlier count and percentage

T-test results

Model evaluation metrics

RMSE for ARIMA forecast

“All analysis completed successfully!”

Visual Outputs:

Sales Trend Over Time

Monthly Sales Trend

Correlation Heatmap

Outlier Boxplot

ARIMA Forecast Plot

Confusion Matrix (Random Forest)

🧠 Insights Derived
Seasonal trends in sales help with demand forecasting.

Correlation heatmap reveals drivers of profit and sales.

Outlier detection identifies unusual transactions.

Discount impact indicates pricing effectiveness.

ARIMA forecasting predicts near-future sales volume.

Customer repurchase prediction supports loyalty program design.

📊 Example Key Results
Outliers: ~2–5% depending on dataset

T-test p-value: < 0.05 → Discounts significantly impact sales

ARIMA RMSE: Indicates forecast accuracy

Random Forest Accuracy: Usually higher than Logistic Regression

📎 Notes
Works with similar retail sales datasets (Superstore-style).

For improved ARIMA performance, consider seasonal models (SARIMA).

For customer prediction, more features (e.g., region, segment) can enhance accuracy.
