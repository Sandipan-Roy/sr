# BOOSTING ALGORITHMS
Boosting is an ensemble learning method that improves a model's predictive power by combining several weak learners (simple models that perform only slightly better than random guessing) into a single strong learner.
Unlike bagging (like Random Forests), which builds models in parallel, boosting builds them sequentially.

**Core Concept:**

- Equal Weighting: Initially, all data points in the training set are given equal importance.
- Sequential Learning: A base model (the first weak learner) is trained on the data.
- Error Correction: The algorithm identifies misclassified data points or calculates residuals (errors).
- Weight Adjustment: Subsequent models are trained with a higher focus on these difficult-to-predict examples.
- Aggregation: All individual weak learners are combined—often via a weighted average—to produce the final high-accuracy prediction.

**Common Boosting Algorithms:**

- AdaBoost (Adaptive Boosting): Adjusts weights of misclassified samples after each round so the next model prioritizes them. It is often used with "decision stumps" (single-level trees).
- Gradient Boosting (GBM): Instead of changing sample weights, it trains new models to predict the residuals (errors) of the previous ensemble using gradient descent to minimize a loss function.
- XGBoost (eXtreme Gradient Boosting): An optimized, scalable version of gradient boosting that includes XGBoost regularization to prevent overfitting and supports parallel processing.

**Key Benefits Vs Limitations:**

- Bias Reduction:
    - ***Benefit*** Effectively reduces bias, making it great for underfitting models.
    - ***Limitation*** High risk of overfitting if the data is noisy or the number of iterations is too high.
- Accuracy:
    - ***Benefit*** Often provides higher accuracy than bagging or single models.
    - ***Limitation*** Computationally intensive due to the sequential nature (cannot be easily parallelized like bagging).
- Handling Outliers:
    - ***Benefit*** Can prioritize hard cases.
    - ***Limitation*** Highly sensitive to outliers because it keeps trying to "fix" the error for extreme values.


The purpose of this is to create a concise workbook covering advanced skills in using NumPy, Pandas, Matplotlib, Seaborn and Decision Tree model uncovering insights, patterns, relationships within the data and classification of the class within the target variable using AdaBoost, Gradient Boosting and XGBoost Classification model.

The repository consists of:

- **Boosting Classifier:** Classification analysis to provide insights into Brain Stroke dataset

    [Git Path: Insights into Water Quality: An In-depth Examination using Boosting Classification](https://github.com/Sandipan-Roy/sr/blob/Dev/ML/Classification/Boosting/Boosting_SandipanRoy_1_20260326.ipynb)

- **Data:** This section comprises of 2 parts:

    - **raw:** consists of the input data or our entire dataset which we have used to train, validate and test our model.

        - [Git Path: Training Dataset](https://raw.githubusercontent.com/Sandipan-Roy/sr/refs/heads/Dev/ML/Classification/Boosting/data/raw/brain_stroke.csv)

    - **output:** consists of the our customed model for this particular use case.

        - [Git Path: Model .pkl file](https://raw.githubusercontent.com/Sandipan-Roy/sr/refs/heads/Dev/ML/Classification/Boosting/data/output/brain_stroke_model.pkl)
