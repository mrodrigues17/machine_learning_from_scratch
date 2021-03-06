# Writing Machine Learning Algorithms from Scratch in Python (no ML libraries) 
Implementation of various machine learning algorithms on a binary classification task using only numpy and pandas

## Data
The data are from Titanic survival dataset from Kaggle.com. This is a beginner's level competition where competitors use information about the Titanic passengers to predict if they survived or perished on the sinking ship.

## Algorithms Implemented

  * <b>[Logistic Regression](https://github.com/mrodrigues17/machine_learning_from_scratch/blob/main/logistic-regression-classifier-no-sklearn.ipynb)</b>
As an overview of the algorithm, I initialized coefficients and an intercept to zero and used the log-odds function to find the logarithm of the odds then applied a sigmoid function to restrict the values from 0 to 1. I then used gradient descent to find the optimal coefficients and intercept. These coefficients and intercept are then put into the sigmoid function with these sigmoid values determining the best threshold for classification. I included accuracy, recall and precision functions.
  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Accuracy on test set: 0.78468
* <b>[K-Nearest Neighbors](https://github.com/mrodrigues17/machine_learning_from_scratch/blob/main/titanic-classifier-competition-knn-no-sklearn.ipynb)</b>
After basic data cleaning and feature engineering, I applied min-max normalization and only included numeric data for this algorithm. Using Euclidean distance as the distance measure, I built a function that finds the distance from each data sample to all other data samples to find the "k" most similar cases to each. For each test case, the algorithm goes through each sample in the training set taking the k most similar and applies the label using majority voting (so k must be odd for the algorithm to properly work).
  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Accuracy on test set: 0.77272

* <b>[Decision Tree](https://github.com/mrodrigues17/machine_learning_from_scratch/blob/main/decision-tree-without-ml-libraries.ipynb)</b>
 After data cleaning and feature engineering, I built a function that calculate the gini impurity of each attribute to determing the best attribute to split on at each iteration. Using the gini impurity function, the data are then iteratively split until gini impurity no longer decreases. Once the tree is determined, test cases are applied to the tree rules and corresponding leaf labels are set to each case for prediction.
  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Accuracy on test set: 0.76794


I built these algorithms without the use of step-by-step tutorials and these were simply meant as challenges for myself. I am currently working on making the decision tree algorithms more efficient, and plan to implement other algorithms including a random forest.
