Milestone 1
===========

Descriptions
-------
We trained and ran a linear classifier on the given training data, and evaluate the model with the given test data.
Then we merged the given train.csv and test.csv to one csv file, and used cross-validation to evaluate the linear classifier.
We did the similar things using decision tree with and without bagging.

Methods
-------
We first read the data from csv file, preprocessed the data for our analysis. Then we created linear classifier on the training dataset.
After we got the linear classificiation model, we fit it onto the test dataset which is independent of the training dataset.
Next, we compared the fitted value from the model and the true value to calculate the error rate.
For cross-validation, we first read both dataset into python, then combined them into new matrix and saved in csv file.
We then did similar approch on the combined dataset to do cross validation. 
We hold part of the data and then did cross-validation on 10 folders to get 10 fitted results.
For decision tree, we built decision tree on the training set, then tested the model using test set.
We also did cross-validation on the combined dataset to check the performance of decision tree.

Difficulties
-------
The potential difficulty we faced was the running time of our Python code. 
Since we got a really large dataset with dimensions 10299 by 561, it took a long time to build the model and do cross-validation.

Resources
-------
The resources we used are: 
* Python 3 
* pandas package 
* numpy package 
* sklearn package 
* warnings package 


Files
-------
* "Linear_Classifier.ipynb" is for reading data and running linear classifier on training dataset and then fit on test set.
* "Linear_Classifier_CV.ipynb" is for merging data and running cross-validation on combined dataset.
* "Decision_Tree.ipynb" is for running decision tree model and doing cross-validation with decision tree.


Each file is a markdown file that includes both code and result. The code included is intended to be run in Python 3

