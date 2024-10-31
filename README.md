
# Big Mart Sales Prediction - Analytics Vidhya (Hackathon Competition) [Nov 2024]






## Problem statement:

The data scientists at BigMart have collected 2013 sales data for 1559 products across 10 stores in different cities. Also, certain attributes of each product and store have been defined. The aim is to build a predictive model and predict the sales of each product at a particular outlet.

Using this model, BigMart will try to understand the properties of products and outlets which play a key role in increasing sales.

Please note that the data may have missing values as some stores might not report all the data due to technical glitches. Hence, it will be required to treat them accordingly. 





## Data Description

We have train (8523) and test (5681) data set, train data set has both input and output variable(s). You need to predict the sales for test data set.

Train file: CSV containing the item outlet information with sales value

Variable: Description
- Item_Identifier: Unique product ID
- Item_Weight: Weight of product
- Item_Fat_Content: Whether the product is low fat or not
- Item_Visibility: The % of total display area of all products in a store allocated to the particular product
- Item_Type: The category to which the product belongs
- Item_MRP: Maximum Retail Price (list price) of the product
- Outlet_Identifier: Unique store ID
- Outlet_Establishment_Year: The year in which store was established
- Outlet_Size: The size of the store in terms of ground area covered
- Outlet_Location_Type: The type of city in which the store is located
- Outlet_Type: Whether the outlet is just a grocery store or some sort of supermarket
- Item_Outlet_Sales: Sales of the product in the particular store. This is the outcome variable to be predicted.


Test file: CSV containing item outlet combinations for which sales need to be forecasted

Variable: Description
- Item_Identifier: Unique product ID
- Item_Weight: Weight of product
- Item_Fat_Content: Whether the product is low fat or not
- Item_Visibility: The % of total display area of all products in a store allocated to the particular product
- Item_Type: The category to which the product belongs
- Item_MRP: Maximum Retail Price (list price) of the product
- Outlet_Identifier: Unique store ID
- Outlet_Establishment_Year: The year in which store was established
- Outlet_Size: The size of the store in terms of ground area covered
- Outlet_Location_Type: The type of city in which the store is located
- Outlet_Type: Whether the outlet is just a grocery store or some sort of supermarket


## Inference

**Analysis of the Dataset Using Regression Models for Big Mart Sales Prediction**

* Model Performance Overview: 
The evaluation of various regression models for predicting sales at Big Mart indicates that the tuned versions of Random Forest, Gradient Boosting, and XGBoost Regressors are the top performers. Notably, the tuned XGBoost Regressor achieved an R² score of 65.47% on the test set, with an RMSE of 1016.17 and a MAPE of 50.51%. These metrics suggest that the model effectively captures the underlying patterns of the target variable, although there remains potential for further enhancement.

* Error Metrics: 
The Root Mean Square Error (RMSE) and Mean Absolute Percentage Error (MAPE) for each model provide insights into prediction accuracy. The tuned Gradient Boosting, Random Forest, and XGBoost regressors show the lowest RMSE values on the test set, indicating high prediction accuracy. The tuned Random Forest recorded an RMSE of 1019.62, while the tuned Gradient Boosting reached 1020.88, both closely aligned with the performance of the XGBoost model.

* Overfitting Insights: 
The Decision Tree Regressor displayed an R² score of 100% on the training set but plummeted to 35.08% on the test set, indicating severe overfitting. This significant disparity illustrates the model’s limited ability to generalize to unseen data, highlighting the necessity for more robust ensemble models like Random Forest, Bagging, and Boosting regressors, which better balance complexity and generalization.

* Model Selection: 
Among all evaluated models, the tuned Random Forest, Gradient Boosting, and XGBoost Regressors exhibit the strongest generalization capabilities while effectively balancing bias and variance. Their performance metrics are as follows:

        Tuned XGBoost Regressor: R²: 65.47% | RMSE: 1016.17 | MAPE: 50.51%
        Tuned Random Forest Regressor: R²: 65.23% | RMSE: 1019.62 | MAPE: 51.03%
        Tuned Gradient Boosting Regressor: R²: 65.15% | RMSE: 1020.88 | MAPE: 50.68%
  
These models demonstrate similar performance, making them strong candidates for further analysis and optimization.

* Hyperparameter Tuning: 
While the current tuning has yielded promising results, there remains significant potential for improvement. Further exploration of hyperparameters—such as learning rate, regularization terms, and tree-specific parameters—could enhance predictive power. Utilizing techniques like Randomized Search or Bayesian Optimization may uncover optimal settings that maximize model performance.

* Business Impact: 
The predictive performance of these models is crucial in applications such as sales forecasting, where accurate predictions can significantly influence inventory management and resource allocation. Reliable sales forecasts help in optimizing stock levels, ultimately reducing costs associated with stockouts or overstocking. The high RMSE and MAPE values underscore the importance of assessing the implications of prediction errors to guide resource allocation effectively.

**Conclusion**

The analysis illustrates that the tuned XGBoost, Random Forest, and Gradient Boosting Regressors provide the best balance between predictive performance and generalization, with XGBoost showing marginally superior results. However, it is essential to evaluate each model's prediction error concerning the practical needs of the application. Ensuring alignment between model performance and organizational goals, particularly in resource planning and management, is critical. Further refinement and careful consideration of trade-offs between predictive performance and resource constraints will help achieve optimal outcomes in predictive tasks.