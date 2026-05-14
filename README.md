# Abnormal\-Futures\-Dataset

A high\-frequency futures trading dataset with abnormal labels, designed to support research on futures market anomaly detection, quantitative trading strategy development, and market behavior analysis\. The dataset provides comprehensive trading information with clear abnormal markers, enabling researchers and developers to conduct in\-depth studies on market irregularities\.

## Dataset Overview

This dataset contains high\-frequency trading data of futures, including key trading indicators and manually/algorithmically labeled abnormal flags\. It is suitable for tasks such as anomaly detection model training, market risk assessment, and quantitative strategy verification\. The data is structured in a standardized format, easy to load and process with common data analysis tools \(e\.g\., Python, R\)\.

## Dataset Structure

The dataset includes two CSV files \(`High\-frequency futures\.csv` and `futures2\.csv`\) with the following fields \(consistent across all files\):

|Field Name|Description|Data Type|
|---|---|---|
|Time|Trading time, recorded in a standardized datetime format \(e\.g\., YYYY\-MM\-DD HH:MM:SS\), ensuring accurate time sequence alignment\.|Datetime|
|Open|Opening price of the futures contract at the corresponding trading time, representing the first transaction price of the period\.|Float|
|High|Highest price of the futures contract during the corresponding trading period\.|Float|
|Low|Lowest price of the futures contract during the corresponding trading period\.|Float|
|Close|Closing price of the futures contract at the end of the corresponding trading period, representing the last transaction price of the period\.|Float|
|Volume|Trading volume during the corresponding period, representing the total number of futures contracts traded\.|Integer|
|Amount|Trading amount during the corresponding period, representing the total value of futures contracts traded \(calculated as price × volume\)\.|Float|
|Open Interest|Open interest of the futures contract at the corresponding trading time, representing the total number of outstanding contracts that have not been closed or delivered\.|Integer|
|Abnormal|Abnormal flag, marked as 1 \(abnormal\) or 0 \(normal\)\. The flag is determined based on market irregularities such as abnormal price fluctuations, abnormal trading volume, or other abnormal market behaviors\.|Integer \(0/1\)|

## Data Features

- **High Frequency**: The dataset provides high\-frequency trading data, capturing real\-time market changes and facilitating the analysis of short\-term market anomalies\.

- **Complete Indicators**: Covers core trading indicators \(OHLC, volume, amount, open interest\) and abnormal labels, providing comprehensive data support for multi\-dimensional analysis\.

- **Standardized Format**: The CSV format is compatible with most data analysis tools, and the datetime and numerical fields are standardized to avoid data cleaning difficulties\.

- **Clear Anomaly Markers**: The \&\#34;Abnormal\&\#34; field provides explicit labels, enabling direct use for supervised learning tasks such as anomaly detection model training and validation\.

## Usage Guidelines

### Loading the Dataset \(Python Example\)

```python
import pandas as pd

# Load the dataset
df = pd.read_csv("High-frequency futures.csv")

# Check data structure
print(df.info())

# Check basic statistics
print(df.describe())
```

### Anomaly Detection Use Case

The dataset can be used to train machine learning models \(e\.g\., LSTM, Isolation Forest, SVM\) for futures market anomaly detection\. The \&\#34;Abnormal\&\#34; field serves as the target variable, and other fields serve as feature variables to build prediction models\.

## Notes

- The trading time is in the local time zone; please adjust the time format according to your research needs if necessary\.

- The abnormal labels are generated based on predefined market rules and algorithmic detection; users can adjust the label standards according to specific research scenarios\.

- Please ensure that the dataset is used for academic research or legitimate commercial purposes only, and abide by relevant data usage regulations\.

## Contact

For questions, suggestions, or data updates, please contact the repository owner via GitHub Issues or the associated email\.
