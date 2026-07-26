# Predicting Heart Failure (An example of Binary Classification case)

[You can read the Medium Article here!](https://apricitea.medium.com/an-introduction-to-machine-learning-predicting-heart-failure-using-binary-classification-and-a992c585b92d)

## Data Source

The current version of the dataset was elaborated by Davide Chicco (Krembil Research Institute, Toronto, Canada) and donated to the University of California Irvine Machine Learning Repository under the same Attribution 4.0 International (CC BY 4.0) copyright in January 2020. A detailed description of the dataset can be found in the Dataset section of the following paper: Davide Chicco, Giuseppe Jurman: "Machine learning can predict survival of patients with heart failure from serum creatinine and ejection fraction alone". BMC Medical Informatics and Decision Making 20, 16 (2020).

[The dataset can be accessed here!](https://archive.ics.uci.edu/ml/datasets/Heart+failure+clinical+records)

## Preprocessing 

- Check for missing value: no missing value in the dataset, therefore no imputation is needed.
- Performing Z-score Standardization on all the predictor variables using StandardScaler in ScikitLearn library.
- Check for the label proportion: There label class is imbalanced. Synthetic minority oversampling technique (SMOTE) is used to solve imbalanced data.
- Splitting data into train-test set for model validation.

## Classification Model

The classification model used in this project is KNN (which is a simple, easy-to-understand classification method for beginner). Looping will be performed (with max possible K = 30) to decide which K has the lowest error rate. Model will be validated using the test dataset and several metrics like Confusion Matrix and Classification Report available at Metrics in Scikit Learn library. 

## Result

- We obtained 0.64 recall score for the dataset that uses SMOTE (more than 0.5)
- The dataset that used SMOTE to solve imbalanced label class has better recall and f1-score. 
- Using SMOTE for this dataset increases the recall score from 0.14 to 0.64.
- Would be cool to use several different classification method to compare their performance (e.g: Logistic Regression, Naive Bayes, Decision Tree, etc.)

## Reference

Chicco D, Jurman G. 2020. Machine learning can predict survival of patients with heart failure from serum creatinine and ejection fraction alone. BMC Medical Informatics and Decision Making 20, 16.
