# Waze
## Predicting What made users churned from apps

# Overview
The goal of this project was to  increase overall growth by preventing users to churn from Waze app. EDA first was made to understand relationship between variables and churn rate. linear regression and random forest model to predict high rider gratuity or not. This project utilized yellow taxi trips taken in New York City during 2017. The final random forest model performed with 86% accuracy and 72% precision determining what features were most important in separating low tippers from high tippers. Based on the model, the duration, distance, and cost of the trip were most influential in determining a generous tipper (>20%) vs a non-generous one (<20%).

# Business Understanding
Waze, the popular navigation app, generates a significant portion of its revenue through data monetization. By leveraging the vast amount of anonymized user information it collects, Waze is able to create valuable insights and sell this data to interested parties. It involves selling this aggregated data to various entities, including government agencies, urban planners, and businesses. So its important to retent customers in order to gather more data from them.

# Data Understanding
None of the variables in the first 10 observations have missing values. Note that this does not imply the whole dataset does not have any missing values. The variables label and device are of type object; total_sessions, driven_km_drives, and duration_minutes_drives are of type float64; the rest of the variables are of type int64. There are 14,999 rows and 13 columns. The dataset has 700 missing values in the label column. Comparing summary statistics of the observations with missing retention labels with those that aren't missing any values reveals nothing remarkable. The means and standard deviations are fairly consistent between the two groups. Furthermore, features engineering was applied to create meaningful new varialbes (driven_km_drives, km_per_driving_day, drives_per_driving_day, by using median instead of mean due to outliers.

# Modeling and Evaluation
A random forest model comprising 100 decision trees was used to determine feature importance in who would tip generously or not. The below plot shows that trip duration, distance, and the cost of a fare were the Top 3 most important factors in determining a generous tipper from a non-generous one. The overall model performed with 86% accuracy and 72% precision.

Feature Importance Horizontal bar chart showing feature importance of random forest model.

# Conclusion
The median user who churned drove 698 kilometers each day they drove last month, which is ~240% the per-drive-day distance of retained users. The median churned user had a similarly disproporionate number of drives per drive day compared to retained users.
Perhaps the data in particular the sample of churned users—contains a high proportion of long-haul truckers.
In consideration of how much these users drive, it would be worthwhile to recommend to Waze that they gather more data on these super-drivers. It's possible that the reason for their driving so much is also the reason why the Waze app does not meet their specific set of needs, which may differ from the needs of a more typical driver, such as a commuter.
