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
