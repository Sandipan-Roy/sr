# Hierarchical Clustering
Hierarchical clustering is an unsupervised machine learning algorithm that groups data points into a nested hierarchy of clusters based on their similarities. It builds a tree-like structure called a dendrogram to visualize these relationships, meaning you do not need to pre-define the number of clusters.

## The Two Main Approaches

There are two primary methods for building a hierarchical cluster tree:

    - **Agglomerative (Bottom-Up):** Starts with every single data point as its own individual cluster. The algorithm iteratively finds the closest pairs of clusters and merges them together until only one giant cluster remains.

    - **Divisive (Top-Down):** Starts by treating the entire dataset as a single large cluster. It then iteratively splits clusters into smaller, dissimilar groups until every data point is isolated into its own cluster.

## How Agglomerative Clustering Works

    - **Compute Distances:** Calculate a distance (or similarity) matrix for all pairs of data points using metrics like Euclidean distance or Manhattan distance

    - **Assign Clusters:** Treat each data point as its own distinct cluster

    - **Merge and Update:** Find the two closest clusters and merge them into one. Recalculate the distances between the newly formed cluster and all remaining clusters

- Repeat: Repeat the process of merging the closest pairs until all points belong to a single cluster

## Linkage Methods

When clusters contain multiple data points, the algorithm needs a rule to determine how distance is calculated between them. Common linkage criteria include:

    - **Single Linkage:** The distance between the two closest members of different clusters.

    - **Complete Linkage:** The distance between the two farthest members of different clusters.
    
    - **Average Linkage:** The average of all distances between members of one cluster and members of another.

    - **Ward’s Method:** Minimizes the variance within each merged cluster, often producing tightly knit, evenly sized groups

## The Dendrogram and Cutting the Tree

The results of hierarchical clustering are best understood using a dendrogram. The vertical branches represent the distance at which clusters are merged.

To create flat clusters for real-world use, you "cut" the dendrogram horizontally at a chosen height or distance. The number of vertical lines your cut intersects equals your final number of clusters.

## Use Cases and Considerations

    - **Use Cases:** Ideal for grouping genes in bioinformatics, customer segmentation in marketing, building taxonomies in biology, and document classification.

    - **Pros:** Does not require you to guess the number of clusters in advance; intuitive visualizations via dendrograms.

    - **Cons:** High computational cost (O(n³) complexity for standard algorithms), making it inefficient for massive datasets without optimizations like BIRCH.


The purpose of this is to create a concise workbook covering advanced skills in using NumPy, Pandas, Matplotlib, Seaborn and KMeans model uncovering insights, patterns, relationships within the data, performing Principal Component Analysis of data and ultimately creation of clusters using Hierarchical Clustering model.

The repository consists of:

- **Hierarchical Clustering Algorithm:** The goal is to develop a customer segmentation to define marketing strategy using Hierarchical Clustering algorithm from there behaviour pattern across different metrics:

    - To analyze and preprocess the dataset for effective model training.
    - To identify significant features influencing there behaviour pattern with the help of PCA.
    - To develop and train Machine Learning Clustering models using the dataset.
    - To evaluate the performance of the models using Silhouette Score.
    - To build a reliable clustering system that can assist the East West Airlines to track ROI by segment and adjust strategies.

    [Git Path: EastWestAirlines Dataset : An In-depth Examination using Hierarchical Clustering](https://github.com/Sandipan-Roy/sr/blob/Dev/ML/Unsupervised/Hierarchical/Hierarchical_SandipanRoy_1_20260504.ipynb)

- **Data:** This section comprises of 2 parts:

    - **raw:** consists of the input data or our entire dataset which we have used to train our model.

        - [Git Path: Training Dataset](https://raw.githubusercontent.com/Sandipan-Roy/sr/refs/heads/Dev/ML/Unsupervised/Hierarchical/data/raw/CC_GENERAL.csv)

    - **output:** consists of the our customed model and the dataset along with Customer Clusters for this particular use case.

        - [Git Path: Model .pkl file](https://raw.githubusercontent.com/Sandipan-Roy/sr/refs/heads/Dev/ML/Unsupervised/Hierarchical/data/output/Hierarchical_model.pkl)
        - [Git Path: Output file](https://raw.githubusercontent.com/Sandipan-Roy/sr/refs/heads/Dev/ML/Unsupervised/Hierarchical/data/output/CreditCard_CustomerClusters.csv)