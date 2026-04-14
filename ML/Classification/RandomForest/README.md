# RANDOM FOREST
Random Forest is a popular supervised machine learning algorithm that creates an "ensemble" of multiple decision trees, typically trained using the "bagging" method. By combining the predictions of many trees (via voting or averaging), it reduces individual tree overfitting and improves accuracy for both classification and regression tasks.

**Core Concept:**

The algorithm achieves its robustness through a technique called bagging (Bootstrap Aggregating) and feature randomness:

- Bootstrap Sampling: Each tree in the forest is trained on a random subset of the training data, sampled with replacement.
- Random Feature Selection: At every split in each tree, only a random subset of features is considered, ensuring that the trees are uncorrelated.
- Majority Voting: For a new input, every tree in the "forest" casts a vote for a class. The class with the most votes becomes the final prediction.

**Key Benefits:**

- Reduces Overfitting: By averaging many uncorrelated trees, it mitigates the tendency of a single decision tree to overfit its training data.
- Handles High Dimensionality: It performs well even with thousands of input variables without requiring feature deletion.
- Robustness: It is resilient to noise and can handle missing values effectively through internal estimation methods.
- Feature Importance: It provides built-in rankings of which features are most influential in making predictions.


The purpose of this is to create a concise workbook covering advanced skills in using NumPy, Pandas, Matplotlib, Seaborn and Decision Tree model uncovering insights, patterns, relationships within the data and classification of the class within the target variable using Random Forest Classification model.

The repository consists of:

- **Random Forest Classifier:** Classification analysis to provide insights into Water Quality:

    - To analyze and preprocess the water quality dataset for effective model training.
    - To identify significant features influencing water quality prediction.
    - To develop and train Machine Learning classification models using the training dataset.
    - To evaluate the performance of the models using appropriate evaluation metrics.
    - To build a reliable predictive system that can assist in the assessment of water quality.

    [Git Path: Insights into Water Quality: An In-depth Examination using Random Forest Classification](https://github.com/Sandipan-Roy/sr/blob/Dev/ML/Classification/RandomForest/DecisionTree_SandipanRoy_1_20260309.ipynb)

- **Data:** This section comprises of only 1 part:

    - **raw:** consists of the input data or our entire dataset which we have used to train, validate and test our model.

        - [Git Path: Training Dataset](https://raw.githubusercontent.com/Sandipan-Roy/sr/refs/heads/Dev/ML/Classification/RandomForest/data/raw/waterQuality1.csv)

    - **output:** consists of the our customed model for this particular use case.

        - [Git Path: Model .pkl file](https://raw.githubusercontent.com/Sandipan-Roy/sr/refs/heads/Dev/ML/Classification/RandomForest/data/output/random_forest_model.pkl)
