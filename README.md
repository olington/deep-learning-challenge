# deep-learning-challenge
Challenge 21

OVERVIEW

The aim of this analysis is to develop a binary classifier through the application of deep learning methods, with the objective of predicting the success of organizations or entities funded by Alphabet Soup. The primary objective is to construct a model capable of accurately discerning whether the allocated funding resulted in success or not.

RESULTS
1.	Data Preprocessing:
o	What variable(s) are the target(s) for your model?
y = numeric_df["IS_SUCCESSFUL"].values
o	What variable(s) are the features for your model?
X = numeric_df.drop(["IS_SUCCESSFUL"],1).values
o	What variable(s) should be removed from the input data because they are neither targets nor features?
application_df = application_df.drop(columns=["EIN","NAME"])
2.	Compiling, Training, and Evaluating the Model:
The refined model consisted of an increased three concealed layers with 80, 40, and 20 neurons, respectively in contrast with the 2 hidden layers in the first trial. I employed the 'relu' activation for the hidden layers due to its efficiency, while 'sigmoid' was chosen for the output layer as taught in class and aligning with its suitability for binary classification. The peak accuracy attained on the test however was approximately 73.06%.
SUMMARY
The deep learning model that was created exhibited moderate success, achieving an accuracy of approximately 73.2% in forecasting the proficient utilization of funds by organizations. While demonstrating promise, there is scope for enhancement to reach the intended accuracy goal of 75%. 
A change in the number of epochs could help improve accuracy. Tinkering with the activation function might also help in increasing accuracy scores. 
Also, with its capacity to manage non-linear relationships and offer insights into feature importance, opting for a Random Forest Classifier presents a noteworthy alternative. This model demonstrates lower susceptibility to overfitting and tends to be more interpretable, aligning well with Alphabet Soup's requirements for comprehending and forecasting successful funding applications
