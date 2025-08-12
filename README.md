# Facial Action Unit Clustering and Engagement Analysis

This repository provides a comprehensive pipeline for clustering YouTube videos based on facial Action Unit (AU) features and analyzing the relationship between facial expressions and video engagement metrics. The project includes data preprocessing, clustering (KMeans), statistical analysis, and visualization.

## Project Structure

```
FacialExtractionClustering/
├── data/
│   ├── processed_faces_v4_aggregated.csv   # Aggregated AU features per video
│   ├── Results_Count_Final.csv             # Video engagement metrics
│   └── ...                                 # Other raw and processed data
├── notebooks/
│   ├── kmeans.ipynb                        # Main clustering and analysis notebook
│   ├── face correlation analysis.ipynb     # Engagement and correlation analysis notebook
│   └── ...                                 # Additional notebooks
├── results/
│   ├── clustered_data.csv                  # Cluster assignments
│   ├── cluster_anova_results_raw.csv       # ANOVA results for engagement metrics
│   ├── channel_weighted_data.csv           # Channel-weighted engagement data
│   ├── weighted_cluster_statistics.csv     # Weighted statistics by cluster
│   ├── top_channels_per_face_cluster.csv   # Top channels per cluster
│   ├── merged_all_data.csv                 # Merged channel, cluster, and engagement data
│   ├── merged_au_engagement_data.csv       # Merged AU and engagement data
│   └── ...                                 # Additional results and outputs
├── README.md                               # Project documentation
└── ...                                     # Additional files
```

## Features

- **AU Data Aggregation**: Aggregate facial Action Unit features per video
- **KMeans Clustering**: Group videos by AU patterns and find optimal clusters
- **Cluster Analysis**: Identify distinctive AUs and interpret cluster meanings
- **Engagement Analysis**: Merge clusters with engagement metrics and perform statistical tests
- **Channel Weighting**: Adjust engagement analysis for channel frequency
- **Visualization**: Visualize clusters, engagement distributions, and AU correlations

## Installation

### Prerequisites

- Python 3.8 or higher
- pip (Python package installer)

### Steps

1. Clone the repository:

   ```bash
   git clone https://github.com/lexilure/FacialExtractionClustering.git
   cd FacialExtractionClustering
   ```

2. Install the required dependencies:

   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn scipy pillow
   ```

## Usage

### Clustering Pipeline

The main clustering and analysis pipeline is in `kmeans.ipynb`:

- Loads and preprocesses AU data
- Aggregates features and scales for clustering
- Finds optimal clusters and performs KMeans clustering
- Visualizes clusters and calculates intra-cluster distances
- Saves cluster assignments for further analysis

To run the pipeline:

1. Open `kmeans.ipynb` in Jupyter Notebook or VS Code
2. Run all cells sequentially to reproduce the analysis and visualizations

### Engagement and Correlation Analysis

For engagement and correlation analysis:

1. Open `face correlation analysis.ipynb`
2. Run all cells to:
   - Merge cluster assignments with channel and engagement data
   - Apply channel weighting
   - Perform ANOVA and other statistical tests
   - Visualize engagement metrics and cluster distributions
   - Save merged and weighted datasets

## Data Flow

1. **Raw AU Data** (`processed_faces_v4_aggregated.csv`): Aggregated facial features
2. **Clustering** (`kmeans.ipynb`): Cluster videos by AU patterns
3. **Cluster Assignments** (`clustered_data.csv`): Output of clustering
4. **Engagement Analysis** (`face correlation analysis.ipynb`): Merge with engagement data, analyze, and visualize
5. **Results**: Cluster statistics, ANOVA results, weighted statistics, and visualizations

## Key Files

| File/Directory                      | Description                                         |
| ----------------------------------- | --------------------------------------------------- |
| `kmeans.ipynb`                      | Main notebook for clustering and analysis           |
| `face correlation analysis.ipynb`   | Engagement and correlation analysis notebook        |
| `processed_faces_v4_aggregated.csv` | Input data with aggregated AU features              |
| `clustered_data.csv`                | Output with cluster assignments                     |
| `Results_Count_Final.csv`           | Video engagement metrics                            |
| `cluster_anova_results_raw.csv`     | ANOVA results for engagement metrics by cluster     |
| `channel_weighted_data.csv`         | Channel-weighted engagement data                    |
| `weighted_cluster_statistics.csv`   | Weighted statistics by cluster                      |
| `top_channels_per_face_cluster.csv` | Top channels per face cluster                       |

## Results

The pipeline generates several types of outputs:

- **Cluster Assignments**: Videos grouped by facial AU similarity
- **Cluster Statistics**: Distinctive features and intra-cluster distances
- **Engagement Analysis**: Statistical test results and AU-engagement correlations
- **Weighted Statistics**: Channel-weighted engagement metrics by cluster
- **Visualizations**: Cluster plots, engagement distributions, and AU correlations

## Troubleshooting

### Common Issues

1. **Notebook not showing results**: Run all cells from the beginning
2. **Missing Dependencies**: Ensure all packages are installed via pip
3. **Data File Not Found**: Check that all required CSV files are present in the project root

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## License

This project is part of academic research. Please cite appropriately if using this code.

## Contact

For questions or issues, please open an issue on GitHub or contact the repository