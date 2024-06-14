# Flight Delay Prediction Analysis

## Table of Contents
1. Abstract
2. Introduction
3. Dataset Description
4. Literature Review
5. Exploratory Data Analysis
6. Modeling Techniques
7. Results and Discussions
8. Conclusions

## Abstract

This comprehensive flight delay prediction analysis dives into the complex world of aviation disruptions, meticulously examining diverse datasets comprising flight details, weather records, and operational metrics. Spanning sources like the Bureau of Transportation Statistics, FAA, and Weather Underground, the study dissects various factors contributing to delays, encompassing flight specifics, weather attributes, and airport operations. Leveraging techniques including ridge regression, XGBoost, and LSTM, the report aims to pre-empt and manage disruptions by delving into extensive data analysis and modeling. The project’s integrated approach scrutinizes vast datasets to unravel insights into mitigating disruptions and optimizing aviation operations, offering a roadmap to proactively address flight delays and enhance operational efficiency within the aviation industry. Through detailed analysis and predictive modeling, this study navigates through multifaceted data to unveil strategies for reducing disruptions and improving overall aviation performance.

## Dataset Description
This research delves into the realm of domestic commercial flights within the United States, analyzing data collected between January 2015 and August 2023. The information derives from reputable sources, namely the Bureau of Transportation Statistics and the Federal Aviation Administration. Focused on 45 key airports, the dataset encompasses comprehensive monthly reports from various airlines. It includes critical details such as flight times, airline specifics, origin and destination data, departure and arrival performance, cancellations, diversions, flight summaries, delay causes, available seat miles, daily flight operations, and staffing metrics. 

Supplementing this aviation data, weather information was sourced from Weather Underground, spanning a nine-year hourly record. This weather dataset includes significant attributes such as wind speed, humidity levels, weather conditions, atmospheric pressure, and dew point readings.

### Data Collection
To gather this wealth of data, a combination of scraping tools—Selenium and BeautifulSoup—was deployed. These tools were instrumental in extracting information from three primary sources: 
- [Bureau of Transportation Statistics](https://www.transtats.bts.gov)
- [FAA](https://www.aspm.faa.gov)
- [Weather Underground](https://www.wunderground.com)

Through these efforts, a comprehensive dataset was compiled, enabling an in-depth analysis of the intricate interplay between flight operations and meteorological conditions over an extended time span.

Analyzing existing research on flight delay prediction encompasses methodologies, data sources, and challenges in aviation. This review investigates predictive models, data features, and their impact, aiming to improve operational efficiency, passenger experience, and safety within the aviation industry.

## Modeling Techniques
### Regression Techniques
1. **Linear Regression**: A supervised machine learning algorithm for predicting a continuous target variable based on one or more independent features.
2. **Ridge Regression**: A regularization technique applied to linear regression, introducing a regularization term (L2 penalty) to prevent overfitting.

### XGBoost Technique
XGBoost is an ensemble learning algorithm combining predictions of multiple weak learners to produce a robust and accurate regression model, suitable for capturing intricate patterns in flight delay data.

### Long Short-Term Memory (LSTM)
LSTM, a type of recurrent neural network (RNN), effectively captures and remembers long-term dependencies in sequential data, making it suitable for flight delay prediction.

## Results and Discussions
### Metrics Used
1. **Mean Squared Error (MSE)**
2. **Mean Absolute Error (MAE)**
3. **R-Squared Score**

### Discussion
The LSTM model outperformed other algorithms, demonstrating its ability to learn and generalize complex temporal dependencies. Traditional regression models like Linear and Ridge Regression showed limitations in capturing intricate dynamics. XGBoost demonstrated commendable performance but was surpassed by LSTM.

### Feature Importance
Using an XGBoost model, significant features included ‘Carrier Code’, ‘Condition’, and ‘Scheduled Elapsed Time (Minutes)’. The prominence of ‘Carrier Code’ indicates potential bias due to market share variability among different airlines. Adverse weather conditions and longer flight durations also significantly influenced delays.
