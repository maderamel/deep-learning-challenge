# deep-learning-challenge

# Overview

Alphabet Soup, a nonprofit foundation, wants a machine learning tool to predict the success of funding applicants. They provided a dataset containing various features related to the applicants. The goal is to create a binary classifier that predicts whether an applicant will succeed if funded by Alphabet Soup. 

# Results

- Data Preprocessing

   - ***What variable(s) are the target(s) for your model?*** 
Y represents the target array, which contains the output variable. It corresponds to the "IS_SUCCESSFUL" column in the application_df_clean DataFrame.

  - ***What variable(s) are the features for your model?***
X represents the feature matrix, which contains the input variables. It is obtained by dropping the columns ["APPLICATION_TYPE", "AFFILIATION", "USE_CASE", "ORGANIZATION", "INCOME_AMT", "SPECIAL_CONSIDERATIONS"] from the application_df_clean DataFrame, leaving behind the variables that the model will focus on. The features are: ["STATUS", "ASK_AMT", "CLASSIFICATION_C1000", "CLASSIFICATION_C1200", "CLASSIFICATION_C2000", "CLASSIFICATION_C2100", "CLASSIFICATION_C3000", "CLASSIFICATION_Other"]

  - ***What variable(s) should be removed from the input data because they are neither targets nor features?***   
These variables should be removed: ["APPLICATION_TYPE", "AFFILIATION", "USE_CASE", "ORGANIZATION", "INCOME_AMT", "SPECIAL_CONSIDERATIONS"] from the application_df_clean DataFrame, leaving behind the variables that the model will focus on.

- Compiling, Training, and Evaluating the Model

  - ***How many neurons, layers, and activation functions did you select for your neural network model, and why?***
I chose 2 neuron layers and activation functions. I chose to use the Sigmoid Function because it is useful for binary classification problems. 
I chose the ReLU (Rectified Linear Unit) because it is one of the most widely used activation functions. ReLU is  efficient and helps mitigate the vanishing gradient problem, which the Sigmoid function suffers from. 
 
  - ***Were you able to achieve the target model performance?***
I was able to achieve the target model performance.

  - ***What steps did you take in your attempts to increase model performance?***
My model seemed to function well initially, so I did optimization testing to see if changes would impact accuracy and loss to ensure I chose correctly. 

# Summary

The model achieved high accuracy in predicting the success of funding applicants for the nonprofit foundation Alphabet Soup. By using a binary classifier and leveraging various features from the provided dataset, the model demonstrated the ability to predict whether applicants would be successful if funded. 

### Recommendation

A Random Forest classifier could be a suitable alternative to the deep learning model. Random Forest combines multiple decision trees to make predictions. Here's why Random Forest could be a good choice:

- Harder to Overfit: Random Forest models are less prone to overfitting, especially when there are many irrelevant features in the dataset. They tend to generalize well even with less data. I think I may have had an overfitting issue in my model, so a random forest approach may have mitigated that problem. 

- No Feature Scaling Required: Random Forest is not sensitive to the scale of the features. It can handle both numerical and categorical features without the need for extensive feature scaling. I may have has issues scaling in my model, so avoiding that hurdle would be beneficial. 

Further analysis is required to determine if the neural network was the best fit or if another model such as Random Forest would be a better fit. 

