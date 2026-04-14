# Call Center Efficiency Analysis

## 📌 Objective
The goal is to assist supervisors in identifying inefficient operators, taking into account factors such as the number of calls, wait times, and whether outbound calls are being made.

# Technologies used
## Python | Pandas | SQL | Tableau | NumPySciPy | Matplotlib | Seaborn | Plotly | Statistical Analysis

# 🧩 Dataset structure
### The compressed dataset 'telecom_dataset_us.csv' contains the following columns:

- 'user_id': Customer account ID
- 'date': Date on which the statistics were retrieved
- 'direction': Call "direction" (`out` for outgoing, `in` for incoming)
- 'internal': Whether the call was internal (between a customer's operators)
- 'operator_id': Operator identifier
- 'is_missed_call': Whether it was a missed call
- 'calls_count': Number of calls
- 'call_duration': Call duration (excluding wait time)
- 'total_call_duration': Call duration (including wait time)
  
### The compressed dataset 'telecom_clients_us.csv' contains the following columns:

- 'user_id': User ID
- 'tariff_plan': Current client tariff plan
- 'date_start': Client registration date

## 📎 Process 
### Data Preprocessing: 
The data was cleaned and standardized, eliminating inconsistencies and verifying the absence of duplicates and missing values.
Exploratory Data Analysis (EDA): Call records were analyzed, focusing on call volume, duration (both including and excluding hold time), and inbound versus outbound calls. Based on this analysis, KPIs were established to define the criteria for inefficiency.
Clustering: A Mann-Whitney U test was performed, as it is well-suited for datasets exhibiting high dispersion.


## 📌 Insights
The established criteria resulted in a significant number of inefficient users. Inefficient Users (< 2,000 outgoing calls): 176 (79.3%); Efficient Users (≥ 2,000 outgoing calls): 46 (20.7%). Furthermore, the results of the statistical test indicated that the null hypothesis is rejected, as its significance level is very high.


