# Avocado-Price-Forecasting
## Introduction:

This repository delves into the world of avocado prices, exploring how they fluctuate across regions and uncovering valuable insights for informed market decisions. The analysis leverages the power of R, a robust statistical programming language, to build forecasting models for California and Syracuse - two key avocado hubs.

![DALL·E 2024-06-03 10 01 23 - A detailed infographic illustrating avocado price prediction using different models  The image should include sections for each region (California and Syracuse)](https://github.com/NiharikaTHub/Avocado-Price-Forecasting/assets/171478142/349869cc-bea2-416c-9a53-d12688d0ce08)

 ## Tech Stack:
 
* R (Programming Language)
* tidyverse (Data Analysis and Visualization Suite)
* dplyr (Data Manipulation)
* MLmetrics (Machine Learning Evaluation Metrics)
* tseries (Time Series Analysis)
* ggplot2 (Data Visualization)
* forecast (Time Series Forecasting)
* TTR (Technical Analysis Tools)

## Exploratory Data Analysis (EDA):

Through meticulous EDA, we gained a comprehensive understanding of the data:

* **California vs. Syracuse:** California's avocado market, characterized by higher demand and supply, exhibits less price sensitivity compared to Syracuse. This is evident in both organic and conventional avocado pricing.
* **Organic Avocado Dynamics:** Syracuse's organic avocado prices displayed a fascinating trend. A significant price drop in mid-2017 coincided with an increase in sales volume, highlighting the market's responsiveness to changes.
* **Focus on Organic Avos:** Given the consistent patterns observed across both regions and the slightly higher sensitivity of organic avocados to market dynamics, we strategically shifted our focus to modeling the average price of organic avocados. This approach allows for a more generalized model that captures regional trends and considers the broader market implications of organic avocado pricing.

<img width="1118" alt="Screenshot 2024-06-03 at 9 49 13 AM" src="https://github.com/NiharikaTHub/Avocado-Price-Forecasting/assets/171478142/1a381fb2-2b71-4f5a-b61f-4e0ff4f681f4">

## Data and Methodology:

* **Data Acquisition and Cleaning:** Acquired and cleaned avocado price data from 2015 to 2018 for various US cities.
* **Exploratory Data Analysis (EDA):** Analyzed data distribution, identified missing values, and performed imputation. Split the data into training and testing sets.
* **Model Selection:** Evaluated ARIMA, Exponential Smoothing (SES), Holt-Winters, and Neural Network models based on Root Mean Square Error (RMSE) and Mean Absolute Percentage Error (MAPE) calculated with MLmetrics.
* **Model Training and Evaluation:** Trained models on the training set and evaluated performance on the testing set using MLmetrics.

## Results:

| Region      | Type    | Model                   | RMSE  | MAPE    |
|-------------|---------|-------------------------|-------|---------|
| California  | Organic | ARIMA                   | 0.183 | 10.02%  |
| California  | Organic | SES                     | 0.190 | 10.40%  |
| California  | Organic | Holt-Winters            | 0.199 | 11.00%  |
| California  | Organic | **Neural Network (nnetar)** | **0.177** | **8.45%**   |
| Syracuse    | Organic | ARIMA                   | 0.257 | 19.23%  |
| Syracuse    | Organic | **SES**                     | **0.083** | **4.28%**   |
| Syracuse    | Organic | Holt-Winters            | 0.197 | 13.08%  |
| Syracuse    | Organic | Neural Network (nnetar) | 0.272 | 20.46%  |

## Conclusion:

The study highlights the effectiveness of various time series models in forecasting avocado prices. The chosen models capture regional trends and provide valuable insights for market participants. By wielding the power of R and time series forecasting, this analysis empowers stakeholders in the avocado industry to navigate market fluctuations with greater confidence. The insights gleaned from this exploration can guide informed decisions and lead to a more prosperous avocado future.
