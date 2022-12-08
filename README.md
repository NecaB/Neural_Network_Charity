# Neural_Network_Charity

Overview 


This challenge was to predict the probability of success for applicants if they are funded by the charity program offered by Alphabet Soup Co. To determine the probability of success for these applicants we will utilize a neural network with Data Manipulation, create, train and test sets and then analyze the models that were created.

Results 

Data Processing 

To perform data processing, we identified the different columns in the dataset to determine their validity for the model.  Based on the objectives of this research it was decided that the EIN and NAME columns are unique identifiers to the different samples in the dataset but are of no value to the model as such they were removed. 

The variables that will be used in the model are: ‘STATUS’, ‘ASK_AMT’, ‘IS_SUCCESSFUL’, ‘APPLICATION_TYPE’, ‘CLASSIFICATION’, ‘USE_CASE’, ‘ORGANIZATION’, ‘INCOME_AMT’. 

The ‘USE_CASE’ column was also later removed from the dataset as it was insignificant to the model for predicting the probability of success.  

The Dependent variable is ‘IS_SUCCESSFUL’ as the objective of the model is to predict the probability with high accuracy. 

Compiling, Training, and Evaluating the Model

Attempt #1 

-	There are 2 Hidden Layers 
-	80 neurons are in Layer 1 and 30 neurons are in Layer 2
-	The Relu and Sigmoid activation functions are used because Relu is ideal for nonlinear datasets and Sigmoid is best for binary classification problems
-	The ‘EIN’ and ‘NAME’ columns are removed. 


<img width="468" alt="image" src="https://user-images.githubusercontent.com/109915684/206358640-863a9dc2-0325-44e2-b981-34d2f807577c.png">


 <img width="468" alt="image" src="https://user-images.githubusercontent.com/109915684/206358605-9b453f5d-f665-4dd9-87dc-350b9975d58a.png">
 

The accuracy for the model was 72%.  Hence, it did not achieve target model performance 


 <img width="468" alt="image" src="https://user-images.githubusercontent.com/109915684/206358574-15ba8474-8719-460f-a188-4eaf4129677e.png">


Attempt #2

-	There are 3 Hidden Layers
-	100 neurons are in Layer 1, 50 neurons are in Layer 2, 20 neurons are in Layer 3
-	The Relu and Sigmoid activation functions are used because Relu is ideal for nonlinear datasets and Sigmoid is best for binary classification problems
-	The ‘EIN’ and ‘NAME’ and ‘USE_CASE’ columns are removed. 

 <img width="468" alt="image" src="https://user-images.githubusercontent.com/109915684/206358531-ecd818f9-1a22-414e-8536-43906ce6065b.png">


 <img width="468" alt="image" src="https://user-images.githubusercontent.com/109915684/206358499-6a81145f-c861-4a8d-8c34-ccf767e54f17.png">


The accuracy for the model was 57%. Hence, it did not achieve target model performance.

<img width="468" alt="image" src="https://user-images.githubusercontent.com/109915684/206358477-1e445e90-de8a-43ae-a0be-e0583041422e.png">

 
Attempt #3

-	There are 3 Hidden Layers 
-	80 neurons are in Layer 1, 30 neurons are in Layer 2, 20 neurons are in Layer 3
-	The Relu activation functions are used because Relu is ideal for nonlinear datasets and Tanh is used in an attempt to achieve improved accuracy. 
-	The ‘EIN’ and ‘NAME’ and ‘USE_CASE’ columns are removed. 

 
 <img width="468" alt="image" src="https://user-images.githubusercontent.com/109915684/206358433-3ab41b62-28e9-41ff-92ba-1494ac8be728.png">


The accuracy for the model was 46%.  Hence, it did not achieve target model performance.

 
<img width="468" alt="image" src="https://user-images.githubusercontent.com/109915684/206358367-94ce2699-bf73-4afa-8499-4ce24317dbb5.png">

SUMMARY 

The model achieved a 46% accuracy score after optimization. This was lower than the initial 72% accuracy score of the neural network. This decline in accuracy may be because of overfitting the model. We could make additional attempts at increase accuracy by removing more columns that are of no value to the model or adding more data to the dataset used. Since the accuracy score was so poor a better model for predicting success with the applicants for Alphabet Soup charity maybe a Random Forest Classifier. A Random Forest Classifier is more robust and accurate due to their sufficient estimators and depth, they are also faster models and are better for avoiding overfitting. 
