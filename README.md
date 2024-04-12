## SVM classifier implementation solving dual optimization problem

Classification algorithms such as logistic regression require manual feature engineering to classify data with a nonlinear boundary. This involves extending the feature space, such as using feature powers, feature products, trigonometric functions, etc. to increase the complexity of the model.

The SVM algorithm allows to classify data with a nonlinear boundary without manual feature engineering - it uses so-called kernel functions for this purpose.

The goal of the SVM algorithm is to find the optimal $(d-1)$-dimensional hyperplane in $d$-dimensional space that best separates the data.

The algorithm is primarily used for binary classification - it finds the hyperplane that best separates two classes (in the case of a set with two classes). In the case of more classes, we can build multiple classifiers that perform the task of classification - a point belongs to class $A$ or a point does not belong to class $A$ (the so-called one-against-all method).

The simplest version of the SVM algorithm is a linear classifier that searches for a hyperplane that separates the data by maximizing the distance between the hyperplane and the nearest points from both classes (known as the margin). If the data are linearly separable, the algorithm finds the hyperplane that maximizes the margin.

When the data is not linearly separable, so-called kernel functions are used, which map the data to a higher dimensionality space where the data is better separable, so that the problem of classifying data with a nonlinear boundary can be solved.