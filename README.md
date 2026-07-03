# CS771 Course Project: Probabilistic ML & Mixed Regression

This repository contains my final project assignments and coursework for **CS771 (Introduction to Machine Learning)**. Since we weren't required to submit raw code files during the course, I've cleaned up my messy experiment scripts and compiled the final logic into three clean Jupyter notebooks, alongside my final PDF reports.

---

## 1. High-Dimensional LinearSVC Optimization (`minor1_linearsvc/`)

For the first minor assignment, I explored how different hyperparameters affect the Linear Support Vector Classifier (LinearSVC) on high-dimensional datasets.

* **What I did:** I ran extensive grid searches to optimize the regularization parameter ($C$), convergence tolerance ($tol$), and max iterations.
* **The goal:** To strictly classify linearly separable datasets without overfitting, mapping out the exact tradeoffs between training time and accuracy.
* **Files:** You can check out my analysis in the `minor1_linearsvc_optimization.ipynb` notebook and read the full theoretical breakdown in `Minor1_Report.pdf`.

---

## 2. MNIST Digit Reconstruction via MAP Inference (`minor2_mnist_map/`)

For the second assignment, we had to fix broken/censored images of handwritten digits from the MNIST dataset.

* **What I did:** Instead of just training a basic neural net, I formulated a single-step Maximum A Posteriori (MAP) inference framework.
* **How it works:** By modeling the pixel distributions as multivariate Gaussian densities, the algorithm can mathematically deduce and reconstruct the missing pixels in a single step based on the surrounding data.
* **Files:** The math and the generated images (before/after reconstruction) are in `minor2_mnist_reconstruction.ipynb` and `Minor2_Report.pdf`.

---

## 3. Mixed Ridge Regression for AQI Prediction (`minor3_mixed_ridge/`)

The final and most complex assignment involved predicting Air Quality Index (AQI) using spatio-temporal data.

* **What I did:** I engineered a custom Mixed Ridge Regression model and used the Expectation-Maximization (EM) algorithm to train it.
* **The results:** This custom model actually outperformed the baseline Decision Trees by **11%** in Mean Absolute Error (MAE).
* **Speeding it up:** To keep it fast, I used exact component routing to minimize inference latency, so it doesn't just guess better, it guesses faster.
* **Files:** The EM implementation and performance benchmarks against Decision Trees are laid out in `minor3_aqi_mixed_regression.ipynb` and `Minor3_Report.pdf`.
