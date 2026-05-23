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

