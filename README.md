# Machine Learning Models 

A structured collection of end-to-end Machine Learning projects covering Regression, Classification, and Unsupervised Learning algorithms using modular Python scripts and exploratory Jupyter notebooks.

---

## Projects Overview

| Category | Project Name | Tech Stack | Description | Link |
| :--- | :--- | :--- | :--- | :--- |
| Regression | Seoul Bike Rental Demand | Scikit-Learn, TensorFlow/Keras, Pandas | Predicting hourly bike rental demand based on meteorological conditions. | [View Project](./01-regression/seoul-bike-demand/) |
| Classification | MAGIC Gamma Telescope | Scikit-Learn, Imbalanced-Learn, TensorFlow | Classifying high-energy gamma particles vs cosmic ray background noise. | [View Project](./01-classification/magic-bricks-classification/) |
| Unsupervised | Wheat Seed Kernel Clustering | Scikit-Learn (K-Means, PCA), Seaborn | Grouping wheat seed varieties based on geometric kernel attributes. | [View Project](./03-unsupervised/seeds-clustering/) |

---

## Repository Structure

```text
ML-Models/
├── 01-classification/
│   └── magic-bricks-classification/
│       ├── magic_classification.py    # Refactored Python pipeline
│       └── README.md                  # Project documentation
│
├── 01-regression/
│   └── seoul-bike-demand/
│       ├── bikes_regression.ipynb     # Exploratory Colab notebook
│       └── README.md                  # Project documentation
│
└── 03-unsupervised/
    └── seeds-clustering/
        ├── seeds_clustering.ipynb     # Exploratory Colab notebook
        └── README.md                  # Project documentation
