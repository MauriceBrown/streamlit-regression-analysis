# Streamlit Regression Analysis App
A regression analysis tool using strealmit and statsmodels

[This dashboard is currently live on streamlit community cloud.](https://)

---
## Purpose

This app was created as an example of creating interactive statstical modelling software

---
## Using the app

Example data is available in the **Real estate valuation data set.csv** file in this repo. A description of the data available on the [UCI website](https://archive.ics.uci.edu/ml/datasets/Real+estate+valuation+data+set).

You can upload **your own** csv data as well as long as it has headers in the first row and contiguous column data (i.e. the same format as the "Real estate valuation data set.csv" file).

The dashboard is split into **three** sections and a sidebar

1. Data Exploration
    * This section is used to give a brief graphical overview of the variables in the uploaded file.
    * Data can be viewed as a bar chart, histogram, line chart or scatter plot
2. Model Output
    * This section shows the output from the specified regression model
3. Raw Data
    * A table containing the raw data from the uploaded csv file
4. Side bar containg filters in three sections
    1. The "Upload Data" section contains a file upload widget for uploading csv data files
    2. The "Data Exploration" section contains selection box controls for charting data from the uploaded csv file
    3. Model Specification allows you to select a dependent variable and a set of explanatory variables
        * Note 1: The dependent variable **must** be numerical, categorical variables are not allowed. If you have a categorical variable that is encoded numerically (e.g. a vector such as [1,1,2,1,3,1,2,3,3,3,2]) then the model will naively take that variable to be cardinal and run the regression accordingly.
        * Note 2: If your explanatory variable is categorical, dummies will be automatically created as long as there are **five or fewer** unique values.

---
## Potential Extensions
This app is by no means meant to be a complete statistical modelling package and can be exented to add any arbitrary additional functionality. Examples include:

1. Data exploration functionalty
    * additional chart types
    * plotting of multiple variables
    * faceted plotting of varaibles
2. Modelling functionalty
    * More detailed model output
    * Allowing for **multiple** dependent variables for SEM, path or VAR modelling etc
    * Adding different linear regression models (e.g. probit, quantile regression, lasso/ridge or other coeffieicnt constraint models)
    * Adding functionality for classification models (e.g. SVM, naive bayes, tree models, neural network classifiers etc)