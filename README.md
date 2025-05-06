# Task-8
# Mall Customer Segmentation using K-Means Clustering

This project applies **K-Means Clustering** on the Mall Customers dataset to segment customers based on income and spending score.  
The project includes dataset visualization, optimal cluster selection using the Elbow Method, cluster visualization, and evaluation using the Silhouette Score.

---

## Technologies Used

- Python  
- NumPy  
- Pandas  
- Matplotlib  
- Scikit-learn  

---

## Steps and Implementation

### 1. Load and Visualize Dataset (Optional PCA for 2D View)
- Loaded the dataset `Mall_Customers.csv`
- Selected key features:
  - `Annual Income (k$)`
  - `Spending Score (1-100)`
- (Optional) Applied feature scaling using `StandardScaler`
- Visualized the original data using a scatter plot

### 2. Fit K-Means and Assign Cluster Labels
- Applied `KMeans` from `sklearn.cluster` with an initial cluster count (`n_clusters=5`)
- Predicted cluster labels and assigned them to the data
- Stored and visualized the centroids

### 3. Use the Elbow Method to Find Optimal K
- Evaluated `K` values from 1 to 10 using Within-Cluster Sum of Squares (WCSS)
- Plotted the Elbow Curve to identify the best `K` value
- Chose the "elbow" point where WCSS stops decreasing significantly

### 4. Visualize Clusters with Color-Coding
- Used different colors for each cluster
- Marked centroids with a black 'X' marker
- Labeled axes with scaled features

### 5. Evaluate Clustering Using Silhouette Score
- Computed `silhouette_score` to assess the consistency within clusters
- Score ranges from -1 to 1, with higher values indicating better clustering

### 6. Suppress Warning
- Suppressed the known Windows + MKL memory leak warning from `sklearn.cluster.KMeans`

---

## Example Output

```text
Silhouette Score (K=5): 0.553
