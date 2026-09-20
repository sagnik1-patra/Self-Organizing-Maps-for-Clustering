# Customer Segmentation Using Self-Organizing Maps

## Project Overview

This project performs customer segmentation using a
Self-Organizing Map (SOM), also known as a Kohonen Network.

The model maps high-dimensional credit-card customer behavior
onto a two-dimensional neuron grid while attempting to preserve
topological relationships.

## Dataset

Credit Card Customer Dataset

Customers analysed: 8950

## Methodology

1. Data cleaning
2. Median missing-value imputation
3. IQR outlier detection
4. IQR-based outlier capping
5. Feature engineering
6. Min-Max normalization
7. Z-score standardization comparison
8. PCA dimensionality analysis
9. Self-Organizing Map training
10. SOM neuron clustering using K-Means
11. Customer mapping
12. Cluster profiling
13. ANOVA statistical analysis
14. Business interpretation
15. Comparison against direct K-Means

## SOM Configuration

Grid size: 10 x 10

Topology: Rectangular

Initialization: PCA-based

Learning rate: 0.5

Neighborhood radius: 3.0

Neighborhood function: Gaussian

Distance metric: Euclidean

Training iterations: 10000

## Number of Customer Segments

4

## Important Outputs

### U-Matrix

`graphs/06_u_matrix.png`

The U-Matrix visualizes distances between neighboring SOM
neurons. Higher distances can indicate boundaries between
customer groups.

### Hit Map

`graphs/07_hit_map.png`

The hit map shows the number of customers mapped to each neuron.

### Cluster Map

`graphs/08_cluster_labeled_som_map.png`

Shows the customer segments identified by clustering the
trained SOM neurons.

### Radar Chart

`graphs/12_cluster_radar_chart.png`

Compares the behavioral profiles of the customer segments.

### ANOVA Analysis

`graphs/14_anova_feature_importance.png`

Shows features that differ strongly between customer segments.

### SOM vs K-Means

`graphs/15_som_vs_kmeans_comparison.png`

Compares SOM-based segmentation with conventional K-Means.

## Model Files

- `models/trained_som.pkl`
- `models/som_weights.npz`
- `models/minmax_scaler.pkl`
- `models/standard_scaler.pkl`
- `models/som_neuron_kmeans.pkl`
- `models/model_configuration.json`
- `models/feature_names.json`

## Data Outputs

- `customer_cluster_assignments.csv`
- `preprocessed_data_with_clusters.csv`
- `cluster_feature_means.csv`
- `cluster_feature_std.csv`
- `cluster_sizes.csv`
- `anova_cluster_comparison.csv`
- `customer_risk_analysis.csv`
- `som_vs_kmeans_comparison.csv`

## Business Applications

The customer segments can be used for:

- Targeted marketing
- Customer retention
- Premium product recommendations
- Loyalty campaigns
- Credit-product cross-selling
- Customer risk monitoring
- Personalized financial offers

## Conclusion

Self-Organizing Maps provide a useful approach for customer
segmentation because they combine unsupervised learning with
two-dimensional visualization.

The U-Matrix, component planes and hit maps provide additional
information about customer relationships that conventional
clustering algorithms such as K-Means do not directly provide.