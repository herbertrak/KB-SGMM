# KB-SGMM

This repository contains Python notebooks for **KB-SGMM (Kernel-Based Spatial Gaussian Mixture Model)** clustering with associated uncertainty estimation. It includes implementations, experimental evaluations, and visualizations supporting the corresponding paper.

![Uncertainty](https://github.com/user-attachments/assets/efd067c8-358d-4c5b-b127-08fd2a35af65)

---

## 📂 Repository Structure

### 1. Dataset Generation
- **`Datasets_generation.ipynb`**  
  This notebook generates all synthetic datasets used in the study, including:
  - Simple synthetic datasets (SD1, SD2)
  - Geological synthetic datasets (GSD1–GSD4)  
  The generation pipeline includes spatial layout construction, clustering-based labeling, and Gaussian sampling with controlled overlap.

---

### 2. Clustering Experiments
- **`KB_SGMM_EXP.ipynb`**  
  This notebook presents clustering experiments on the generated datasets.  
  It compares KB-SGMM with several baseline methods:
  - Classical methods: **KMeans**, **GMM**
  - Feature-regularized method: **GMM-Laplacian**
  - Spatial methods:
    - **SGMM** (sliding window)
    - **SAGMM** (spatially aided GMM)
    - **GMM-CRF**
    - **GMM-HMRF**

  The notebook reports performance metrics (ARI, NMI) and provides visual comparisons of clustering results.

---

### 3. Uncertainty Analysis
- **`Uncertainty_EXP.ipynb`**  
  This notebook evaluates the uncertainty estimation framework:
  - Analysis on **7 synthetic probability scenarios**
  - Application to the experimental datasets (SD and GSD)
  - Evaluation of uncertainty metrics (Top-2 Gap, Hybrid Score)
  - Quantitative validation using uncertainty-threshold analysis

---

## 📊 Overview

The proposed KB-SGMM framework introduces spatial regularization at the posterior level, enabling:
- Improved clustering performance in spatially structured data
- Interpretable **assignment uncertainty maps**
- Efficient computation independent of feature dimensionality

---

## 🚀 Usage

Run the notebooks in the following order:

1. `Datasets_generation.ipynb`
2. `KB_SGMM_EXP.ipynb`
3. `Uncertainty_EXP.ipynb`

---

## 📌 Notes
- All experiments are reproducible (fixed random seeds included).
- The framework is designed for spatial clustering applications such as predictive geological mapping.
