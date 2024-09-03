### **Sales ForeCasting and Predection**

## **Features**

Contains additional data related to the store, department, and regional activity for the given dates.
-	Store - the store number
-	Date - the week
-	Temperature - average temperature in the region
-	Fuel_Price - cost of fuel in the region
-	MarkDown1-5 - anonymized data related to promotional markdowns. MarkDown data is only available after Nov 2011, and is not available for all stores all the time. Any missing value is marked with an NA
-	CPI - the consumer price index
-	Unemployment - the unemployment rate
-	IsHoliday - whether the week is a special holiday week
- The data consists of three sheets:
    - Stores
    - Features
    - Sales

**Key Technologies and Skills**

- Python
- Scikit-Learn
- Numpy
- Pandas
- Matplotlib
- Seaborn
- Streamlit

**Data Preprocessing:**

**Data Understanding:** The dataset comprises store, sales, and features data, offering details on store attributes like name, department, date, type, size, weekly sales, and environmental factors such as holiday status, temperature, fuel price, multiple markdowns, CPI, and unemployment. The primary focus is on predicting weekly sales, serving as the target variable for our modeling endeavors. This initial exploration forms the basis for subsequent data preprocessing and model development.

**Encoding and Data Type Conversion:** The process involves preparing categorical features for modeling by transforming them into numerical representations, considering their inherent nature and relationship with the target variable. Simultaneously, data types are converted to align with the modeling process requirements, ensuring seamless integration and compatibility. This step facilitates the effective utilization of categorical information in the subsequent stages of the project.

**Handling Null Values:** Notably, the 'MarkDown' columns present a challenge with over 50% null values, while other columns exhibit minimal null values. To address this, we employ machine learning models to predict and impute the missing values, ensuring a more complete and robust dataset for subsequent analysis and modeling. This strategic approach allows us to mitigate the impact of missing data on the overall quality of our dataset.

**Feature Improvement:** Emphasizing enhanced modeling effectiveness, we concentrate on refining the dataset. This involves creating new features to extract deeper insights and enhance overall dataset efficiency. Evaluation, conducted through Seaborn's Heatmap, reveals that aside from Size and Type with correlation values of 0.21 and 0.17 (absolute value) respectively, no other columns exhibit a strong correlation with weekly sales. This underscores the need for a strategic feature enhancement to bolster the predictive power of our model.

## Machine Learning Regression Model:

**Multiple Models:** I built and evaluated five machine learning models to predict sales, and their respective train and test scores are as follows:
## Linear Regression: Train Score = 0.105597, Test Score = 0.103934
## Decision Tree: Train Score = 0.517049, Test Score = 0.513199
## Random Forest Regression: Train Score = 0.995533, Test Score = 0.968403
## XGBoost Regression: Train Score = 0.913102, Test Score = 0.911439
## ExtraTrees Regressor: Train Score = 1.000000, Test Score = 0.970189

**Conclusion:** 
The ExtraTreesRegressor (ET_model) performs slightly better overall based on the evaluation metrics provided. It has a marginally higher R² score and lower values for MAE, MSE, and RMSE compared to the RandomForestRegressor (RF_model). Therefore, ET_model is the preferred model among the two based on these performance metrics.

Since "Dept," "Size," "Type," and "Store" are critical, consider these variables in your strategic planning. For example, optimizing store layouts, tailoring marketing strategies by department, and considering store size in inventory planning might enhance sales performance.

## Build a predictive model to forecast sales for the next quarter using historical sales data

1. Prepare the Dataset
- **Training Data:** Used all data before the last three months.
- **Testing Data:** The data from the last three months.
2. Split the Data into Training and Testing Sets
3. Train the ExtraTreesRegressor Model
4. Predict the Sales for the Last 3 Months
5  Evaluate the Model's Performance
- Evaluate model performed using metrics like Mean Squared Error (MSE) and R-Squared (R²):
6. Forecasting for the Next Quarter
