# CS5691: Programming Assignment 4  

## 📘 Overview  
This repository contains the complete solution for **Programming Assignment 4** of the course **CS5691: Pattern Recognition and Machine Learning**, offered in the **July–November 2024** semester.  

This assignment focuses on applying **Support Vector Machines (SVMs)** with different kernels, exploring **dimensionality reduction using PCA**, and comparing performance with **MLFFNN** and **GMM** classifiers.  
It emphasizes hyperparameter tuning, decision region visualization, support vector analysis, and classification performance reporting.  

---

## 🎯 Assignment Objectives  

- Implement **SVM classifiers** with linear, polynomial, and Gaussian (RBF) kernels.  
- Tune SVM hyperparameters (**C, kernel degree, kernel width**) and analyze results.  
- Perform **Principal Component Analysis (PCA)** for dimensionality reduction.  
- Compare classifiers (**SVM, MLFFNN, GMM**) on reduced-dimension data.  
- Visualize **decision boundaries**, **support vectors**, and **cumulative variance plots**.  
- Report and interpret **classification accuracy**, **confusion matrices**, and **support vector statistics**.  

---

## 📁 Files and Structure

```
multi-class-knn-bayes/
├── Assignment_4.ipynb      # Main Jupyter Notebook with all code and analysis
├── README_4.md               # This file
├── sample_plots_4.pdf        # Reference plots provided with the assignment
└── datasets_assignment_4/
    ├── dataset-4.1/           # 2D: Linearly separable dataset for 3 classes (train.csv, validation.csv, test.csv)
    ├── dataset-4.2/           # 2D: Nonlinearly separable dataset for 2 classes (Train.csv, Val.csv, Test.csv)
    └── dataset-4.3/           # 35-D image dataset for 5 classes (train_data.csv, train_label.csv, val_data.csv, val_label.csv, test_data.csv, test_label.csv)
```

---

## 🧠 Tasks & Classifiers  

### 📌 Dataset 1 (2D, Linearly Separable)  
- **SVM Classifier with Linear Kernel**  

---

### 📌 Dataset 2 (2D, Nonlinearly Separable, 2 Classes)  
- **Polynomial Kernel SVM** (with 4 different degrees, C = 1, 10, 100)  
- **Gaussian Kernel SVM** (with 4 different kernel widths, C = 1, 10, 100)  

---

### 📌 Dataset 3 (35-D, Image Data, 5 Classes)  
- **Polynomial Kernel SVM** (4 degrees, C = 1, 10, 100)  
- **Gaussian Kernel SVM** (4 kernel widths, C = 1, 10, 100)  

---

### 📌 PCA & Reduced-Dimension Classification  
- Perform **PCA** on Dataset 3 to identify a suitable reduced dimension `l`.  
- Train classifiers using reduced data:  
  - **GMM** (same configuration as Assignment 3)  
  - **MLFFNN** (same configuration as Assignment 3)  
  - **SVM** (best performing SVM model from Dataset 3)  

---

## 📊 Report Requirements  

1. **Classification Accuracies Table**  
   - For training, validation, and test sets of Datasets 1, 2, and 3 (all classifiers).  

2. **Confusion Matrices**  
   - For training and test data in:  
     - Exercise 1 (Linear SVM)  
     - Exercise 5 (Reduced-dimension classifiers)  
     - Best models in Exercises 2 & 3  

3. **Decision Region Plots**  
   - Dataset 1: Linear SVM decision region with training data, marking **support vectors**.  
   - Dataset 2: Best Polynomial SVM and Gaussian SVM decision regions with training data, marking **bounded and unbounded support vectors**.  

4. **Support Vector Statistics (Dataset 3)**  
   - Table of percentage of bounded and unbounded support vectors for the best Polynomial and Gaussian SVM models.  

5. **PCA Results (Dataset 3)**  
   - Plot of **Cumulative Variance (σ²cl) vs reduced dimension (l)**.  

---

## 🧰 Requirements  

Install the following Python packages:  

```bash
pip install pandas numpy matplotlib scikit-learn seaborn torch jupyter
```  

---

## ▶️ Run the Notebook  

```bash
jupyter notebook Assignment4.ipynb
```  

Execute cell by cell to run SVM experiments, PCA analysis, classification, and visualizations.  

---

## ✅ Conclusion  

This assignment demonstrates the application of **SVMs** with different kernels, their effectiveness on both simple and complex datasets, and the impact of **dimensionality reduction with PCA**.  
It also compares **SVM, MLFFNN, and GMM classifiers** on reduced data, providing deeper insights into model performance, generalization, and decision boundary analysis.  
