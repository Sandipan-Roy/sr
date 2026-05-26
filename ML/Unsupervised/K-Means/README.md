# K-MEANS
K-Means clustering is a popular unsupervised machine learning algorithm that partitions unlabeled data into \(k\) distinct, non-overlapping clusters based on feature similarity. It works by minimizing the variance within clusters—calculating the distance between data points and central points called centroids.

## Key Aspects of K-Means Clustering:

- **Goal:** To group similar data points together, such as customer segmentation, image processing, and pattern discovery.
- **Iterative Process:** The algorithm starts by initializing \(k\) random centroids, then alternates between assigning points to the nearest centroid and re-calculating centroids until convergence.
- **Distance Metric:** Usually uses the Euclidean distance to measure the distance between a data point and the centroid.
        Distance = √(\(x_{i}\) - \(x_{c}\) )^2  + (\(y_{i}\) - \(y_{c}\) )^2
        Or
        Distance = sqrt(pow((\(x_{i}\) - \(x_{c}\) ), 2) + pow((\(y_{i}\) - \(y_{c}\) ), 2))
- **Choosing \(K\):** The optimal number of clusters (\(k\)) is often found using the "elbow method," which identifies the point where increasing \(k\) provides diminishing improvements to the model.
- **Limitations:** It can produce varying results depending on the initial centroid placement and may not handle outliers well.

## Steps of the K-Means Algorithm:

    1. Define Clusters: Choose the number of clusters (\(k\)).
    2. Initialize Centroids: Randomly place \(k\) centroids in the dataset.
    3. Assign Data Points: Assign each data point to the closest centroid.
    4. Update Centroids: Re-calculate the centroids by taking the average of all points in that cluster.
    5. Iterate: Repeat steps 3 and 4 until centroids no longer change.

The purpose of this is to create a concise workbook covering advanced skills in using NumPy, Pandas, Matplotlib, Seaborn and KMeans model uncovering insights, patterns, relationships within the data, performing Principal Component Analysis of data and ultimately creation of  clusters using KMeans Clustering model.

The repository consists of:

- **KMeans Clustering:** Clustering of passengers to provide insights from there behaviour pattern across different metrics:

    - To analyze and preprocess the dataset for effective model training.
    - To identify significant features influencing there behaviour pattern with the help of PCA.
    - To develop and train Machine Learning Clustering models using the dataset.
    - To evaluate the performance of the models using Silhouette Score.
    - To build a reliable clustering system that can assist the East West Airlines to track ROI by segment and adjust strategies.

    [Git Path: EastWestAirlines Dataset : An In-depth Examination using KMeans Clustering](https://github.com/Sandipan-Roy/sr/blob/Dev/ML/Unsupervised/K-Means/KMeans_SandipanRoy_1_20260427.ipynb)

- **Data:** This section comprises of 2 parts:

    - **raw:** consists of the input data or our entire dataset which we have used to train, validate and test our model.

        - [Git Path: Training Dataset](https://raw.githubusercontent.com/Sandipan-Roy/sr/refs/heads/Dev/ML/Unsupervised/K-Means/data/raw/EastWestAirlines.csv)

    - **output:** consists of the our customed model and the dataset along with Customer Clusters for this particular use case.

        - [Git Path: Model .pkl file](https://raw.githubusercontent.com/Sandipan-Roy/sr/refs/heads/Dev/ML/Unsupervised/K-Means/data/output/KMeans_model.pkl)
        - [Git Path: Output file](https://raw.githubusercontent.com/Sandipan-Roy/sr/refs/heads/Dev/ML/Unsupervised/K-Means/data/output/EastWestAirlines_CustomerClusters.csv)
