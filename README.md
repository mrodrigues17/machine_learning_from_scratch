# Writing Machine Learning Algorithms from Scratch in Python (no ML libraries) 
Implementation of various machine learning algorithms on a binary classification task.

## Data
The data are from Titanic survival dataset from Kaggle.com. This is a beginner's level competition where competitors use information about the Titanic passengers to predict if they survived or perished on the sinking ship.

## Algorithms Implemented
<ol>
  <li><b>Logistic Regression</b></li>
As an overview of the algorithm, I initialized coefficients and an intercept to zero and used the log-odds function to find the logarithm of the odds then applied a sigmoid function to restrict the values from 0 to 1. I then used gradient descent to find the optimal coefficients and intercept. These coefficients and intercept are then put into the sigmoid function with these sigmoid values determining the best threshold for classification. I included accuracy, recall and precision functions.
Accuracy on test set: 0.78468
  <li><b>K-Nearest Neighbors</b></li>
After basic data cleaning and feature engineering, I applied min-max normalization and only included numeric data for this algorithm. Using Euclidean distance as the distance measure, I built a function that finds the distance from each data sample to all other data samples to find the "k" most similar cases to each. For each test case, the algorithm goes through each sample in the training set taking the k most similar and applies the label using majority voting (so k must be odd for the algorithm to properly work).
Accuracy on test set: 0.77272

  <li><b>Decision Tree</b></li>
</ol>

I built these algorithms without the use of step-by-step tutorials and these were simply meant as challenges for myself. I am currently working on making the decision tree algorithms more efficient, and plan to implement other algorithms including a random forest.
