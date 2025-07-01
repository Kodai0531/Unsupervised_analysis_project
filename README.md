# Spotify dataset

## Objective

This project make a visual representation of the diversity of songs defined in the Spotify Tracks Dataset and make high-dimensional data by applying **dimensionality reduction** and **clustering techniques**. The objective is to uncover song clusters, identify their defining features, and gain insights into patterns within the dataset.

## Dataset

**Source:** [Kaggle Spotify Tracks Dataset](https://www.kaggle.com)

-   **Samples:** 114,000 samples (subset of 10,000 are used fo used for analysis)

-   **Features:** 16 numeric attributes (e.g., 'danceability,' 'tempo') and 4 categorical features (e.g., 'track_genre').

### Preprocessing

-   Dropped duplicates and missing values.
-   Encoded categorical attributes for uniformity.
-   Random sampling of 10,000 tracks for analysis.

------------------------------------------------------------------------

## Methodology

### 1. **Dimensionality Reduction**

Three methods were tested for dimensional reduction:

-   **PCA:** Best performance based on stress values and correlations.

-   **t-SNE:** Preserved local structure but high stress.

-   **UMAP:** Balanced global and local patterns but less effective than PCA.

### 2. **Clustering**

Three clustering methods were evaluated:

-   **K-Means (k=4):** Selected for its clear separation and interpretability.

-   **Hierarchical & HDBSCAN:** Showed limited scalability and pattern recognition.

Parameter optimization included using the Elbow Method to determine the optimal number of clusters.

------------------------------------------------------------------------

## Results

### Cluster Characteristics

Clusters were grouped into four distinct categories based on song features:

1.  **Cluster 1:** Upbeat, rhythmic genres (e.g., 'disco,' 'dance').

2.  **Cluster 2:** Intense, high-energy genres (e.g., 'hard rock,' 'metal').

3.  **Cluster 3:** Refined, melodic genres (e.g., 'jazz,' 'acoustic').

4.  **Cluster 4:** Calm, atmospheric genres (e.g., 'ambient,' 'classical').

### Popularity and Size

-   Cluster 2 and Cluster 3 contained more popular songs.

-   Cluster 4 had the smallest number of songs and the least popularity.

------------------------------------------------------------------------

## Key Findings and Insights

-   **Genre Associations:** Each cluster shows strong correlations with specific genres, reflecting the distinct musical styles captured.

-   **Popularity Trends:** Mid-range clusters (2 and 3) are more popular, while extremes (1 and 4) cater to niche audiences.

-   **Cluster Profiles:** Feature analysis highlights contrasting styles, from energetic tracks to calm, instrumental compositions.

------------------------------------------------------------------------

## Limitations and Future Work

-   **Subset Dependence:** Results are based on a random subset and may not reflect the full dataset.

-   **Fixed Clustering (k=4):** The choice of k may overlook finer nuances.

-   **Future Improvements:** Explore dynamic clustering approaches and integrate listener preferences for a recommendation system.
