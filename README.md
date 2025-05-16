# 🎗️ GBM Subtype Classification (Glioblastoma Multiforme)

This project tackles the problem of classifying molecular subtypes of **Glioblastoma Multiforme (GBM)** — one of the most aggressive brain tumors — using **gene expression data**. Both **unsupervised** and **supervised** machine learning approaches are explored to distinguish between:

- **Classical subtype** (0) – Prognostically favorable
- **Mesenchymal subtype** (1) – Prognostically adverse

---

## 🔍 Project Objectives

1. **Explore subtype structure** using unsupervised methods:
   - PCA, UMAP
   - K-Means and Hierarchical Clustering
   - Evaluation with Adjusted Rand Index (ARI)

2. **Build binary classifiers** for subtype prediction:
   - Support Vector Machine (SVM)
   - Random Forest (RF)
   - 4-Fold Cross-Validation with feature selection (ANOVA F-test)
   - Metrics: Accuracy, Precision, Recall, F1-score (mean ± std across folds)
  
  ---

## 🛠️ Tools & Libraries
Python 3.8+

scikit-learn – ML models and metrics

umap-learn – dimensionality reduction

matplotlib, seaborn – visualization

pandas, numpy – data handling

👥 Contributors
[Gonçalo Brochado]

[Matheus Bissacot]
