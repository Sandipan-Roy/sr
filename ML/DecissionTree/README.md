# DECISION TREE
A decision tree is a widely used, transparent supervised machine learning algorithm that uses a flowchart-like structure to make predictions for both classification (predicting categories) and regression (predicting numerical values) tasks. The algorithm uses a top-down, greedy approach called recursive partitioning to build the tree. It selects the best feature to split data using metrics like Information Gain or Gini Index. This process repeats for sub-nodes until a stopping condition is reached (e.g., maximum depth), at which point leaf nodes are assigned predicted values.The mathematical core of a Decision Tree lies in Information Theory, specifically in how it measures "purity" to decide where to split data. The goal is to start with a mixed (impure) set of data and split it into subsets that are as pure as possible.To build a tree, the algorithm must first quantify the disorder in a node. There are two primary ways to do this:

- **Entropy:** Entropy (**H**) measures the amount of uncertainty or randomness in a dataset.

                H(S) =    $ - \sum_{i=1}^{c} p_i*log_2(p_i) $

            - **S:** The current dataset.
            - **c:** The number of classes.
            - **pi:** The proportion of samples belonging to class 

- **Gini Impurity:** Gini (**G**) measures the probability of a randomly chosen element being incorrectly classified.

                    $      1 - \sum_{i=1}^{c} {p^2}_i      $

A pure node has a Gini index of 0. It is computationally faster than Entropy because it avoids logarithmic calculations. 


The purpose of this is to create a concise workbook covering advanced skills in using NumPy, Pandas, Matplotlib, Seaborn and Decision Tree model uncovering insights, patterns, relationships within the data and classification of the class within the target variable using Decision Tree Classification model.

The repository consists of:

- **Decision Tree on excel:** Decision Tree Classification implementation over an excel file.
[Git Path: Excel](https://github.com/Sandipan-Roy/sr/blob/Dev/ML/DecissionTree/DTree.xlsx)

- **Decision Tree Classification:** Classification analysis to predict the likelihood of heart disease using structured clinical data. The main objectives of this project are:

    - To analyze and preprocess the heart disease dataset for effective model training.
    - To identify significant clinical features influencing heart disease prediction.
    - To develop and train Machine Learning classification models using the training dataset.
    - To evaluate the performance of the models using appropriate evaluation metrics.
    - To build a reliable predictive system that can assist in early detection of heart disease.

    [Git Path: Heart Attack Analysis & Prediction using Decision Tree Classification](https://github.com/Sandipan-Roy/sr/blob/Dev/ML/DecissionTree/DecisionTree_SandipanRoy_1_20260309.ipynb)

- **Data:** This section comprises of 2 parts:

    - **raw:** consists of the input data or our entire dataset which we have used to train, validate and test our model.

        - [Git Path: Training Dataset](https://raw.githubusercontent.com/Sandipan-Roy/sr/refs/heads/Dev/ML/DecissionTree/data/raw/heart_disease_train.csv)
        - [Git Path: Test Dataset](https://raw.githubusercontent.com/Sandipan-Roy/sr/refs/heads/Dev/ML/DecissionTree/data/raw/heart_disease_test.csv)

    - **output:** consists of those data, predicted data/outcome and/or model.pkl files which we have generated during the entire journey for each projects.

        - [Git Path: Predicted Data](https://raw.githubusercontent.com/Sandipan-Roy/sr/refs/heads/Dev/ML/DecissionTree/data/output/heart_disease/heart_disease_predictions.csv)
        - [Git Path: Model .pkl file](https://raw.githubusercontent.com/Sandipan-Roy/sr/refs/heads/Dev/ML/DecissionTree/data/output/heart_disease/decision_tree_model.pkl)
