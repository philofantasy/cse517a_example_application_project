Milestone 2 Gaussian Process
===========

Descriptions
-------
In this project, we apply Gaussian Process on multi-class classification using the **RBF kernel** and the **linear kernel**. Our raw data consists of a training set and a test set. We train our GPC on the training data set with two kernels and then compare the performance of these two kernels on the test set. The log marginal likelihood on training set and the prediction accuracy on test set are two measures we use to measure the model performance. Then we merge the training set and the test set and conduct a 10-fold cross-validation on our full dataset to compare the two kernels. Due to the high dimensionality of the features and the large sample size, the cross-validation process is very time consuming. So we randomly draw 1000 samples from the original sample set and conduct a 10-fold CV on it. Prediction accuracy is the measure we use here. 

Methods
-------
* **Gaussian Process Classification (GPC)**  
Gaussiann Process Classifier places a GP prior on a latent function f, which is then squashed through a link function to obtain the probabilistic classification. Internally, the Laplace approximation is used for approximating the non-Gaussian posterior by a Gaussian. Currently, the implementation is restricted to using the logistic link function. The GP prior mean is assumed to be zero. The prior’s covariance is specified by a passing a kernel object. The hyperparameters of the kernel are optimized by maximizing the log-marginal-likelihood (LML) based on the passed optimizer. For multi-class classification, several binary one-versus rest classifiers are fitted. In one-versus-rest, one binary Gaussian process classifier is fitted for each class, which is trained to separate this class from the rest. 

Difficulties
-------

* Gaussian process classification scales cubically with the size of the dataset. So it's not efficient for high dimensional dataset. 

* For multi-class classification, GPC does not implement a true multi-class Laplace approximation internally, but is based on solving several binary classification tasks internally, which are combined using one-versus-rest or one-versus-one. So it does not support predicting probability estimates but only plain predictions. We couldn't use any probabilistic metric as our measure of model performance.

Resources
-------
The resources we used are: 
* Python 3 
* pandas package 
* sklearn package 
* random package 
* Scikit-learn

Files
-------
* "Gaussian Process Classification.ipynb" is for importing data, running GPC and 10-fold CV.

This file is a markdown file that includes both code and result. The code included is intended to be run in Python 3
