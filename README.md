##🎗️ GBM Subtype Classification (Glioblastoma Multiforme)
### Second assignment of the course Bioinformatics (MSc in Artificial Intelligence, 1st year, 2st semester)

This project addresses the classification of molecular subtypes of Glioblastoma Multiforme (GBM)—one of the most aggressive brain tumors—leveraging gene expression data. The objective is to distinguish between:

Classical subtype (0): Prognostically favorable

Mesenchymal subtype (1): Prognostically adverse

Both unsupervised and supervised machine learning methods are applied to explore and predict these subtypes.

## 🔍 Project Objectives
1. Unsupervised Analysis: Subtype Structure Exploration
Dimensionality reduction techniques: PCA and UMAP

Clustering algorithms: K-Means and Hierarchical Clustering

Cluster validation using Adjusted Rand Index (ARI)

### 2.**Supervised Learning: Binary Classification of GBM Subtypes**
Models implemented:
 - Support Vector Machine (SVM)
 - Random Forest (RF)

Rigorous evaluation using 4-fold cross-validation
Feature selection via ANOVA F-test to identify the most relevant genes
Performance metrics reported as mean ± standard deviation across folds:
   - Accuracy
   - Precision
   - Recall
   - F1-score

## 🛠️ Tools & Libraries
Python 3.8+

You can find a text file "requirements.txt" with all the libraries and versions

## 👥 Contributors

Gonçalo Brochado up202106090

Matheus Bissacot up202106708
