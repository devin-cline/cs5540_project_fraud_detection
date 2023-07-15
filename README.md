# cs5540_project_fraud_detection

This project is to implement fraud detection using different machine learning techniques in a big data architecture.

Two datasets were explored and are listed below. Ultimately, dataset 1 was chosen for simplicity of input.

dataset 1 from https://www.kaggle.com/datasets/jainilcoder/online-payment-fraud-detection
dataset 2 from https://www.kaggle.com/datasets/kartik2112/fraud-detection

The src folder contains the source code for the models and preprocessing of the two different datasets.

The trained models folder contains the output of the trained models that were chosen to be implemented in the big data architecture. The three selected were:
1. DecisionTreeClassifier from grid_search_smote.ipynb ('DecisionTreeClassifier.pkl')
2. RandomForestClassifier from grid_search_smote.ipynb ('RandomForestClassifier.pkl')
3. XGBClassifier from xgb_1_class_weight.ipynb ('xgb.pkl')

Two different techniques were explored to handle the class imbalance in the data. 
1. compute_class_weight from scikit-learn
2. SMOTE

Pyspark models were explored but due to poor performance and limited time to try and solve and improve, others were chosen.

GridSearchCV was implemented to try and find the best model using a variety of parameters. If there was more time to work on the project, it would have been great 
to explore more parameters and to use GridSearchCV with both methods for handling class imbalance. Due to limited time and computing power, GridSearchCV 
was implemented only using SMOTE and with a small variety in the parameters.  

GridSearchCV provided well-performing models for DecisionTreeClassifier and RandomForestClassifier but the XGBClassifier performed much better using 
compute_class_weight for handling class imbalance and using default parameters.

Those three models are used...
