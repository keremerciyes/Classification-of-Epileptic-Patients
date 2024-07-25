EpiClassify: Leveraging Machine Learning for Epilepsy Classification
Overview
EpiClassify is a machine learning project aimed at classifying epilepsy severity using EEG signals. The project focuses on categorizing patients into mild and mild severe categories, utilizing advanced machine learning techniques for accurate diagnosis and classification.

Project Team
Yesim Nur Tortop
Mustafa Soydan
Kerem Ercüyes
Supervised By: Isabella Castiglioni
Objectives
The principal objective of this project is to establish a machine learning methodology for the classification of epilepsy severity based on EEG data analysis.

Dataset
Source: EEG data from 500 individuals
Features: 4094
Data Description: The dataset includes EEG signals, which measure electrical activity in the brain using electrodes attached to the scalp. This data is essential for diagnosis, classification, localization, and treatment monitoring.
Methodology
Data Preparation
Selecting Class 3 and Class 4 Patients: Focusing on specific patient categories.
Normalization: Standardizing the data.
Train-Test Split: Dividing the data into training and testing sets.
Outlier Detection: Using a Z-score threshold of 2.5 to remove outliers.
Feature Selection
PCA (Principal Component Analysis): Dimensionality reduction and feature compression to improve model performance.
K-Best Selection: Identifying the top features that contribute most significantly to the classification.
Classification Models
Support Vector Machine (SVM)
Hyperparameters:
C: Controls the trade-off between smooth decision boundaries and correctly classifying training points.
Kernel: Function used to map the dataset into a higher-dimensional space.
Gamma (γ): Determines the influence distance of a single training example.
Performance: Evaluated using 5-fold cross-validation, with and without outliers.
Random Forest
Hyperparameters:
N-Estimators: Number of trees in the forest.
Max Depth: Maximum length of the paths from the root to any leaf.
Criterion: Measures affecting how decision trees split data at a node.
Max Features: Number of features to consider when looking for the best split.
Performance: Evaluated using 5-fold cross-validation, with and without outliers.
Results
SVM
Best Model: Outliers removed, feature selection with K-Best (K=50)
Accuracy: Varies across folds, with a mean accuracy of 0.69375 and a standard deviation of 0.087 (without outliers).
Random Forest
Best Model: Outliers removed, feature selection with K-Best (K=100)
Accuracy: Highest mean accuracy of 0.854 with a standard deviation of 0.0348 (without outliers).
Conclusion
In our comparative study, the Random Forest algorithm paired with K-Best feature selection (K=100) proved to be superior. This model's success is attributed to its ensemble nature, leveraging multiple decision trees and focusing on the most statistically significant features, demonstrating robust generalization capabilities.

References
WHO. (2020). Epilepsy: a public health imperative. Available: WHO Publication
Krumholz et al. (2015). Management of an unprovoked first seizure in adults. Neurology, 85(17), 1526-1537.