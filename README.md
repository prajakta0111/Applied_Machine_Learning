# Applied_Machine_Learning
Machine Learning Assignments at Indiana University

## [00_linear_regression.ipynb](https://github.com/prajakta0111/Applied_Machine_Learning/blob/master/00_linear_regression.ipynb)
#### Part 1
The first problem is to implement Linear Regression using Gradient Descent from scratch. The dataset used is Boston Housing Price dataset. The features given include details about houses like number of rooms, per capita price in the town and so on. The train-test split is done as 70%-30%. To find the error in the predictions, Root mean squared error is implemented.
#### Part 2 
The second part is a classic binary classification problem. 
The first step is to generate random points to be classified. After generating those, a line that will classify the points into two classes is needed. For that, keep changing the values of X,Y and slope of line which clasifies the points into 2 classes. When a line giving least misclassification is obtained, the updation of parameters to find new lines can be stopped. 

## [01_data_processing_modelling.ipynb](https://github.com/prajakta0111/Applied_Machine_Learning/blob/master/01_data_processing_modelling.ipynb)
#### Part 1
This notebook implements data preprocessing for the given dataset and fits a regression model on it. 
The preprocessing steps implemented are:

Normalization 

Missing value imputation by mean

One hot encoding for categorical variables

Once these steps are done, a baselie regression model is fit which yields an accuracy of 81%

In order to improve the accuracy, experimenting with the hyperparameters is done. Rather than using lambda value chosen by default by the sklearn method, a set of varying lambda values is given to the function so as to see which lambda value is better in terms of higher accuracy. 
The best accuracy is achieved at accuracy of 84.1% with threshold =  0.99 and regularization coefficient = 100.0

#### Part 2 
This part is mainly to understand how the degree of polnomial affects the fit of a model on a dataset. The aim was to generate datapoints with a distribution of various degrees and fitting a polynomial while experimenting with different fits to understand the phenomenon of over/under fitting.

## [02_NN_scratch.ipynb](https://github.com/prajakta0111/Applied_Machine_Learning/blob/master/02_NN_scratch.ipynb)
The aim is to build a neural network from scratch having the following architecture:

Input layer

Dense hidden layer with 512 neurons, using relu as the activation function

Dropout with a value of 0.2

Dense hidden layer with 512 neurons, using relu as the activation function

Dropout with a value of 0.2

Output layer, using softmax as the activation function

A 5 fold cross validation yields the best accuracy at 54%

## [03_EDA_Feature.ipynb](https://github.com/prajakta0111/Applied_Machine_Learning/blob/master/03_EDA_Feature.ipynb)

This notebook performs Exploratory Data Analysis and Feature Engineering on a dataset whose headers are masked in order to understand data in a better way. 
The data preprocessing steps from [01_data_processing_modelling.ipynb](https://github.com/prajakta0111/Applied_Machine_Learning/blob/master/01_data_processing_modelling.ipynb) are performed on this data as well. Then in order to remove the reduntant column from the data which are not correlated and do not contribute much to the target variable, a random forest is fit on the data. The feature importance method is used to calculate the contribution od each variable to the target variable. The columns below a specific threshold value are removed. From almost 500 columns, the data is reduced to 93 columns. Then, various models are trained on the data like:

Neural Network

Random Forest

SVM

KNN

The best result in terms of accuracy is observed for Random Forest with an accuracy of 88%
