# MNIST Digit Classification: k-NN vs Nearest Centroid

This repository contains the implementation and analysis of two classic machine learning algorithms used to classify handwritten digits from the **MNIST dataset**: **K-Nearest Neighbors (k-NN)** and the **Nearest Centroid Classifier**.

## 📊 Project Overview
The assignment focuses on building both custom and library-based (`scikit-learn`) versions of the classifiers to evaluate their generalization capabilities, performance, and behavior under different hyperparameters (distance metrics and number of neighbors $k$).

### Key Features:
* **Custom Implementations:** Scratch implementation of k-NN and Nearest Centroid classifiers.
* **Hyperparameter Tuning:** Evaluated $k$ values ranging from 3 to 60,000.
* **Distance Metrics Compared:** Euclidean vs. Manhattan distance.
* **Comprehensive Evaluation:** Detailed confusion matrices, accuracy reports, and analysis of underfitting.

## 📈 Performance Summary

| Algorithm | Hyperparameters | Accuracy |
| :--- | :--- | :--- |
| **k-NN** (scikit-learn) | $k=3$, Euclidean | 97.11% |
| **k-NN** (Custom) | $k=3$, Euclidean | **97.30%** |
| **Nearest Centroid** (scikit-learn) | Euclidean | 81.30% |
| **Nearest Centroid** (Custom) | Euclidean | 81.30% |

### Key Insights:
* The **k-NN classifier** significantly outperforms the Nearest Centroid model by capturing local variations in handwriting styles.
* **Underfitting Effect:** Increasing $k$ leads to a massive drop in performance for k-NN, peaking at $k=60,000$ where the model completely underfits and predicts only the majority class.
* **Metric Comparison:** Euclidean distance systematically yielded better accuracy than Manhattan distance for this specific morphological task.

## 📁 Repository Structure
* `Project1(AP).ipynb`: The complete Google Colab / Jupyter Notebook with the source code.
* `images/`: Directory containing generated confusion matrices and classification examples (correct/incorrect predictions).

## 🛠️ Requirements & Installation
To run the notebook locally, ensure you have the following Python libraries installed:
```bash
pip install numpy scikit-learn matplotlib
