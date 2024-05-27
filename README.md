# Time Series Forecasting Analysis For Corporation Favorita ⏰

Welcome to the **Time Series Forecasting Project**. The aim is to predict store sales using data from Corporation Favorita, a major grocery retailer in Ecuador, using Machine Learning techniques.

![Python Version](https://img.shields.io/badge/Python-3.11-blueviolet)
![Data Analysis](https://img.shields.io/badge/Data-Analysis-blueviolet)
![Data Visualization](https://img.shields.io/badge/Data-Visualization-blueviolet)
![Hypothesis Testing](https://img.shields.io/badge/Hypothesis-Testing-blueviolet)
![Machine Learning](https://img.shields.io/badge/Machine-Learning-blueviolet)

## Preview 🔍`

Below is a preview showcasing some features of the notebook.

<div style="display: flex; align-items: center;">
    <div style="flex: 33.33%; text-align: center;">
        <p>Top</p>
        <img src="Images/Readmepics/Image1.png" alt="Top" width="90%"/>
    </div>
    <div style="flex: 33.33%; text-align: center;">
        <p>Middle</p>
        <img src="Images/Readmepics/Image2.png" alt="Middle" width="90%"/>
    </div>
    <div style="flex: 33.33%; text-align: center;">
        <p>Bottom</p>
        <img src="Images/Readmepics/Image3.png" alt="Bottom" width="90%"/>
    </div>
</div>


## Project Scenario
Every business aims to boost its revenue or profit margin, and one important area where industry participants concentrate their efforts is client retention. The majority of businesses in today’s machine learning environment use forecast models utilising time series analysis to determine how to handle client demand or prevent losses.

### Overview
Scenario: As a data scientist in Corporation Favorita, a large Ecuadorian-based grocery retailer. Corporation Favorita wants to ensure that they always have the right quantity of products in stock. To do this I have decided to build a series of machine learning models to forecast the demand of products in various locations. The marketing and sales team have provided you with some data to aid this endeavor. Your team uses CRISP-DM Framework for Data Science projects



## Project Description 📋

The primary focus of this project is to utilize time series regression analysis to forecast sales for Corporation Favorita, a prominent grocery retailer based in Ecuador.

### Project Ojectives
- Perform hypothesis testing to reject or fail to reject the null hypothesis
- Develop and train  build  models that more accurately predicts the unit sales for thousands of items sold at different Favorita stores.
- Evaluate the model's performance using appropriate metrics.
- Fine-tune the model parameters to optimize performance.

### Data for the project
The training data includes dates, store, and product information, whether that item was being promoted, as well as the sales numbers. Additional files include supplementary information that may be useful in building the models

### Data Dictionary

| **Dataset** | **Description** |
|------------|-----------------|
| train.csv  | Training data containing time series of features store_nbr, family, and onpromotion, as well as the target sales. |
|            | - `store_nbr`: Identifies the store where the products are sold. |
|            | - `family`: Identifies the type of product sold. |
|            | - `sales`: Total sales for a product family at a specific store on a given date (can be fractional). |
|            | - `onpromotion`: Total number of items in a product family that were being promoted at a store on a given date. |
| test.csv   | Test data with the same features as the training data. Predict target sales for these dates. |
| transaction.csv | Contains date, store_nbr, and transactions made on specific dates. |
| sample_submission.csv | Sample submission file in the correct format. |
| stores.csv | Store metadata, including city, state, type, and cluster. |
|            | - `cluster`: Grouping of similar stores. |
| oil.csv    | Daily oil price data, including values during both the train and test data timeframes. |
| holidays_events.csv | Holidays and events data, with metadata. |


### Business Sucess Criteria
1. Improved Inventory Management: Accurate sales predictions will enable Favorita to manage inventory levels efficiently.

2. Enhanced Resource Allocation: With precise sales forecasts, Favorita can allocate human resources and logistics more effectively, ensuring that stores have adequate staff and supplies to meet customer demand.

3. Marketing and Promotion Strategies: By understanding the impact of promotions on sales, Favorita can tailor its marketing strategies to boost sales during specific periods.

4. Optimized Financial Planning: Accurate sales predictions facilitate better financial planning and budgeting.

### Future Work
Deploy the model to be used in the company's mobile/web application

## `Hypotheses`

`Null Hypothesis`: The payment of wages in the public sector on the 15th and last days of the month does not influence store sales.

`Alternate Hypothesis`: The payment of wages in the public sector on the 15th and last days of the month significantly influences store sales.

## Results
alpha = 0.05
t-statistic: 0.4424065109693579
Critical t-value: 1.9613753699116634

Fail to reject the null hypothesis. There is no significant difference in average store sales between payday and non-payday days.


## ✍️Data Understanding
The data was pulled from the following various sources:
- data from a Github repository
- data from a OneDrive 
- data from a remote database

Data from the Github repository and SQL database data sets were used in this project for training and evaluation the machine
learning model while the last data set was used for testing the accuracy of the model.

Some additional tables acted as supplements for providing extrwa information

The major libraries used for this project were:
 1. Data manipulation: NumPy, pandas
 2. Data visualisation : Matplotlib, Seaborn, Plotly
 3. Machine learning methods : Sklearn, XGBoost, CatBoost, Linear Regression
 4. Statistical models : ARIMA, SARIMA


# 🏋️‍♀️Data cleaning

The first phase of the cleaning aspect checked for duplicates, nulls, mismatched columns, data coherency, datatypes and column names

There were some observations which included:

- null values present in the following columns: some dates were missing
- the datatype of date being strings or integers
- there are no duplicates in the concatenated stage

 
In general, not much cleaning was required for the dataset. Highlights of the cleaning process include:
 - Converting to the appropriate datatypes
 - Using the tools to fill in blank dates in order to maintain data coherency

The time series nature of this project necessitated a sequential approach for optimal efficiency. Consequently, traditional techniques did not apply to certain steps, such as filling in missing values or testing and training data for model construction.This is true of the models that are employed as well.




## Project Preview 🖼

The project includes the following stages:

### 1. 📥 Data Collection

- Azubi Africa's SQL Server database, GitHub repository and OneDrive.

N/B: The datasets from the sources above where saved in the root folder of this repository for easy access

### 2. 📚 Data Loading

- Utilizing `pyodbc` for SQL data
- Leveraging `pandas` for CSV and Excel files

### 3. 💡 Exploratory Data Analysis (EDA)

- Merging
- Duplicate checks
- Handling missing values
- Renaming Columns and Changing Datatypes
- Creating new features
- Visualizations
- Hypothesis testing
- ADF Testing

### 4. 📈 Answering Questions with Visualizations

**Questions:**

Visualisations were produced based on the analytical questions asked. These visuals were paramount to providing a solid foundation for analysising any trends or hitting patterns in analysing the factors contributing to churn analysis

 Business Questions
1. Is the train dataset complete (has all the required dates)?
2. Which dates have the lowest and highest sales for each year (excluding days the store was closed)?
3. Compare the sales for each month across the years and determine which month of which year had the highest sales.
4. Did the earthquake impact sales?
5. Are certain stores or groups of stores selling more products? (Cluster, city, state, type)
6. Are sales affected by promotions, oil prices and holidays?
7. What analysis can we get from the date and its extractable features?
8. Which product family and stores did the promotions affect.
9. What is the difference between RMSLE, RMSE, MSE (or why is the MAE greater than all of them?)
10. Does the payment of wages in the public sector on the 15th and last days of the month influence the store sales.

**Visualization Tools:**

- Matplotlib
- Seaborn

### 5. ⚙️ Feature Engineering

- Data Splitting
- Feature Encoding with OneHotEncoder
- Feature Scaling with MinMaxScaler

### 6. ⌛ Model Training

- Linear Regression
- XGBoost
- CatBoost
- AutoReg
- ARIMA
- SARIMA (was not utilised because of computational resources)

### 7. 📊 Model Evaluation

- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- Mean Squared Logarithmic Error (MSLE)
- Root Mean Squared Logarithmic Error (RMSLE)

### 8. 🎯 Hyperparameter Tuning

- RandomSearchCV

### 9. 🤔 Prediction on Validation Set

### 10. 📒 Prediction on Test Dataset

### 11. 💭 Exportation

- os
- pickle
- save_model

## 👀Observations

CatBoost outperforms the other models across all metrics, making it the best choice for your dataset. It produces the most accurate predictions with the smallest errors

## Installation and Setup 🔧

To get started with this project, you'll need to install the following Python packages using `pip`:

```bash
pip install pyodbc sqlalchemy lightgbm catboost python-dotenv pandas numpy matplotlib seaborn scipy pmdarima
```

Make sure to have these packages installed before running the project.
Follow these steps for installation:

1. Clone this repository to your local machine.
2. Install the required Python packages using pip:
   ```bash
   pip install -r requirements.txt
   ```

You're now ready to dive into this exciting data journey!

## Author 👨‍💼

This project was built by **Prince Acquah Rockson**.

Here are his details:



| Detail | Link |
| ------ | ---- |
| Email | parockson@gmail.com or prockson@outlook.com |
| LinkedIn | [Prince Acquah Rockson](https://www.linkedin.com/in/prince-acquah-rockson/) |
| GitHub | [parockson](https://github.com/parockson) |
| Medium | [parockson](https://medium.com/@parockson) |`


## Article Publication 📄

I went further to explain the work process of this project in an article published on Medium. Click on this link to find the article: [TIME SERIES FORECASTING ANALYSIS FOR CORPORATION FAVORITA](medium.com/@parockson/time-series-analysis-3d3bcdb5db5c).



## License

The MIT Licence governs the use of this project. Details can be found in the LICENCE file.

## Acknowledgments 🙏

I would like to express my gratitude to the [Azubi Africa Data Analyst Program](https://www.azubiafrica.org/data-analytics) for offering valuable projects as part of this program. Not forgeting my scrum master [Rachel Appiah-Kubi](https://www.linkedin.com/in/racheal-appiah-kubi/) & CTA [Foster Nana Kwabena Abrefa
 ](https://www.linkedin.com/in/foster-nana-kwabena-abrefa-3b917b34/) for their support throughout this program.

## Contact

Reviews, questions, comments, and requests for collaboration may be sent to parockson@gmail.com or prockson@outlook.com.
