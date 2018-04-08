Milestone 3
===========


Descriptions
-------
For this milestone, we mainly applied PCA to our original datasets. Since our datasets has many attributes (561 columns), doing dimensional reduction is very necessary and helpful to our project. We would like to have transformed datasets saved in new csv file, so that we could use similar code in Milestone 1 and 2. 


Methods
-------
We first read the data from csv file and preprocessed the data for our analysis, that is we removed the labels and irrelevant columns from our datasets.Then we summarized our data sets by showing the dimensions of both Training and Test sets. We also include scatter plot to show the shape.

After that, we did PCA on the original training set, we checked the variance explained by such model, and then decided the number of princial components being 50. Then we applied the PCA model we learned to both datasets. And we saved the transformed training dataset and test dataset into new csv files named "train/test_pca.csv" for further analysis.

We also did Kernel PCA since we observed some kind of 'rbf' relationship. Based on 'rbf' kernel with gamma=1/#columns, we get a better result than PCA with respect to variance explained. Then we applied the KPCA model to both datasets, and saved them into new csv files named "train/test_kpca.csv" 


Difficulties
-------
The PCA model runs fast, but KPCA runs slowly.

KPCA reqires input value of gamma, which relies on cross validation result.

The variance explained by KPCA is nice, but that by PCA is not good. We have to use up to 50 principal components to get a reasonable accuracy on other analysis.


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
