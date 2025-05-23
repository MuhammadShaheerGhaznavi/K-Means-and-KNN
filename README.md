# K-Means and KNN for Cell Type Annotation

This repository contains an implementation of **K-Means Clustering** and **K-Nearest Neighbors (KNN)** for **Cell Type Annotation**. The script `pa1_task.py` is designed to process biological data, cluster it into meaningful groups, and classify cell types based on their features.

## Overview

The script implements two key machine learning algorithms:

1. **K-Means Clustering**: Used to group cells into clusters based on their protein abundance profiles.
2. **K-Nearest Neighbors (KNN)**: Used to classify cells into predefined types based on labeled training data.

The file includes modular functions for clustering and classification, making it reusable for various datasets.

---

## Key Functions and Methods

### 1. **`k_means_split(abundance_matrix)`**
   - **Purpose**: Performs K-Means clustering on the input data to split clusters and assign labels.
   - **Key Steps**:
     - Calculates Euclidean distances between data points and centroids.
     - Updates centroids by splitting clusters and reassigning data points.
   - **Parameters**:
     - `abundance_matrix` (numpy array): Input data matrix where rows represent cells and columns represent protein abundances.
   - **Returns**:
     - `centroids` (numpy array): Updated centroids after clustering.
     - `labels` (numpy array): Cluster labels assigned to each cell.

---

### 2. **`calculate_euclidean_distance(centroids, abundance_matrix)`**
   - **Purpose**: Computes the Euclidean distance between each data point and the centroids.
   - **Parameters**:
     - `centroids` (numpy array): Current centroids of the clusters.
     - `abundance_matrix` (numpy array): Input data matrix.
   - **Returns**:
     - A distance matrix where each entry represents the distance between a data point and a centroid.

---

### 3. **`knn_classify(training_data, training_labels, test_data, k)`**
   - **Purpose**: Implements the K-Nearest Neighbors algorithm to classify test data based on labeled training data.
   - **Parameters**:
     - `training_data` (numpy array): Feature matrix for the training dataset.
     - `training_labels` (numpy array): Labels corresponding to the training dataset.
     - `test_data` (numpy array): Feature matrix for the test dataset.
     - `k` (int): Number of nearest neighbors to consider.
   - **Returns**:
     - `predicted_labels` (numpy array): Predicted labels for the test data.

---

### 4. **Main Execution**
   - The script includes an example execution in the `__main__` block:
     - Demonstrates the use of `k_means_split` with a sample dataset.
     - Processes a training dataset (`processed_train_feature`) and outputs cluster labels.

---

## Example Workflow

1. **Clustering with K-Means**:
   - Input a matrix of protein abundance data.
   - Run `k_means_split` to obtain cluster centroids and labels.

2. **Classification with KNN**:
   - Provide labeled training data and test data.
   - Use `knn_classify` to predict cell types for the test data.

---
