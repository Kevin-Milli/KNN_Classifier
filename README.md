# KNN Classifier
The KNN (K-Nearest Neighbors) Classifier is a machine learning algorithm that can be used for both classification and regression tasks. 

It is a simple and intuitive algorithm that determines the class or value of a sample based on the majority vote or average of its nearest neighbors in the feature space.

## Class Description

The `KNN` class represents the KNN Classifier. It has the following attributes:

* `method`: Specifies the method used for classification. Default is 'k' (k-nearest neighbors).
* `k`: The number of nearest neighbors to consider. Only used when `method` is 'k'.
* `r`: The radius within which neighbors are considered. Only used when `method` is 'r'.
* `weight`: Determines whether to weight the neighbors by their distance. Default is `False`.
* `distance_metric`: The distance metric used to measure the similarity between samples. Can be 'euclidean', 'manhattan', or 'chebyshev'. Default is 'euclidean'.

## The class provides the following methods:

* `feed(X_tr, y_tr, seed)`: Shuffles the input matrix `X_tr` and vector `y_tr` using the same random order. Returns the shuffled matrices `X` and `y`.
* `stack(X_tr, y_tr, test_percentage)`: Splits the dataset into training and testing sets based on the specified test_percentage. Default is 0.2 (80% training, 20% testing). Returns the training and testing matrices `X_train` and `X_test`, and the corresponding vectors `y_train` and `y_test`.
* `single_predict(X_tr, y_tr, x_test)`: Predicts the class label for a single test sample `x_test` based on the training samples `X_tr` and their corresponding labels `y_tr`. Returns the predicted class label.
* `best_fit(X, y, low, high, weight, list_prev, list_ytest)`: Finds the best fit for the KNN classifier within a specified range of values for `k` or `r`. Calculates the accuracy of the classifier for each value in the range and returns the best fit value, percentage of correct predictions, and optionally the list of prediction percentages and the list of corresponding test labels.

## Usage

I show two examples of famous datasets in the Notebook

