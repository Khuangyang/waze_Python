# Waze
## Predicting What made users churned from apps

# Overview
The goal of this project was to  increase overall growth by preventing users to churn from Waze app.EDA first was made to understand relationship between variables and churn rate. linear regression and random forest model to predict high rider gratuity or not. This project utilized yellow taxi trips taken in New York City during 2017. The final random forest model performed with 86% accuracy and 72% precision determining what features were most important in separating low tippers from high tippers. Based on the model, the duration, distance, and cost of the trip were most influential in determining a generous tipper (>20%) vs a non-generous one (<20%).

Business Understanding
Waze, the popular navigation app, generates a significant portion of its revenue through data monetization. By leveraging the vast amount of anonymized user information it collects, Waze is able to create valuable insights and sell this data to interested parties. It involves selling this aggregated data to various entities, including government agencies, urban planners, and businesses. So its important to retent customers in order to gather more data from them.

Data Understanding
The NYC Taxi and Limousine Commission data came from NYC.gov . The data consisted of approximately 408k unique trips and 18 features. The features included information on trip duration and destination, vendor used, toll information, and payment type. The bar chart below shows the breakdown of how many generous tippers (>20%) versus non-generous tippers that exist in the data set. Non-generous vs generous Graph shows the percentage of Non-Generous and Generous Tippers. In connection to this, a feature was engineered to represent if a ride was taken during rush hour or not. Multiple redundant columns were dropped and reformatted into the proper data type.

Modeling and Evaluation
A random forest model comprising 100 decision trees was used to determine feature importance in who would tip generously or not. The below plot shows that trip duration, distance, and the cost of a fare were the Top 3 most important factors in determining a generous tipper from a non-generous one. The overall model performed with 86% accuracy and 72% precision.

Feature Importance Horizontal bar chart showing feature importance of random forest model.

Conclusion
This model can benefit Taxi Drivers in knowing if they will be tipped generously or not; however, running a parametric model to determine how much each variable will influence the actual price of the tip. In the future, adding more information on a rider’s past tipping behavior may also be beneficial in helping the stakeholder address their business problem.

