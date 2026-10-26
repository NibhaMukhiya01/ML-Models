# MAGIC Gamma Telescope Particle Classification (Supervised Learning)

A binary classification project predicting atmospheric particle types (Gamma signals vs. Hadron background noise) using physical metrics recorded by the MAGIC Cherenkov Telescope.

---

## What is Supervised Classification? 

In Machine Learning, Supervised Classification predicts categorical labels for input data points using labeled training examples.

- Regression predicts continuous numbers (e.g., predicting temperature or price).
- Binary Classification assigns observations into one of two distinct categories:
  - Class 1 (Gamma Signal): High-energy photon showers.
  - Class 0 (Hadron Background): Cosmic ray particle noise.

---

## How the MAGIC Dataset is Used

The dataset contains 10 continuous physical attributes describing Cherenkov radiation light patterns (such as length, width, size, concentration, and asymmetry).

### Workflow
1. Handling Class Imbalance: The dataset contains more background noise events than signal events. We apply Random Over-Sampling (RandomOverSampler) to the training set to prevent model bias towards the majority class.
2. Standard Scaling: Features vary significantly in unit scales. We apply StandardScaler to normalize feature distributions.
3. Model Benchmarking: We train and compare four baseline classifiers:
   - k-Nearest Neighbors (kNN)
   - Gaussian Naive Bayes
   - Logistic Regression
   - Support Vector Machine (SVC)
4. Deep Learning with Hyperparameter Tuning: We construct a multi-layer Neural Network in TensorFlow/Keras and run a hyperparameter grid search across hidden node capacities, dropout probabilities, learning rates, and batch sizes to minimize validation loss.

---

## What You Learn From This Project

1. Class Imbalance Resampling:
   - Resampling techniques prevent models from achieving misleadingly high accuracy simply by predicting the majority class.

2. Comprehensive Benchmark Comparison:
   - Comparing traditional algorithmic models (kNN, Naive Bayes, Logistic Regression, SVM) against Deep Neural Networks reveals trade-offs between model complexity and classification speed.

3. Performance Metrics Beyond Accuracy:
   - Evaluating predictions using Precision, Recall, and F1-Score to ensure high sensitivity when detecting rare gamma signals.

---

## Folder Structure

```text
magic-bricks-classification/
├── magic_classification.ipynb   # Interactive Google Colab exploratory notebook
├── magic_classification.py      # Refactored, modular Python script
└── README.md                    # Project documentation
