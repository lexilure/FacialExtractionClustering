# Facial Action Unit Clustering and Engagement Analysis

## Overview

This project clusters videos based on facial Action Unit (AU) features and analyzes the relationship between facial expressions and video engagement metrics (views, likes, comments). The workflow includes data preprocessing, clustering, cluster interpretation, visualization, and statistical analysis.

## Workflow

1. **Data Preparation**
    - Loads AU data from `processed_faces_v4_aggregated.csv`.
    - Aggregates AU features per video (`Video_ID`), removes columns ending with `_c`.
    - Scales features for clustering.

2. **Clustering**
    - Uses KMeans clustering to group videos by AU patterns.
    - Finds the optimal number of clusters using silhouette scores.
    - Assigns cluster labels and saves results to `clustered_data.csv`.

3. **Cluster Analysis**
    - Identifies distinctive AUs for each cluster and interprets their meanings.
    - Visualizes clusters in PCA space and shows representative images.
    - Maps AU patterns to likely emotions using standard FACS definitions.

4. **Statistical Analysis**
    - Merges cluster assignments with engagement metrics from `Results_Count_Final.csv`.
    - Performs statistical tests (Mann-Whitney U, ANOVA) to compare engagement across clusters.
    - Computes and visualizes correlations between AUs and engagement metrics.

5. **Visualization**
    - Plots distinctive features for each cluster.
    - Displays representative images and saves cluster images as PNGs.
    - Visualizes engagement metric distributions and AU-engagement correlations.

## Key Files

- `kmeans.ipynb`: Main notebook for clustering and analysis.
- `processed_faces_v4_aggregated.csv`: Input data with aggregated AU features.
- `clustered_data.csv`: Output with cluster assignments.
- `Results_Count_Final.csv`: Video engagement metrics.
- `cluster_anova_results_raw.csv`: ANOVA results for engagement metrics by cluster.

## How to Run

1. **Install Dependencies**

    ```bash
    pip install pandas numpy matplotlib seaborn scikit-learn scipy pillow
    ```

2. **Run the Notebook**

    - Open `kmeans.ipynb` in Jupyter Notebook or VS Code.
    - Execute cells sequentially to reproduce the analysis and visualizations.

## Outputs

- Cluster assignments and statistics.
- Visualizations of clusters, distinctive features, and representative images.
- Statistical test results and AU-engagement correlations.

## Notes

- AU meanings are mapped using the `au_meaning` dictionary in the notebook.
- Emotion mappings are based on standard FACS definitions.
- Representative images are loaded from the directory specified by `base_path`.