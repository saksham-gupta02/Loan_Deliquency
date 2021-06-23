# Loan_Deliquency
What if we can predict who will return the loan on time and who doesn't ? Great na, we can minimize the bank loss.
Given Data of loan borrower we need to predict who will pay the installment on time and who might skip. Its a huge burden on bank when someone doesn't pay the loan back. Sometimes its just delay in paying installment while there are some who took a huge amount of money and run away.

Approach
-	Data – Preprocessing and Recursive Feature Engineering
-	First loaded the training data
-	Checked for missing Values but found none.
-	Then checked for the categorical and numerical features
-	There are 3 columns containing categorical data (source, financial_institution and loan_purpose)
-	Tried Multiple ways.
-	Convert categorical data into (1,2,3) ex:  source X as 1 ,Y as 2 and Z as 3 (Masking)
-	Same tried for financial institution and loan purpose
-	That didn’t work so tried with one hot encoding for source , financial institution and loan purpose

Recursive Feature engineering
-	Tried different model with masking features dividing data into 80-20 ratio
-	Logistic Regression
-	Decision Tree
-	Random Forest Classifier
-	Adaboost classifier
-	Gradient descent algo
-	KNN
-	XGBOOST
-	Tried all these above models with one hot encoding and found a better result
-	Then proceeded with one hot encoding
-	And tried multiple ways by omitting few features.
-	And Dropped the few features for further processing.(which were giving the low f1-score)
-	And checked the f1 score for the model.

Then Finally worked with the Key features where I was getting the maximum f1-score and train the model on XGboost classifier with all the training data.
- Then loaded the test data and pre-process It into the same data(features) on my model was trained.
-	Ex: one hot encoding with categorical data and omitted the features which was not included in the features used to train the model.
-	Final using predict method predicted the values and converted those into a csv file.






