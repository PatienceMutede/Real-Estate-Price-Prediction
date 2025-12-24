<p align="center">
  <img src="Images/2020-01-29-12-50-26-257.jpg" width="120">
</p>


# Real-Estate-Price-Prediction

Click on link below to view project in Github

[PROJECT 1: Real Estate Price prediction (Random Forest, Multiple Linear Regression)](https://github.com/PatienceMutede/Real-Estate-Price-Prediction/blob/75b9ba0563813b54b9bd7604b01b59eb2b8706cc/Real_Estate_Price_Prediction_project.ipynb)

## **The aim of the project is to develop an automated machine learning model capable of predicting Dubai property prices.**


**Motivation**

Dubai, has one of the most dynamic property markets in the world, contributing 8.2% to the country's GDP. In 2021 alone, the real estate sector recorded over 300 billion Dirhams in transactions, reflecting strong global investor interest and significant year-over-year growth. Machine learning has become an essential tool in real estate for analysing large datasets and identifying key market patterns. Historically, property decisions were based on financial, physical, and transactional data. However, big data has expanded the range of available information, allowing real-time or near-real-time analysis that includes economic shocks, shifts in consumer income, and broader macroeconomic changes—leading to more informed and timely decision-making.


**The Problem in the Financial Crime field**

In fast growing markets like Dubai where transaction volumes are high and property values fluctuate rapidly the need for accurate, data-driven price estimation is even more critical. With large amounts of real estate data now available, the challenge lies in identifying which variables most strongly influence price and creating a reliable model that can predict property values with reasonable accuracy.

The core problem this project seeks to solve is the difficulty of generating consistent, accurate, and objective property price predictions in a complex and dynamic market, and the need for a machine learning model that can help buyers, sellers, and real estate professionals make better-informed pricing decisions.


## **Objectives**

•	Develop an effective, automated property price prediction model.

•	Validate the model’s accuracy and predictive performance.

## Data Explanatory Analysis

**Dealing with Outliers**

![](https://github.com/PatienceMutede/Real-Estate-Price-Prediction/raw/main/images/box%20plot.png)

As shown in Figure above, there is an uneven distribution in our data. It is highly left skewed, the uneven distribution can affect our prediction model. Our tail started from 5 million up to 35 million, so we checked to see how many properties were above 5 million,  and if the number was too small, we split the data and removed the outliers to improve the distribution.


![](https://github.com/PatienceMutede/Real-Estate-Price-Prediction/raw/main/images/Distribution%20plot.png)

The above findings are very interesting, there are 1817 properties which are under 5 million and only 89 properties have prices between 5 million to 35 million. Since the outlier of 89 properties is very small we will eliminate the 89 properties from the model.

**Distribution after outliers are removed**

![](https://github.com/PatienceMutede/Real-Estate-Price-Prediction/raw/main/images/distribution%20after%20adjustments.png)

Skewness = 1.14 and Kurtosis = 1.06

The distribution is now normal and better after removing 89 outliers.

![](https://github.com/PatienceMutede/Real-Estate-Price-Prediction/raw/main/images/neighbourhood%20%20.png)

There are neighbourhoods with more properties, like Downtown Dubai with a total of 302 properties, while some have fewer properties; Al Quoz has only 1 property. This distribution of properties in the neighbourhood is uneven. This would impact the price prediction model. Thus we added another variable to present neighbourhoods with properties under 100 properties. This properties are represented in a new added variable ‘as others’.

![](https://github.com/PatienceMutede/Real-Estate-Price-Prediction/blob/main/images/location%20and%20price.png)

The above plot shows the neighbourhood and the price per sqft, it can be seen that Downtown Dubai is most expensive, which makes sense, followed by Palm Jumeirah.

![](https://github.com/PatienceMutede/Real-Estate-Price-Prediction/raw/main/images/price%20vs%20size.png)

As shown in the figure above, there is a positive linear relationship between the price and the size and sqft. As the size per sqft increases, the price also increases. 

![](https://github.com/PatienceMutede/Real-Estate-Price-Prediction/raw/main/images/number%20of%20bedrroms%20vs%20size.png)

From the above results it shows that the price for 1 bedroom ranges from 500,000 to 5 million depending on location but most of them are between 500 000 to 2.5 million. 2 bedroom apartments are also ranging from 500,000 to 5 million depending on location, they are more evenly distributed across the range. 4 bedrooms are above 1 million up to 5 million.



## **Model Performance** 

Model Fitting (Random Forest)

![](https://github.com/PatienceMutede/Real-Estate-Price-Prediction/blob/main/images/rf.png)

Model Fitting (Linear Regression)

![](https://github.com/PatienceMutede/Real-Estate-Price-Prediction/raw/main/images/linear%20regression%20results.png)

Two machine learning algorithms were run on the training dataset and the performance scores were compared between Multiple Linear Regression and Random Forest. The performance of the models results is shown in the table below. Comparing the two models the random forest had the highest score. The MSE for Random forest is small compared to the Multiple Linear Regression. The two models perform fairly well.

![](https://github.com/PatienceMutede/Real-Estate-Price-Prediction/raw/main/images/machine%20learning.png)

The Random Forest model significantly outperformed Linear Regression, achieving a higher R² value and a much lower MSE. This shows that Random Forest captured the nonlinear relationships within the real estate data far more effectively.

## **Conclusion**

The project successfully produced an accurate, automated machine learning model for predicting real estate prices in Dubai. After cleaning the data by removing extreme outliers and grouping underrepresented neighbourhoods, the Random Forest model proved to be the most reliable, achieving an excellent R² of 0.99. 

The model provides a strong foundation for real-estate professionals, investors, and analysts, enabling:

•More accurate price estimation

•Better evaluation of property value drivers

•Data-supported decision-making

•A consistent, automated approach to real estate valuation

Overall, the Random Forest model offers a robust and practical solution for predicting housing prices in Dubai’s dynamic and competitive property market.

