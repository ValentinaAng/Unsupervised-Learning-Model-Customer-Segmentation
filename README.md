# Title:
Unsupervised Machine Learning Project - Customer Segmentation

## Project Overview:

The Wholesale Customers dataset from the UCI Machine Learning Repository is used for analyzing customer segments based on annual spending on diverse product categories. This dataset is valuable for performing customer segmentation, which can help businesses tailor their marketing strategies, optimize inventory, and enhance customer satisfaction.


## About Dataset:

The dataset consists of 440 instances and includes the following features:

- `Channel:` Integer value representing the customer channel (1 for Horeca (Hotel/Restaurant/Cafe) and 2 for Retail).
- `Region:` Integer value representing the customer region (1 for Lisbon, 2 for Oporto, and 3 for Other).
- `Fresh:` Annual spending (m.u.) on fresh products.
- `Milk:` Annual spending (m.u.) on milk products.
- `Grocery:` Annual spending (m.u.) on grocery products.
- `Frozen:` Annual spending (m.u.) on frozen products.
- `Detergents_Paper:` Annual spending (m.u.) on detergents and paper products.
- `Delicassen:` Annual spending (m.u.) on delicatessen products.

## Table of Contents:
1. Preliminary Data Analysis
2. Exploratory Data Analysis
3. Data Preprocessing
4. Dimensionality Reduction (PCA)
5. K-Means, Agglomerative, DBScan Clustering
6. Results
7. Conclusion

## Important:
There are two notebooks uploaded.
`Notebook name: Unsupervised Learning-Customer Segmentation Project Cleaned` : This notebook is cleaned, doesn't contain outliers.
`Notebook name: Unsupervised Learning-Customer Segmentation Project-With Outliers` : This notebook is original, only scaler was applied.

## Results:

**From notebook 1:**
`K-Means Clustering`

| Results          |                     |
|------------------|---------------------|
| Best Score       | 0.5835959057118082 |
| Best Parameters  | {'n_clusters': 2, 'random_state': 42} |
| Number of Labels | 2                   |


`Agglomerative Clustering`

| Results          |                     |
|------------------|---------------------|
| Best Score       |  0.5835959057118082 |
| Best Parameters  | {'distance_threshold': None, 'linkage': 'ward', 'metric': 'euclidean', 'n_clusters': 2} |
| Number of Labels | 2                   |

`DBScan`

| Results          |                     |
|------------------|---------------------|
| Best Score       |  0.5835959057118082 |
| Best Parameters  | {'eps': 0.7000000000000001, 'min_samples': 1} |
| Number of Labels | 2                   |


**From notebook 2:** 

`K-Means Clustering`

| Results          |                     |
|------------------|---------------------|
| Best Score       | 0.7982              |            
| Best Parameters  | {'n_clusters': 2, 'random_state': 42} |
| Number of Labels | 2                   |

`Agglomerative Clustering`

| Results          |                     |
|------------------|---------------------|
| Best Score       |0.7987               |
| Best Parameters  | {'distance_threshold': None, 'linkage': 'average', 'metric': 'euclidean', 'n_clusters': 3} |
| Number of Labels | 3                  |

`DBScan`

| Results          |                     |
|------------------|---------------------|
| Best Score       |  0.8003             |
| Best Parameters  | {'eps': 0.5, 'min_samples': 2} |
| Number of Labels | 3                |

## Conclusion:

Data with Outliers: Retaining outliers in the dataset resulted in more meaningful and robust clustering outcomes.
Performance Metrics: The silhouette scores and cluster distributions were improved with the inclusion of outliers, indicating that the presence of these outliers provided additional valuable information for the clustering algorithms.

Based on our analysis, DBSCAN emerged as the best model for the dataset with outliers. This conclusion is supported by the fact that the Agglomerative Clustering dendrogram indicated that the optimal number of clusters is two. DBSCAN's performance, combined with this insight from the dendrogram, suggests that DBSCAN effectively handled the dataset with outliers and provided meaningful clustering results.
