# LOGISTIC REGRESSION
Logistic regression is a supervised machine learning algorithm primarily used for classification tasks. Unlike linear regression, which predicts continuous numbers. Unlike linear regression, which predicts continuous numbers, logistic regression predicts the probability that an input belongs to a specific category.The algorithm takes a linear combination of input features and "squashes" the result into a range between 0 and 1 using the sigmoid function(also knwon as logistic function)The sigmoid function, also known as the standard logistic function, is defined by the following mathematical formula: 
            (\(Z = 1 / (1 + e^(-y))\))  
                where (\(y=aX+b\))

The purpose of this is to create a concise workbook covering advanced skills in using NumPy, Pandas, Matplotlib, Seaborn and Linear Regression model uncovering insights, patterns, relationships within the data and predicting the target variable using Logistic Regression model.

The repository consists of:

- **LR on excel:** Logistic Regression implementation over an excel file.
[Git Path: Excel](https://github.com/Sandipan-Roy/sr/blob/Dev/ML/Regression/Logistic_Regression/Logistic%20Regression.xlsx)
- **Logistic Regression:** Regression analysis on Classification of the type of dry beans. The purpose of the notebook is to identify different types of dry beans based on the given features. We've kept the dataset within [Git Path: Dry Beans Dataset](https://raw.githubusercontent.com/Sandipan-Roy/sr/refs/heads/Dev/ML/Regression/Logistic_Regression/data/raw/Dry_Bean_Dataset.csv) and used it in our notebook from the same location. Apart from the above, we have created one .csv file and .pkl file during data wrangling which can be found inside [Git Path: Data-Output](https://raw.githubusercontent.com/Sandipan-Roy/sr/refs/heads/Dev/ML/Regression/Logistic_Regression/data/output).
[Git Path: Classification of the type of dry beans by using Logistic Regression](https://github.com/Sandipan-Roy/sr/blob/Dev/ML/Regression/Logistic_Regression/LogisticRegression_SandipanRoy_1_20260225.ipynb)