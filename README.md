# DBSCAN Clustering on Synthetic Data

## Problem Statement and Goal of Project

The goal of this project is to demonstrate the application of the **DBSCAN (Density-Based Spatial Clustering of Applications with Noise)** algorithm for clustering synthetic data. The primary objective is to show how the model works, understand its parameters, and evaluate clustering performance beyond merely optimizing for the best scores. It focuses on hands-on exploration and understanding of clustering techniques, particularly for non-linear, real-world data with noise.

## Solution Approach

1. **Data Generation**:

   * Synthetic data is generated using `make_blobs` to simulate multiple clusters with varying densities.
   * The data is standardized using `StandardScaler` to ensure consistency in the scale across the dimensions.

2. **Clustering with DBSCAN**:

   * The **DBSCAN** algorithm is applied with the parameters `eps=0.2` (maximum distance for two points to be considered neighbors) and `min_samples=7` (minimum number of points required to form a dense region).
   * Clustering results are generated with labeled clusters and noise points.

3. **Visualization**:

   * The clusters are visualized using **matplotlib**, with noise points displayed in black.
   * Core points are marked distinctively to differentiate between dense regions and outliers.

4. **Evaluation Metrics**:

   * **Silhouette Score**: Assesses how similar each data point is to its own cluster compared to other clusters.
   * **Calinski-Harabasz Score**: Measures the ratio of between-cluster dispersion to within-cluster dispersion.
   * **Davies-Bouldin Score**: Evaluates the similarity between clusters, where a lower score indicates better clustering performance.

   These metrics are calculated to demonstrate the model's effectiveness and to analyze the clustering results.

## Technologies & Libraries

* **Python** 3.x
* **Libraries**:

  * `numpy`: For numerical operations
  * `matplotlib`: For plotting and visualizing data clusters
  * `sklearn`: For generating synthetic data, clustering with DBSCAN, and calculating evaluation metrics

## Description about Dataset

The dataset consists of 1500 data points generated using **`make_blobs`** from Scikit-learn. The points are distributed across four centers in a 2D space, each representing a cluster. The clusters have different densities, and noise points are included in the dataset to simulate real-world scenarios where data is not perfectly structured.

## Installation & Execution Guide

### Requirements

Ensure you have Python 3.x and the following packages installed:

```bash
pip install numpy matplotlib scikit-learn
```

### Steps to Run

1. Clone the repository or download the notebook.
2. Open the notebook (`dbscan.ipynb`) in a Jupyter environment or any Python IDE.
3. Execute the cells in sequence to generate the synthetic data, apply DBSCAN, and evaluate the results.

### Running the Notebook

The notebook includes:

* Data generation and preprocessing
* Application of DBSCAN with specified parameters
* Visualization of clusters and noise points
* Evaluation of clustering performance using the Silhouette, Calinski-Harabasz, and Davies-Bouldin scores.

## Key Results / Performance

* **Silhouette Score**: Measures the quality of clustering, with a higher score indicating better-defined clusters.
* **Calinski-Harabasz Score**: A higher score suggests better separation between clusters.
* **Davies-Bouldin Score**: Lower values indicate better clustering, with values closer to zero indicating perfect clustering.

These metrics are crucial for understanding how well DBSCAN has clustered the data, identifying noise, and determining the right parameter settings.

## Screenshots / Sample Outputs

* The generated synthetic data points are visualized in a scatter plot, showing the clusters and noise points.
* Metrics such as Silhouette, Calinski-Harabasz, and Davies-Bouldin scores are displayed as output.

## Additional Learnings / Reflections

This project goes beyond just achieving high evaluation metrics; it demonstrates a deep understanding of the DBSCAN algorithm and how its parameters (`eps`, `min_samples`) affect clustering outcomes. By exploring how DBSCAN handles different data distributions and noise levels, the project showcases the practical application of clustering algorithms in real-world data scenarios. The evaluation metrics provide a thorough analysis of clustering performance, emphasizing the importance of tuning the algorithm and understanding its behavior.

## 👤 Author

## Mehran Asgari

## **Email:** [imehranasgari@gmail.com](mailto:imehranasgari@gmail.com).

## **GitHub:** [https://github.com/imehranasgari](https://github.com/imehranasgari).

---

## 📄 License

This project is licensed under the Apache 2.0 License – see the `LICENSE` file for details.

---

💡 *Some interactive outputs (e.g., plots, widgets) may not display correctly on GitHub. If so, please view this notebook via [nbviewer.org](https://nbviewer.org) for full rendering.*

