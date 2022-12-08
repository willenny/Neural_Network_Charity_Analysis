# Neural_Network_Charity_Analysis

## Overview

Using skills in preprocessing data, machine learning, and neural networks, we will use the features in the provided dataset to creat a binary classifier that is able to predict whether or not applicants will be successful if funded by Alphabet Soup. After preprocessing the dataset, we will consider how many inputs there are before determining the number of neurons and layers in your model. Lastly, we will compile, train, and evaluate the neural network model

## Resources
Data Source: charity_data.csv <br />
Software: Python, Jupyter Notebook

### Results
- Data Preprocessing
  - The variable that is considered the target for our model is IS_SUCCESSFUL because we are attempting to predict whether an applicant is successful after being funding by Alphabet Soup.
  - The variables that are considered features in our model are APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT because they will be used by the machine learning model to help predict if the applicant is successful.
  - The variables that are neither targets nor features are EIN and NAME because they hold no measureable values that would help the machine learning model. 
- Compiling, Training, and Evaluating the Model
  - Two layers were used with first layers having 8 neurons and the second layer having 6 neurons. The activation function for the first and second layer is relu and the output layer is using the sigmoid activation function. It was suggested that the layers should contain 2 or 3 times more neurons than the amount of inputs but given that their were 43 inputs after preprocessing, using over 80 neurons seems like too much. So i kept it simple to avoid overfitting. 
  - I was not able to achieve tha target model performance of 75%. I achieved 72.57% accuracy.
  - I added a third layer with 2 neurons. I switch the activation function on the first layer to tanh.


### Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and explain your recommendation.

Overall, the deep learning model was able to predict whether an applicant that receives funding from Alphabet Soup would be successful approximately 72% of the time. Depending on the standards that Alphabet Soup sets for itself, that may or may not be strong enough to make their decision. I would suggest using another machine learning model to compare to the neural network. A logistical regression model can analyze continous and cateforical variables and helps predict the probability of the input belonging to one of two groups. Since our data is continous and categorical, this model is promising. Also, Alphabet Soup can choose a predetermine cutoff to assign each sample into two groups, IS_SUCCESSFUL and IS_NOT_SUCCESSFUL.
