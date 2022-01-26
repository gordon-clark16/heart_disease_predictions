## Using Survey Responses to Predict Heart Disease

This repository takes a dataset containing survey responses collected by the CDC in an effort to predict heart disease or attack.

# EDA

This dataset is the largest we have worked with to date, containing 22 columns with 253, 680 rows. It was largely pre-cleaned, with the exception of duplicated rows. The duplicates were dropped and the cleanliness of the dataset was confirmed. We then visually explored the data using Matplotlib to find that our target was very imbalanced. There are two classes in our target vector, with the negative class containing 89.67% of the values. With further exploration, we uncovered trends for correlations to the target.  Diabetes, High Blood Pressure, and Stroke were some of our strongest indicators to heart disease or attack, as shown in the visuals below.

![image](https://user-images.githubusercontent.com/91917998/151103958-7cdb764e-3a6c-48df-a888-3e19935d2f6f.png)

![image](https://user-images.githubusercontent.com/91917998/151103994-b5aa5c00-163a-4222-aed0-b71e02856d76.png)

![image](https://user-images.githubusercontent.com/91917998/151104018-15988a0d-b41b-41ae-b24a-40a8e28e6e4f.png)

# Modeling

To deal with the large class imbalance, we utilized RandomUnderSampler from imblearn to create a new dataset that had a perfectly balanced target vector. We then used this new dataset to train several models for general performance before tuning and re-testing Logistic Regression and XGBOOST. Our final model is that tuned XGBOOST, which achieved 81% accuracy in predicting heart disease or attack. Our XGBOOST also achieved the best results in false negatives (19%), which is the primary error of concern in this use. This model would be most suited for risk reduction, as it is not yet accurate enough to deliver clinical diagnosis. Below is the confusion matrix for our XGBOOST, where 0 is the negative class and 1 is the positive class, HeartDiseaseorAttack.

![image](https://user-images.githubusercontent.com/91917998/151105657-4fcbeff2-3ec6-4148-aaa0-50b03153413b.png)

# Deliver Results

After modeling, presentations were made for both technical and non-technical audiences. This is intended to imitate presenting both to supervisors (technical) and potential stakeholders/executives (non-technical). These slide decks explored both the EDA and modeling aspects of our project, and are attached in the reposition for reference.
