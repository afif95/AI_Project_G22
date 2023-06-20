# AI_Project_G22
COMP-6721-AI , A comparative analysis of image classification using CIFAR10 Dataset

### Description:

This repository contains source code for Naive Bayes for supervised learning classification, Decision Tree for both supervised and semi supervised learning classification, CNN for supervised learning classification. The Cifar 10 Dataset was used for the procedure.

### Naive Bayes:

Data Loading: The CIFAR-10 dataset is loaded using scikit-learn's fetch_openml function. The dataset is split into input features (X) and target labels (y).

Feature Extraction: The Histogram of Oriented Gradients (HOG) features are extracted from the images. HOG is a widely used technique for capturing shape and gradient information in an image.

Data Split: The dataset is split into training and testing sets using the train_test_split function from scikit-learn. The testing set is kept as 20% of the total data.

Preprocessing and Classifier Pipeline: A pipeline is created using scikit-learn's make_pipeline function, which consists of a StandardScaler for feature scaling and a GaussianNB classifier, which is a Naive Bayes classifier assuming Gaussian distribution.

Hyperparameter Tuning: Grid search with cross-validation (GridSearchCV) is performed to find the best hyperparameters for the classifier. In this case, no hyperparameters are specified to tune.

Model Training and Prediction: The best classifier obtained from hyperparameter tuning is trained on the training set and used to predict the labels for the test set.

Performance Evaluation: Various performance metrics such as precision, recall, F1 score, and accuracy are calculated using scikit-learn's metrics module.

Bar Plot of Predicted Class Labels: A bar plot is created to visualize the predicted class labels and their counts using matplotlib.

t-SNE Visualization: t-SNE (t-Distributed Stochastic Neighbor Embedding) is applied to reduce the dimensionality of the test set to 2 dimensions. The reduced features are then plotted in a scatter plot, with each point colored according to its predicted class label.

### Decision Tree for supervised learning classification

Data Loading and Preprocessing:

The CIFAR-10 dataset is loaded using the torchvision library and transformed into tensors.
The input features and target labels are converted to NumPy arrays and reshaped into a 2D array.

Data Splitting:

The dataset is split into training and testing sets using the train_test_split function from scikit-learn.
80% of the data is used for training, and 20% is used for testing.

Decision Tree Classifier:

A decision tree classifier is created using the DecisionTreeClassifier class from scikit-learn.
The classifier is trained on the training set using the fit method.

Model Evaluation:

The accuracy of the model is evaluated on both the training and test sets using the score method.
The confusion matrix is computed using the confusion_matrix function from scikit-learn.
The accuracy, precision, recall, and F1-score are calculated and printed.
The confusion matrix is visualized using a heatmap.

Decision Tree Visualization:

The decision tree is visualized using the export_graphviz function from scikit-learn and the graphviz library.
The resulting decision tree is saved as a PNG image.

Hyperparameter Tuning:

Grid search is performed using the GridSearchCV class from scikit-learn to find the best hyperparameters for the decision tree.
The model is trained again with the best hyperparameters.
The accuracy and evaluation metrics (precision, recall, and F1-score) are calculated and printed.
A bar plot is created to visualize the evaluation metrics.

### Decision Tree for semi supervised learning classification

Decision Tree Classifier:

The CIFAR-10 dataset is loaded, and the input features and target labels are converted to NumPy arrays.
The labeled data is split into training and validation sets.
A decision tree classifier is created using the DecisionTreeClassifier class from scikit-learn.
The classifier is trained on the labeled training data and evaluated on the validation set.
The accuracy scores are calculated and printed.

Semi-Supervised Learning:

The labeled and unlabeled instances are split using train_test_split, and the sizes are adjusted to be equal.
The labeled data is split into training and validation sets.
A decision tree classifier is trained on the combined labeled and unlabeled data.
The model is evaluated on the test set, which consists of a portion of the combined data.
The accuracy scores are calculated and printed.

Random Forest Classifier:

The CIFAR-10 dataset is loaded and split into training set, validation set, and test set.
Hyperparameter tuning is performed to find the best combination of max_depth and n_estimators for the random forest classifier.
The best model is selected based on the highest accuracy on the validation set.
The best model is evaluated on the labeled data and the test set.
The accuracy, precision, recall, and F1-score are calculated and printed.

