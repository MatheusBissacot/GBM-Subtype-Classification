## 🎗️ GBM Subtype Classification (Glioblastoma Multiforme)
### Second assignment of the course Bioinformatics (MSc in Artificial Intelligence, 1st year, 2st semester)

This project addresses the classification of molecular subtypes of Glioblastoma Multiforme (GBM)—one of the most aggressive brain tumors—leveraging gene expression data. The objective is to distinguish between:

Classical subtype (0): Prognostically favorable

Mesenchymal subtype (1): Prognostically adverse

Both unsupervised and supervised machine learning methods are applied to explore and predict these subtypes.

## 🔍 Project Objectives
### 1. **Unsupervised Analysis: Subtype Structure Exploration**

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

## 📊 Results

### Unsupervised analysis
PCA showed the two subtypes have some non-linear structure but no clean linear
separation (119 components were needed to retain 90% of the variance). UMAP improved
the visual separation, especially after first reducing with PCA, though overlap
remained. Clustering validated this: K-Means and Hierarchical Clustering barely aligned
with the true labels (ARI of 0.045, 0.015, and 0.002 respectively), while DBSCAN on the
UMAP embedding did notably better (ARI = 0.223), suggesting the subtypes are
differentiated but not separable by simple unsupervised methods on the full feature space.

### Supervised analysis
Using stratified 5-fold cross-validation, SVM (with and without class balancing) was the
best-performing base model overall, ahead of Random Forest and XGBoost. Hyperparameter
tuning and feature-count experiments (via ANOVA F-test selection) showed:
- SVM peaked at 140 selected features (F1 = 0.941).
- The tuned Random Forest (200 trees) reached F1 = 0.932 ± 0.013 with 200 features, with
  lower variance than its untuned counterpart.
- A soft **VotingClassifier** ensemble (SVM + RF + XGBoost) matched but did not exceed
  the standalone SVM.

**Best model — SVM**: accuracy 93.7%, precision 92.1%, recall 96.2%, F1-score 94.1%.
**Voting Ensemble**: accuracy 93.4%, precision 92.2%, recall 95.5%, F1-score 93.7%.

### Conclusion
SVM was the most effective and efficient classifier for this task, offering the best
balance between precision and recall. Ensemble methods added robustness/stability but no
clear performance gain over SVM alone. Future work could explore further hyperparameter
optimization, alternative ensemble strategies, and growing the dataset to address its
small size and class imbalance.

## 🛠️ Tools & Libraries
Python 3.8+

You can find a text file "requirements.txt" with all the libraries and versions

## 👥 Contributors

Gonçalo Brochado up202106090

Matheus Bissacot up202106708
