Milestone 3
===========


Descriptions
-------
For this milestone, we mainly applied PCA to our original datasets. Since our datasets has many attributes (561 columns), doing dimensional reduction is very necessary and helpful to our project. We would like to have transformed datasets saved in new csv file, so that we could use similar code in Milestone 1 and 2. 


Methods
-------
We first read the data from csv file and preprocessed the data for our analysis, that is we removed the labels and irrelevant columns from our datasets.Then we summarized our data sets by showing the dimensions of both Training and Test sets. We also include scatter plot to show the shape.

After that, we did PCA on the original training set, we checked the variance explained by such model, and then decided the number of princial components being 50. Then we applied the PCA model we learned to both datasets. And we saved the transformed training dataset and test dataset into new csv files named "train/test_pca.csv" for further analysis.

We also did Kernel PCA since we observed some kind of 'rbf' relationship. Based on 'rbf' kernel with gamma=1/#columns, we get a better result than PCA with respect to variance explained. Then we applied the KPCA model to both datasets, and saved them into new csv files named "train/test_kpca.csv".

We then compared the new result using PCA/KPCA with the previous milestones.

In addition, we tried Neural Network using quasi-Newton methods and the stochastic gradient descent. We tried different number and size for the hidden layers and different parameters. Then we calculated the accuracy on test dataset for each method.


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
* "m3.ipynb" is the Milestone 3 main program for applying PCA and applying KPCA.
* "m1.ipynb" is for re-doing Milestone 1.
* "m2.ipynb" is for re-doing Milestone 2.
* "o3.ipynb" is the Neural Network based on PCA data.


Each file is a markdown file that includes both code and result. The code included is intended to be run in Python 3
