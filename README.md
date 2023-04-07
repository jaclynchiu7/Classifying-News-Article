# Binary Classification of News Articles

Created an end-to-end Pipeline to classify news articles into sports and climate categories. Project consists of feature extraction, dimensionality reduction methods, and classification models.

# Pipeline hyperparameters

* note the value of min_df is percentage which to ignore if it doesn't appear in x% of the documents

Module | Options
--- | ---
Feature Extraction| Lemmatization vs Stemming
min_df | 3 vs 5
Dimensionality Reduction | LSI (k = 5, 30, 80) vs NMF (k = 5, 30, 80)
Classifier | SVM, Logistic Regression (L1, L2, and no regularization), Gaussian NB

# Best 5 Performing Models

Feature Extraction | Dimensionality Reduction | Classifier | Accuracy 
--- | --- | --- | ---
Lemmatization min_df = 5 | LSI (k = 80) | Logistic Regression (reg_strength = 1000, penalty = l2) | 96.11%
Lemmatization min_df = 5 | LSI (k = 80) | Logistic Regression (reg_strength = 100, penallty = l1) | 96.07%
Stemming min_df = 5 | NMF (k = 80) | SVM (reg_strength = 1000) | 96.03%
Lemmatization min_df = 3 | LSI (k = 80) | Logistic Regression (reg_strength = 1000, penallty = l2) | 96.03%
Lemmatization min_df = 3 | NMF (k = 80) | SVM (reg_strength = 1000) | 96.95%
