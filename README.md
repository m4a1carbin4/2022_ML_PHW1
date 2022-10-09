# 2022_ML_PHW1
Machine learning subject PHW1 assignment results for the second semester of 2022

# **Program description for PHW 1 programming task.**

# Data

**The dataset used in this function is in the form of a Python pandas data frame.**

- Used Dataset = **Breast Cancer Wisconsin (Diagnostic) Data Set**
    - link : [https://archive.ics.uci.edu/ml/datasets/breast+cancer+wisconsin+(diagnostic)](https://archive.ics.uci.edu/ml/datasets/breast+cancer+wisconsin+(diagnostic))

# Function 1 : make_model

```python
def make_model(K,data,case,**kwargs):
```

- args : K = K_value for Kfold , data = pandas.dataframe for training, case = input switch for model selection, kwargs = args for classification model
    - According to the case argument input, one of decision tree, logistic, and svm classification models are created and the classification_compare function is executed based on the generated model.
    - Users can input model parameters for model training in a Python dictionary way(**kwargs)
    - Returns the return value(Model Accuracy Score array) of the classification_Compare function.

# Function 2 : classification_Compare

```python
def classification_Compare(data,model,K):
```

- Args: data = pandas.dataframe for training, mode = classification model , K = K_value for Kfold
    - It trains the training data on the model input as a factor, validates the trained model, and returns the model's accuracy score.
    - The training data input as a factor is classified into training and validation datasets through the K-fold method. (Factor K is used as input for this K-fold.)
    - There is also an additional model validation process for the dataset that has been preprocessed through the min_max scale for the training data.
    - Returns an array of model accuracy scores for each training and validation dataset generated in a K-fold.

1. Team Member Contribution
    
    201835543 한수민 33%
    
    202035512 김지수 33%
    
    202035540 전효빈 33%
