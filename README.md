# Zillow House Price Forecasting using Time Series Analysis

Project by: Rivana Christie, Pratik Dahibhate and Mitanshi Vyas

The housing market is subject to constant fluctuations, and predicting the changes in house prices and rental rates is a challenge that many individuals and investors face. The lack of reliable means to estimate and predict these prices could result in uninformed decisions, financial risks, and missed opportunities. 

Additionally, the COVID-19 pandemic had a significant impact on the real estate industry, further complicating the prediction of future housing prices and rental rates.

To address this problem, we developed a forecasting model employing ML algorithms such as ARIMA and SARIMA. Our models considered various factors that affected house prices and rental rates, such as economic indicators, demographic trends, interest rates, and market supply and demand. Our model used machine learning algorithms to analyze historical data, identify patterns, and predict future trends in the housing market. 

# About the dataset
For this forecasting project, we utilized the Housing Value and Rental Dataset from Zillow's Research Dataset Website. The dataset is available at https://www.zillow.com/research/data/ and contains a range of valuable features, including RegionID, SizeRank, RegionName, RegionType, StateName, State, City, Metro, and CountyName. 

These features provide a comprehensive view of the housing market across various regions, enabling us to analyze and forecast trends at different levels of granularity. By leveraging this dataset, we were able to build robust and accurate forecasting models that can help individuals and investors make informed decisions in the real estate market.

# Exploratory Data Analysis
1. Top 10 States by Real Estate Price Increase Rate from 2013 to 2023

![image](https://github.com/rivanachristie/Time-Series-Analysis-on-Zillow-House-Price-Dataset/assets/98617715/2483c6f1-7e60-480e-ac22-5b4e0e60eeb0)

2. Top 10 Cities by Real Estate Price Increase Rate from 2013 to 2023

![image](https://github.com/rivanachristie/Time-Series-Analysis-on-Zillow-House-Price-Dataset/assets/98617715/79a3e43d-8936-4ca3-81b6-85796e7faac7)

3. House Prices for 6 cities from Jan 2000 to Jan 2023

![image](https://github.com/rivanachristie/Time-Series-Analysis-on-Zillow-House-Price-Dataset/assets/98617715/dad8dcc0-8286-4163-b402-fc4e96effa9c)

# Data Preprocessing
Since we are dealing with time series data, there were different steps to preprocess this data. We leveraged the following techniques:
1. Filling missing metro names with city names
2. Backfilling NaN values in price columns
3. Dropping non-datetime columns
4. Converting month columns to datetime
5. Melting the time series dataframe

# Feature Engineering
To further analyze the dataset, we created 4 new columns:
1. ROI_5years - Difference in prices in the last 5 years
2. ROI_10years - Difference in prices in the last 10 years
3. price_increase - Difference in prices since the beginning
4. COVID_increase - Difference in prices since the start of COVID i.e. December 2019

# Data Modeling
We used different statistical and machine learning models like ARIMA, SARIMAX, Prophet model for getting a time series for the mentioned cities. 

## ARIMA Model
ARIMA stands for Auto-Regressive Integrated Moving Average. It is a form of a regression analysis that gauges the strength of one dependent variable which is relative to other changing variables. The model has 3 parameters p, d, q which are for lag order, degree of differencing, order of moving average respectively. 

![image](https://github.com/rivanachristie/Time-Series-Analysis-on-Zillow-House-Price-Dataset/assets/98617715/e2a46c83-a690-48ba-bce5-5798a56bfaa5)

## SARIMA Model
SARIMA stands for Seasonal Auto-Regressive Integrated Moving Average. It adds the seasonality component to the ARIMA model, for a better forecasting of time series. It contains 3 more parameters in addition to the p, d, q from the ARIMA model. The parameters are P, D, Q which stands for seasonal autoregressive order, seasonal difference order and seasonal moving average order respectively.

![image](https://github.com/rivanachristie/Time-Series-Analysis-on-Zillow-House-Price-Dataset/assets/98617715/e1569450-4ff9-45c0-aafa-47d6ecbe2755)

## Prophet Model
Prophet is open-source software released by Facebook’s Data Science team. Prophet is a procedure for forecasting time series data based on an additive model. In this model the non-linear trends fit yearly, weekly, and daily seasonality, also the holiday effects can be added in the modeling. It is robust to missing data and shifts in the trend, and typically handles outliers well.

![image](https://github.com/rivanachristie/Time-Series-Analysis-on-Zillow-House-Price-Dataset/assets/98617715/4a047a8d-6271-46e5-9e1b-4a890ec4b210)

# Model Comparison
We compared the RMSE values for the three models for each city and visualized them using a bar chart. From the plot, we can see that SARIMAX has higher RMSE values, whereas Prophet has low or average values for RMSE. So, we can conclude that the Prophet model gave the best results.

![image](https://github.com/rivanachristie/Time-Series-Analysis-on-Zillow-House-Price-Dataset/assets/98617715/b8e9ced6-5898-4d40-a666-43cd620d2339)

# Failure and Future Scope
Currently, the housing market in the US is undergoing a market correction, with an increase in mortgage rates and decline in house prices. This is also a result of the huge number of houses that are currently unsold. This occurrence could not be predicted by the model solely based on the house price data provided. Hence, we can consider this an example of a failure. In order to overcome this failure or to reduce its effect, we could utilize other datasets that provide information related to other external factors that affect house prices.



