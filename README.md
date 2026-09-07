# Clustering ML Lab

A machine learning lab applying **unsupervised clustering** techniques to a customer marketing dataset, segmenting customers based on demographics and purchasing behavior.

## About

Clustering is an unsupervised machine learning technique that groups data points based on similarity, so that points within the same cluster are more alike than points in other clusters. It's widely used in pattern recognition, data mining, and image analysis — here it's applied to **customer segmentation** for a marketing campaign.

## Project Structure

```
Clustering_ML_Lab/
├── RR_I_PES1UG22CS521_Lab6.IPYNB       # Main lab notebook: clustering analysis
├── RR_I_PES1UG22CS521_Lab6.pdf          # Accompanying report/write-up
└── marketing_campaign.csv                # Dataset: customer marketing campaign data
```

## Dataset

`marketing_campaign.csv` is a customer personality/marketing dataset (~2,240 records) with fields including:

- **Demographics:** `Year_Birth`, `Education`, `Marital_Status`, `Income`, `Kidhome`, `Teenhome`
- **Customer history:** `Dt_Customer` (enrollment date), `Recency` (days since last purchase)
- **Spending by category:** `MntWines`, `MntFruits`, `MntMeatProducts`, `MntFishProducts`, `MntSweetProducts`, `MntGoldProds`
- **Purchase channels:** `NumDealsPurchases`, `NumWebPurchases`, `NumCatalogPurchases`, `NumStorePurchases`, `NumWebVisitsMonth`
- **Campaign response:** `AcceptedCmp1`–`AcceptedCmp5`, `Response`, `Complain`

This is the well-known "Customer Personality Analysis" style dataset commonly used for customer segmentation exercises.

## What the Lab Covers

The notebook walks through a typical clustering workflow applied to this dataset:

1. **Data loading & cleaning** — handling missing values (e.g. missing `Income`), converting dates, and removing outliers or invalid records.
2. **Feature engineering** — deriving useful features from raw fields (e.g. customer age from `Year_Birth`, total spending across product categories, total number of purchases/campaigns accepted).
3. **Preprocessing** — encoding categorical variables (`Education`, `Marital_Status`) and scaling numeric features.
4. **Dimensionality reduction** (optional, if used) — e.g. PCA, to visualize high-dimensional customer data in 2D/3D.
5. **Clustering** — applying an unsupervised algorithm (e.g. K-Means and/or hierarchical clustering) to group customers into segments.
6. **Evaluation & interpretation** — using metrics like inertia/elbow method or silhouette score to choose the number of clusters, then profiling each resulting customer segment.

> Refer to the notebook cells directly for the exact algorithms, hyperparameters, and visualizations used, as these are the authoritative source.

## Getting Started

### Prerequisites

```bash
pip install numpy pandas scikit-learn matplotlib seaborn
```

### Running the Notebook

```bash
git clone https://github.com/sandeepelayath/Clustering_ML_Lab.git
cd Clustering_ML_Lab
jupyter notebook RR_I_PES1UG22CS521_Lab6.IPYNB
```

Run the cells in order; the notebook expects `marketing_campaign.csv` to be in the same directory.

## Report

See `RR_I_PES1UG22CS521_Lab6.pdf` for the accompanying write-up detailing the approach, findings, and cluster interpretations.

## Notes

- This is an academic lab exercise; the dataset contains real-world messiness (missing income values, a few implausible birth years) that's typical for a customer segmentation exercise — expect to see cleaning steps addressing this in the notebook.

## License

No license specified. Add one if you intend to share or reuse this code beyond coursework.
