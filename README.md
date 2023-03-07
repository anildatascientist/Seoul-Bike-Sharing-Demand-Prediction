# Seoul-Bike-Sharing-Demand-Prediction

# Abstract:
As a convenient, economical, and eco-friendly travel mode, bike-sharing greatly improved urban mobility. However, it is often very difficult to achieve a balanced utilization of shared bikes due to the asymmetric user demand distribution and the insufficient numbers of shared bikes, docks, or parking areas. If we can predict the short-run bike-sharing demand, it will help operating agencies rebalance bike-sharing systems in a timely and efficient way. 

# Introduction:
Bike-sharing system demand nowadays is increasing in proportional manners globally. This system has gained a lot of attention with its cost-effective system and easy-to-use nature. This system has already attracted a huge customer base globally like in South Korea, São Paulo, China, and Australia. A bike-sharing system generally rents bikes on an hour, day, and monthly basis and is generally based on static pricing inclusive of the hour, days, or month. Because of its affordability and easy renting system, anyone can commute on arrival. According to our problem, our main aim is to build a predictive model so as to find the number of bikes rented based on the given dataset.               

# Business Requirement:
The main objective is to build a predictive model, which could help to train a model to predict the number of bike rentals of the year given the weather conditions.  This would in turn help to predict quickly and efficiently.

# Data Summary:
The dataset contains the following columns: 

•	Date: year-month-day

•	Rented Bike count - Count of bikes rented at each hour

•	Hour - Hour of the day

•	Temperature-Temperature in Celsius

•	Humidity - %

•	Windspeed - m/s

•	Visibility - 10m

•	Dew point temperature - Celsius

•	Solar radiation - MJ/m2

•	Rainfall - mm

•	Snowfall - cm

•	Seasons - Winter, Spring, Summer, Autumn

•	Holiday - Holiday/No holiday

•	Functional Day - NoFunc(Non Functional Hours), Fun(Functional hours)

# Conclusion and Insights:
In the analysis, initially performed EDA on all the features of our dataset. 
First analyzed the dependent variable i.e., 'Rented Bike Count', and also transformed it. 
Next, was the analysis of the categorical variable and dropped the variable that had the majority of one class. Thereafter, analyzed numerical variables, and checked out the correlation, distribution, and relationship with the dependent variable. 
I removed some numerical features that had mostly 0 values and hot encoded the categorical variables.
Next, implemented 7 machine learning algorithms Linear Regression, Lasso, Ridge, Elastic Net, Decision Tree, Random Forest, XGBoost, and XGBoost with Grid Search CV. We did some hyperparameter tuning to improve our model performance.
No overfitting was seen. 
Compared the root mean squared error and mean absolute error of all the models, the XG- boost regression model has less root mean squared error and mean absolute error, ending with the Adj. R-squared of 91%. So, finally, this model is best for predicting the bike rental count on daily basis. 
For all the models, temperature or hour was ranked as the most influential variable to predict the rental bike demand at each hour.

Following are the results of the evaluation:


![Evaluation Results](https://user-images.githubusercontent.com/59911959/223329899-97bd58a3-42a3-4efa-afa0-efac86ed1b7c.png)


•	Out of all the above models “Random forest Regressor” gives the highest Adj.R2 score of 99%.

• For the Train Set and “XG Boost Grid search CV” gives the highest Adj.R2 score of 91% for the Test set.
