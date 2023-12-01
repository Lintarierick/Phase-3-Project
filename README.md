# Customer Churn Prediction

![SyriaTel, Kaggle](https://github.com/Lintarierick/Phase-3-Project/blob/main/bigml_59c28831336c6604c800002a.csv)


## Problem statement
In the telecommunications industry, customer churn poses a significant challenge to service providers, impacting revenue streams and hindering long-term sustainability. For Syria Tel, the need to proactively identify and address factors contributing to customer churn has never been more pressing. The problem at hand is twofold: the lack of a predictive model for customer churn and a limited understanding of the key drivers that influence customer decisions to terminate their services.

The project's aim is to:

Find the most significant predictors of churn to uncover meaningful patterns that can inform the likelihood of customer churn 
Create Machine Learning based predictive models that can show the likelihood of a customer leaving the services of Syriatel Company.
Inform of targeted preventive measures to retain customers.


## PROJECT OVERVIEW 
We will use the SyriaTel dataset available on Kaggle (https://www.kaggle.com/becksddf/churn-in-telecoms-dataset). The goal is to "build a classifier to predict whether a customer will ("soon") stop doing business with SyriaTel, a telecommunications company".

## BUSINESS UNDERSTANDING
In the telecommunications industry, customer churn poses a significant challenge to service providers, impacting revenue streams and hindering long-term sustainability. For Syria Tel, the need to proactively identify and address factors contributing to customer churn has never been more pressing. The problem at hand is twofold: the lack of a predictive model for customer churn and a limited understanding of the key drivers that influence customer decisions to terminate their services.

## Components

* **Jupyter Notebook**
The [Jupyter Notebook](https://github.com/Lintarierick/Phase-3-Project/blob/main/index.ipynb) is our key deliverable and contains details of our approach and methodology, data cleaning, exploratory data analysis and model building and validation.

I recommend using [nbviewer](https://nbviewer.org) to view the Jupyter Notebook.

* **Presentation**
The [presentation](https://) gives a high-level overview of our approach, findings and recommendations for non-technical stakeholders. It is aimed to be between 5 and 10 minutes long.

* **Data**

The dataset can be found in the file *bigml_59c28831336c6604c800002a.csv* in the Data folder, in this repository. It was obtained from Kaggle from this link( https://www.kaggle.com/becksddf/churn-in-telecoms-dataset)

## Technologies/ Packages

* Python version: 3.6.9
* Matplotlib version: 3.1.3
* Seaborn version: 0.9.0
* Pandas version: 0.25.1
* Numpy version: 1.16.5
* Scikit-learn version: 0.21.2  

## To get started

1. Clone this repository - [guidance](https://help.github.com/articles/cloning-a-repository/).
2. Dataset can be found on this link "https://www.kaggle.com/becksddf/churn-in-telecoms-dataset".
3. Check requirements in Technologies section above and download libraries if necessary.

## 1. Data Wrangling
Here we will work on data cleaning, handling missing values, data transformation, handling duplicates, data reshaping and other processes to ensure that we have a clean, structured, and suitable format for analysis and modeling

## 2. Exploratory Data Analysis (EDA)
Here we will explore the different features of the dataset to gain a better understanding of the data. We will use data visualization to uncover trends and patterns. 
    These insights suggest that certain customer behaviors and plan types are strong predictors of churn.
    Strong predictors of churn include "customer service calls", "international_plan" and "total_charges". 
**Overview of churn prediction features**
- Categorical features of churn include `state`, `international plan', 'churn', 'voice mail plan', and 'phone number'.
- Numerical variables include `account length`, `area code`, `total day minutes', 'total day calls', 'total day charge', total evening minutes', 'total evening calls', 'total evening charge', 'total night calls', 'total night minutes', 'total night charge', 'total intl calls', 'total intl charge', 'customer service calls '.                 `
- it can be noticed that as `total charges` increase, so does the risk of churn
- more customer service calls also point to increased likelihood of churn 

## 3. Baseline model: Logistic Regression Model
### Logistic Regression Results

The model exhibits strong predictive performance for the majority class ("False") with high precision (88%), recall (96%), and F1-Score (92%). However, it faces challenges in accurately predicting instances of the minority class ("True"), reflected in lower precision (48%), recall (21%), and F1-Score (29%). This indicates potential difficulties in correctly identifying customers who are likely to churn.

## 4. Iterative Model 1: KNN Model
### KNN Results
The KNN model achieves an accuracy of 87.89%, indicating its overall ability to correctly predict outcomes. In terms of precision, the model demonstrates a satisfactory ability to accurately identify customers who will churn, with a precision of 68%. However, the recall is relatively lower at 31%, suggesting that the model might not capture all instances of actual churn. The F1-score, a balance of precision and recall, is at 43%. The classification report shows that the model performs better in identifying non-churn instances ("False") than churn instances ("True").

## 5. Iterative Model 2: Tuned Logistic Regression Model
The final logistic regression model, tuned with the best hyperparameters identified through grid search, achieved an accuracy of approximately 74.82% on the test set.
While the final logistic regression model has a lower overall accuracy compared to the baseline logistic regression and the KNN models, it demonstrates improved performance in correctly identifying instances of the minority class ("True"). The F1-score for the "True" class is higher in the final logistic regression model, indicating better balance between precision and recall for churn instances.


## Conclusions
These insights suggest that certain customer behaviors and plan types are strong predictors of churn. Strong predictors of churn include "customer service calls", "international_plan" and "total_charges". Therefore, the segment of customers with international plans, higher total charges, and more customer service calls are at higher risk of churn. A higher number of international calls is associated with a lower likelihood of churn. The column "state_numeric" also plays a role, but the impact might depend on the specific states.
Although this model is reliable, it should be used in conjunction with other domain information for more precise prediction of customer churn.


## Contributor:
|Name     |  GitHub   |
|---------|-----------------|
|Erick Lintari|https://github.com/Lintarierick|
|
|






