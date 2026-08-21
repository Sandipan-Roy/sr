# DBSCAN Clustering
DBSCAN (Density-Based Spatial Clustering of Applications with Noise) is an unsupervised machine learning algorithm that groups densely packed data points together. Unlike algorithms like K-Means, DBSCAN identifies clusters of arbitrary shapes and automatically detects outliers/noise. It groups data points based on their local density. It defines clusters as dense regions separated by areas of lower density and intelligently identifies isolated points as noise/outliers.

## Key Concepts & Parameters

The algorithm relies on two primary parameters that you define before training:

- **Epsilon (ε, eps):** The maximum radius used to define the neighborhood around a data point.
- **MinPts (min_samples):** The minimum number of data points required to fall within the ε radius for a region to be considered "dense".

## How the Points are Categorized

Based on the two parameters, DBSCAN classifies every data point into one of three categories:

- **Core Point:** A point that has at least the specified MinPts within its ε radius.
- **Border Point:** A point that is not a core point itself (does not have enough neighbors), but falls within the ε radius of a core point.
- **Noise (Outlier):** Any point that is neither a core nor a border point.

## How the Algorithm Works

- **Identify Core Points:** The algorithm scans the dataset and marks all points with at least MinPts neighbors within their ε radius as core points.
- **Form Clusters:** It picks an unvisited core point and starts a new cluster. It then recursively adds all other core points and border points that are "density-connected" (within reach of each other) to this cluster.
- **Repeat:** The process is repeated until all core points are assigned to clusters.
- **Flag Noise:** All remaining unvisited points that do not belong to any cluster are labeled as noise

## Why Use DBSCAN?

- **No assumption of shape:** Clusters aren't restricted to circles or spheres.
- **Noise handling:** It separates outliers automatically instead of forcing them into a cluster.
- **No need to define the number of clusters (k):** It learns the number of clusters directly from the data density.

## Primary Use Cases

- **Geospatial and GPS Analysis:** Widely used by ride-sharing or logistics companies to group GPS coordinates for delivery points, establish service zones, or optimize fleet routing without relying on rigid geometric boundaries.
- **Anomaly Detection:** Because DBSCAN leaves scattered points unassigned, it is highly effective for flagging credit card fraud, cyber intrusions, or network attacks that deviate from normal transaction clusters.
- **Image Segmentation:** Used to group pixels by color and intensity to identify objects in computer vision when objects do not conform to simple, spherical shapes.
- **Customer Segmentation with Outliers:** Unlike centroid-based methods (like K-Means), DBSCAN does not force every customer into a group. It identifies core, high-density market segments while cleanly isolating fringe buyers.
- **Biological and Medical Data:** Identifying gene expression patterns or disease outbreaks that cluster naturally in irregular shapes.

## Key Considerations and Limitations

- **The "Curse of Dimensionality":** DBSCAN’s performance severely degrades on high-dimensional data. You may need to perform dimensionality reduction (such as PCA or UMAP) before clustering
- **Varying Density Challenges:** Because the neighborhood radius ε (Epsilon) and the minimum points MinPts are constant, DBSCAN struggles with datasets where clusters have significantly different densities. It may merge separate clusters or wrongly classify parts of a sparse cluster as noise.
- **Parameter Sensitivity:** Results are highly dependent on the choice of ε and MinPts. Selecting an improper ε can result in either all points being classified as noise or all points merging into a single cluster.
- **Computational Cost:** The worst-case time complexity is \(\mathcal{O}(N^2)\) unless spatial indexing trees are utilized, which makes it computationally expensive for massive datasets.
- **Feature Scaling:** Like many distance-based algorithms, DBSCAN is heavily affected by the scale of your variables; features must be properly normalized or standardized beforehand.

The purpose of this is to create a concise workbook covering advanced skills in using NumPy, Pandas, Matplotlib, Seaborn and KMeans model uncovering insights, patterns, relationships within the data, performing Principal Component Analysis of data and ultimately creation of clusters using DBSCAN Clustering model.

The repository consists of:

- **DBSCAN Clustering Algorithm:** The goal is to develop a customer segmentation to define marketing strategy using DBSCAN Clustering algorithm from there behaviour pattern across different metrics:

    - To analyze and preprocess the dataset for effective model training.
    - To identify significant features influencing there behaviour pattern with the help of PCA.
    - To develop and train Machine Learning Clustering models using the dataset.
    - To evaluate the performance of the models using Silhouette Score.
    - To build a reliable clustering system that can assist the East West Airlines to track ROI by segment and adjust strategies.

    [Git Path: Customer Personality Analysis : An In-depth Analysis of company's ideal customers using DBSCAN Clustering](https://github.com/Sandipan-Roy/sr/blob/Dev/ML/Unsupervised/DBSCAN/DBSCAN_SandipanRoy_20260511.ipynb)

- **Data:** This section comprises of 2 parts:

    - **raw:** consists of the input data or our entire dataset which we have used to train our model.

        - [Git Path: Training Dataset](https://raw.githubusercontent.com/Sandipan-Roy/sr/refs/heads/Dev/ML/Unsupervised/DBSCAN/data/raw/marketing_campaign.csv)

    - **output:** consists of the our customed model and the dataset along with Customer Clusters for this particular use case.

        - [Git Path: Model .pkl file](https://raw.githubusercontent.com/Sandipan-Roy/sr/refs/heads/Dev/ML/Unsupervised/DBSCAN/data/output/DBSCAN_model.pkl)
        - [Git Path: Output file](https://raw.githubusercontent.com/Sandipan-Roy/sr/refs/heads/Dev/ML/Unsupervised/DBSCAN/data/output/Customer_Personality_Analysis.csv)