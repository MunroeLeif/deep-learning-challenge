# deep-learning-challenge

# Overview
This analysis was performed for the fictional non-profit foundation Alphabet Soup in an effort to help them predict which applicants for their funding were the most likely to succeed.

# Results

  ## Data Preprocessing
  In preprocessing the data, I first removed the identification columns "EIN" and "NAME" as unnecessary data. Then I identified that the target(y) of the model is the variable "IS_SUCCESSFUL", and the features(X) were the rest of the dataset. For "APPLICATION_TYPE" and "CLASSIFICATION" columns it was necessary to bin thier rare categorical values together. Encoding of the categorical variables was done using pd.get_dummies(), resulting in a dataframe of 43 feature columns. Finally, I scaled the split data using the StandardScaler module. 
  
  ## Compiling, Training and Evaluating the Model
  Based on the given data, I decided a Sequential model would be the best fit and to start with rectified linear unit "relu" activation function. In compiling the model, I started with the Sequential model with two hidden layers. The first layer had 80 neurons and activation fuction "relu", and the second layer had 30 neurons and the activation function "relu"; the output layer had the activation fucntion "sigmoid" and the epochs were set to 100. This model resulted in an accuracy score of 72.4%
  -In order to try and achieve the target model performance of 75% accuracy, I first added more neurons to the second layer, bringing the number up to 80 from 30. This attempt resulted in an accuracy score of 72.5%. 
  -For my second attempt at optimization, I tried running the model for longer with 200 epochs instead of 100. This second attempt had an accuracy score of 72.54% - clearly more epochs were not helping the model learn. 
  -Finally, I added a third hidden layer, with 30 neurons and the activation function "relu". This last attempt at optimization, run for 200 epochs like the previous attempt, achieved a 72.8% accuracy score, the highest likely to be reached by changing these few parameters. 
  
# Summary
The highest accuracy score I was able to achieve with this model was 72.8%. Changing the hyperparameters did not result in much improvement of the model's performance - including the "NAME" column would give the model more information to work with, but is unlikely to produce drastic results given the size of the dataset that was provided. 
