# Heart-Disease-Prediction
Heart Disease is the leading cause of death and hospitalization in the world. Due to technological advancements and the assistance of computer engineering, heart disease may now be quickly and successfully diagnosed and treated. In the realm of medicine nowadays, illness prediction using machine learning is quite popular. According to the Chest and Heart Association of Bangladesh, 25% of all heart strokes in Bangladesh happen in those under 40 and 50% of heart attacks happen to people under 50. The risk of heart attacks is three times higher in urban areas than in rural ones. Our project is regarding heart disease prediction which fall under the category of supervised learning and the dataset is taken from the renowned site- kaggel. Based on data preprocessing and models applied to the dataset, we predicted whether a patient had heart disease or not. Using the provided features, this dataset is intended to identify which patients are most likely to develop a heart disease in the near future.

**Dataset description**

The dataset is taken from renowned source Kaggel. This data set dates from 1988 and consists of four databases: Cleveland, Hungary, Switzerland, and Long Beach V. It contains 76 attributes, including the predicted attribute, but all published experiments refer to using a subset of 14 of them. The "target" field refers to the presence of heart disease in the patient. It is integer valued 0 = no disease and 1 = disease.


**Data Preprocessing

When developing a machine learning project, it is not always a case that we come across the clean and formatted data. And while doing any operation with data, it is mandatory to clean it and put it in a formatted way. So for this, we do data preprocessing.It refers to manipulation or dropping of data before it is used in order to ensure or enhance performance, and is an important step in any Machine Learning project.
There are various kinds of data pre-processing methods followed by machine learning projects.For example, Handling/Imputing Missing Values,Check for Redundant values, Feature Scaling/Normalization,Encoding Categorical Features etc.But its not necessary to apply all the methods to any machine learning project.It actually gets determined by the dataset we have.The nature of the data and the purposes of a particular project or researcher will determine what methods we need to apply or even we need to apply any of the pre-processing methods at all.
For example if a random dataset have no null value in its raw data form,then there is no-point of applying method of handling missing/null values.Similarly in our project we didn’t need to apply all kinds of data preprocessing methods.To make the data usable for our purpose of  Heart Disease Prediction,we needed to do :





1.	Handling null or missing values:

Null or missing values need to be handled carefully. Because datasets should have no null values. If so, it should be dropped. The most effective way to do this is to impute the values from the sklearn library.
We start by checking if there are any null values and which columns have how many null values. By performing necessary steps we got null values in our dataset. So we have handel the null values by implementing imputation on our dataset effectively.


2.	Duplicate values:

There should be no duplicate values in any dataset. Therefore, if there are duplicate values, we should drop them. In our dataset, we checked whether there were duplicate values or not. We found duplicate values but our dataset is too small . if we drop the duplicates values there remains a few values. So we didn’t perform it and worked with duplicate values. 


3.	 Features Encoding:

Due to the fact that our machine language only knows binary values, categorical features are handled. Since categorical variables are textual, we encode them. There are two ways to encode categorical variables: one is binary and the other is one-hot encoding. One of the best ways is to do one-hot encoding as it handles efficiently. But in our dataset we don’t need to perform it.


4.	Splitting Features and Label:

For any machile learning project the data must need to be splitted by features and lebel to function the models of any project.In our case we have total 14 columns in the dataset of which the first 13 were splitted as features and The 14th  “Target” as label.We put the features in “X” variable and the “Target” in “Y”. 


5.	Train -Test-split:

Basically, it is a technique for testing how well a machine learning algorithm performs. Training datasets are used to fit the algorithm, while testing datasets are used to evaluate it. To split a single dataset for two different purposes, we use the train-test-split function. A large dataset makes train_test_split the most efficient because there is enough data for training and testing. We gave 80% of the data for training, and 20% for testing to get more accurate results.


Models

Using the dataset we are trying to solve classifier problems. By using the given information we are trying to come to the conclusion whether a person will have heart disease or not. Therefore, we are trying to solve this using supervised learning. These models will basically predict whether a person will have heart disease or not by taking the features of the provided dataset into account. For this purpose we have chosen three classifier models they are mentioned below:



1.	Logistic Regression:
Logistic regression is mainly used to predict categorical value.Logistic regression is a technique used for classification.Our dataset depends on two categorical variables that is presence and absence so binary classification it is.  logistic regression fits for our classification work better. In our dataset we have given 13 features and we want our models to predict whether a person will have heart disease in the future or not. Now on our dataset we have 13 features and we have also specified the target. So when we use this classifier logistic regression on our data set it should be able to classify and plot based on the features and predict whether our patient has a possibility of getting heart disease in the future.


2.	Decision Tree:
 
Decision tree is another popular model which is used to solve classification problems. When we apply this model on our dataset, firstly it creates a tree having root nodes, leaf nodes and decision nodes. For creating nodes it will calculate the entropy of any information gain. When it will create the node it will take the maximum information gain into account. Finally with the help of the decision tree this model will be able to classify whether the patient will have a heart condition in the future or not.


3.	Neural network: 

Neural Network is another algorithm which we used. It is a widely used algorithm. Neural networks have a wide array of uses in machine learning. For our classification purpose this is also a suitable algorithm. Neural Network’s learning is similar to the learning of human beings. There are several layers which facilitate the learning. For example the input layer, hidden layers, output layers. In our case we have set the number of hidden layers to 7 and number of maximum iteration to 1000. Usually the higher the number of iterations the higher the accuracy but in our case 7 is sufficient similarly if we lower the number of iterations then accuracy will decrease. It is considered as a data hungry algorithm the more data we feed the better it gets in terms of accuracy.



Results 

We have used three models : logistic regression, decision tree and neural network. We have seen differences in their accuracy. Firstly in logistic regression training accuracy of Logistic regression is: 0.86 and the test accuracy of Logistic regression is: 0.80. Secondly in decision tree training accuracy of Decision Tree Classifier is 1.00 and the Test accuracy of Decision Tree Classifier is 1.00. Thirdly in Neural network the training accuracy of Neural Network Classifier is 0.85 and the test accuracy of Neural Network is 0.83. Therefore we can see that the decision tree gives the highest accuracy, then logistic regression and finally neural network. But if we can use a higher amount of data surely the neural network will give higher accuracy.
