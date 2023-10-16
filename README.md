
# background

I wanted to see how retail stores and distributors make predictions for the inventory , how arima model can be used in retail, and how it works with dataset that has trend and seasonlity. 

Analyzing store performance stands as a paramount responsibility for retail enterprises. A key hurdle encountered in the retail realm involves the anticipation of sales and necessary inventory levels at individual stores, an important step in preventing overstocking and understocking. This strategic foresight not only cultivates an optimal customer experience but also shields the business from losses, ultimately upholding the store's viability and operational longevity.

Rossmann operates over 3,000 drug stores in 7 European countries. We are tasked with predicting their daily sales for up to six weeks in advance. Store sales are influenced by many factors, including promotions, competition, school and state holidays, seasonality, and locality. 


# Files
 Historical sales data for 1,115 stores. 
•	train.csv - historical data including Sales
•	test.csv - historical data excluding Sales
•	sample_submission.csv - a sample submission file in the correct format
•	store.csv - supplemental information about the stores

# Approach
My initial steps will involve delving into the dataset, followed by addressing any gaps caused by missing values, and conducting constructive feature engineering. Subsequently, our focus will shift towards constructing predictive models aimed at forecasting sales. 

# Evaluation Metrics
There are two popular metrics used in measuring the performance of regression (continuous variable) models i.e MAE & RMSE.

Mean Absolute Error (MAE): It is the average of the absolute difference between the predicted values and observed values.
Root Mean Square Error (RMSE): It is the square root of the average of squared differences between the predicted values and observed values.

MAE is easier to understand and interpret but RMSE works well in situations where large errors are undesirable. 

# Libraries Used
Numpy, pandas, seaborn, statsmodels, ARIMA

# Model Comparison & Selection

I choose SARIMA as our final model to predict the sales because it gives us the least RMSE and is well suited to our needs of predicting time series seasonal data. We chose ARIMA(1, 1, 1)x(0, 1, 1, 12)12 as the final parameter combination with AIC of 1806.29 and RMSE of 739

# Reflection
•	The most interesting thing about the data was that the category of stores having the highest sales didn’t have the highest sale per customer. It might be because those stores sell small items, which are needed on a daily basis.

•	Another interesting thing was that running a promotion for the second time didn’t help in increasing sales. It is probably because customers already purchased whatever they wanted during the first promotional sale.
