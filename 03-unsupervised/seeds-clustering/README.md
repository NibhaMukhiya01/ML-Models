# Wheat Seed Kernel Clustering (Unsupervised Learning Project)

A practical Machine Learning project using K-Means Clustering and Principal Component Analysis (PCA) to group wheat seed varieties based on geometric measurements of kernel structure.

---

## What is Unsupervised Learning?

In Supervised Learning, models learn from dataset examples that already contain correct answers (labels).

In Unsupervised Learning, there are no target labels provided during training. The algorithm discovers hidden structure, natural groupings, and geometric patterns directly from raw input measurements.

- K-Means Clustering groups similar data points into distinct clusters by minimizing the distance between points and cluster centers.
- Principal Component Analysis (PCA) reduces high-dimensional data (e.g., 7 physical measurements) down to 2 dimensions for easy visual analysis while preserving overall data variance.

---

## How the Seeds Dataset is Used

The dataset contains physical measurements of three different varieties of wheat seeds (Kama, Rosa, and Canadian):
- Features used: Area, Perimeter, Compactness, Length, Width, Asymmetry Coefficient, and Kernel Groove Length.

### Workflow
1. Pairwise Visual Exploration: Generating scatter plots across geometric features to inspect natural separations between seed species.
2. 2D Clustering Baseline: Applies K-Means clustering using only two physical features (Compactness vs Asymmetry).
3. Full-Feature Clustering: Trains K-Means on all 7 physical features simultaneously to group seed varieties in high-dimensional space.
4. PCA Projection: Compresses all 7 dimensions into 2 principal components (PCA1 and PCA2) to visualize cluster boundaries side-by-side with ground truth seed classes.

---

## What You Learn From This Project

1. How K-Means Grouping Works:
   - Understanding centroid placement and how distance-based grouping groups similar physical observations without guidance labels.

2. Dimensionality Reduction with PCA:
   - High-dimensional data cannot be rendered easily on 2D graphs. PCA constructs orthogonal coordinate axes that capture maximum data variance, compressing complex datasets into 2D projections.

3. Evaluating Unsupervised Models:
   - Comparing unsupervised cluster assignments against ground truth category labels to evaluate how closely mathematical distance clusters reflect actual real-world species boundaries.

---

## Folder Structure

```text
seeds-clustering/
├── seeds_clustering.ipynb     # Interactive Google Colab exploratory notebook
├── seeds_clustering.py        # Refactored, modular Python script
└── README.md                  # Project documentation
