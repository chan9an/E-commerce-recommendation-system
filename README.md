# Product Description Clustering and Recommendation using K-Means

## Overview
This project applies **K-Means clustering** and **TF-IDF vectorization** to group product descriptions based on text similarity. Additionally, it provides recommendations for similar products based on their textual descriptions.

## Features
- **TF-IDF Vectorization:** Converts product descriptions into numerical vectors for clustering.
- **K-Means Clustering:** Groups products into clusters based on textual similarities.
- **Cluster Analysis:** Extracts key terms from each cluster to understand common themes.
- **Product Recommendation:** Suggests similar products by identifying their cluster.
- **Visualization:** Displays clustering results using plots.

## Implementation Details
- **Data Loading & Preprocessing:**
  - Reads product descriptions from a CSV file.
  - Removes missing values and performs text cleaning.
- **Feature Extraction:**
  - Uses TF-IDF to convert text data into a numerical representation.
- **K-Means Clustering:**
  - Groups similar products into `k` clusters using the K-Means algorithm.
- **Cluster Interpretation:**
  - Identifies the top terms in each cluster to understand common product themes.
- **Recommendation System:**
  - Suggests relevant products by identifying clusters of similar descriptions.

## Dependencies
Install the required libraries using:
```bash
pip install numpy pandas matplotlib scikit-learn
```

## Usage
### Training the Model
1. Load product descriptions from the dataset.
2. Convert text descriptions into numerical vectors using TF-IDF.
3. Apply K-Means clustering to group similar products.
4. Extract cluster keywords to interpret the groupings.

### Running Product Recommendation
```python
show_recommendations("furniture")
```
Example Output:
```
Cluster 7:
 post
 frame
 patio
 aluminum
 screen
 posts
 window
 fence
 steel
 dining
```

### Evaluating Clustering Performance
```python
from sklearn.metrics import silhouette_score
silhouette_avg = silhouette_score(X1, y_kmeans)
print(f"Silhouette Score: {silhouette_avg:.3f}")
print(f"Inertia: {kmeans.inertia_:.3f}")
```

## Dataset
- **Product Descriptions Dataset:** CSV file containing product descriptions.

## Future Enhancements
- Improve clustering accuracy using **BERT embeddings** instead of TF-IDF.
- Optimize the recommendation system using **Nearest Neighbors search**.
- Expand to multi-category product analysis.

