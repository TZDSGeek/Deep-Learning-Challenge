# Neural Network Model Report

## Overview
The purpose of this analysis was to create a machine learning model that can accurately predict if applicants will be successful if funded by the company Alphabet Soup.

## Results

### Data Preprocessing 
*	The target or dependent variable for my model was the Is_Successful column.
*	The features for my model were a combination of the rest of the columns (excluding the target variable) and the columns with string data types converted to binary values by applying the Pandas get dummies function. I established cut off points for several columns to either bin or remove data with low value counts.
*	I removed the EIN and name columns from the input data, because they were specific to each company and had no correlation with applicant success.

### Compiling Training, and Evaluating the Model
*	Before my initial testing, I used a Keras tuner to determine the best hyperparameter configuration. Here were the optimum parameters per the Keras tuner, I used these in my first round of testing and achieved a model accuracy of 72%.

![image](https://github.com/TZDSGeek/Deep-Learning-Challenge/assets/137857956/781c5e48-a163-4787-a415-516797377d87)

After several hours of testing and hyper parameter tuning, I decided to use 3 hidden layers with a relu activation function for each layer, the first hidden layer contained 9 neurons, the second hidden layer contained 7 neurons, the third hidden layer contained 8 neurons. I selected these hyper parameters because the model achieved the highest accuracy and optimal convergence when they were applied. 

![image](https://github.com/TZDSGeek/Deep-Learning-Challenge/assets/137857956/d368d2ce-da54-4273-b73a-e614960b9c90)

![image](https://github.com/TZDSGeek/Deep-Learning-Challenge/assets/137857956/92579ae7-419a-451e-a1f0-ad63434b05b0)

*	My model was not able to reach the targeted accuracy of 75%, but I was able to improve its accuracy to 73%.
*	To improve the model’s accuracy, I added a third hidden layer, experimented for several hours with different counts of neurons applied to each layer, and the number of epochs in each test. I also added more training data by changing the split of training and testing data.

![image](https://github.com/TZDSGeek/Deep-Learning-Challenge/assets/137857956/1051a0e5-8e70-4c5e-832d-2b4cc908c75d)

## Summary
Although this model’s accuracy has been improved, I would not recommend it for production. The model converges around 15 to 20 epochs, indicating that it is learning efficiently from the training data. The number of epochs used to train the model was adjusted to 100 to prevent overfitting. With more dedicated time and resources, the model has potential to meet and even exceed its targeted accuracy. Another model that could be recommended would be random forest algorithm, it would create multiple simple trees assigned to smaller portions of the data and when combined would create a strong classifier with a minimal risk of overfitting the model.
