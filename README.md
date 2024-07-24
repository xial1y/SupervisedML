# Beta Bank Customer Churn Prediction

**Project Description**: <br> Beta Bank, due to the gradual leaving of their clients, is interested in creating a machine learning model that will predict whether a customer will leave or stay with the bank since it is cheaper to retain a customer than to find a new one. This project aims to develop and compare various machine learning model to achieve this goal. The metric threshold that Beta Bank set for this project is F1 score of at least 0.59 and to also consider the AUC-ROC score. 

**Dataset**: <br> The dataset used in this project is given by the bank and it contains information about customers, including their credit score, geography, gender, age, tenure, balance, number of products, credit card ownership, active membership, and estimated salary. The dataset also includes information on whether each customer has exited the bank or not.

**Exploratory Data Analysis (EDA):** The dataset is preprocessed by <br>
1. Dropping unnecessary columns (RowNumber, CustomerId, Surname)
2. Handling missing values in the Tenure column by filling them with the mean value
3. One-Hot Encoding (OHE) categorical columns (Geography and Gender)

**Model Development:** ML models were created and trained <br>
1. Logistic Regression: A basic logistic regression model was trained using the training set and validated on the validation set. The F1 score was 0.4916 and the AUC-ROC score was 0.7537.
2. Logistic Regression with Upsampling: The minority class (clients who have exited) was upsampled to balance the classes. The F1 score was 0.4512 and the AUC-ROC score was 0.7203.
3. Logistic Regression with Downsampling: The majority class (clients who have not exited) was downsampled to balance the classes. The F1 score was 0.4601 and the AUC-ROC score was 0.7153.
4. Random Forest Classifier: A random forest classifier model was trained using the training set and validated on the validation set. The F1 score was 0.6246 and the AUC-ROC score was 0.8496.
5. Random Forest Classifier with Upsampling: The minority class (clients who have exited) was upsampled to balance the classes.  The F1 score was 0.6258 and the AUC-ROC score was 0.8479. 
6. Random Forest Classifier with Downsampling: The majority class (clients who have not exited) was downsampled to balance the classes. The F1 score was 0.6135 and the AUC-ROC score was 0.8510.
7. Decision Tree Classifier: A Decision Tree Classifier model was trained using the training set and evaluated on the validation set. The F1 score was 0.5551 and the  AUC-ROC score was 0.8126. 
8. Decision Tree Classifier with Upsampling: The minority class (clients who have exited) was upsampled to balance the classes. The F1 score was 0.5474 and the AUC-ROC score was 0.7859.
9. Decision Tree Classifier with Downsampling:  The majority class (clients who have not exited) was downsampled to balance the classes. The F1 score was 0.5764 and the AUC-ROC score was 0.8121.

**Results:** <br> The best-performing model s the Random Forest Classifier with upsampling. The model was tested with testing dataset and achieved an F1 score of 0.62 and AUC-ROC score of 0.86. 

**Conclusion:** <br> Beta Bank should employ an RandomForestClassifier with upsampling, if the data has class imbalance, model for client churn prediction. It produces the highest F1 score and good AUC-ROC meaning the model is pretty good at predicting if a client will leave while minimizing false positives (indicating a client will leave but actually stay).



