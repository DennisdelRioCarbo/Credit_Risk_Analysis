# Credit_Risk_Analysis

## Overview 

In this project we  apply machine learning to solve a real-world challenge: credit card risk.

Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, we'll employ different techniques to train and evaluate models with unbalanced classes. We'll use imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.

Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, we’ll oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then, we’ll use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, we’ll compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. Once  done, we’ll evaluate the performance of these models and make a written recommendation on whether they should be used to predict credit risk.

## Results: Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all six machine learning models. Use screenshots of your outputs to support your results.

- **RandomOverSampler**

![image](https://user-images.githubusercontent.com/104289098/187091507-208f3234-a087-4b69-8ab2-9bd63284339b.png)

  - *Balanced accuracy score*: **0.65 Low**
  - *Precision*: High precision for low risk 1.00, extremely low precision for high risk 0.01
  - *Recall*: Low recall for low risk, low recall for high risk.

- **SMOTE Oversampling**

![image](https://user-images.githubusercontent.com/104289098/187091583-619ad4fd-00d9-4e78-8f6d-ca00a3fcb9ac.png)

  - *Balanced accuracy score*: **0.66 Low**
  - *Precision*: High for low risk 1.00, extremely low for high risk 0.01.
  - *Recall*: Low for both high risk and low risk.

- **Undersampling (ClusterCentroids)**

![image](https://user-images.githubusercontent.com/104289098/187091611-9a64f122-ab82-4e92-a0f8-12c6212350cc.png)

  - *Balanced accuracy score*: **0.54** Low
  - *Precision*: High for low risk 1.00, extremely low for high risk 0.01.
  - *Recall*: Low for both high and low risk.

- **Combinatorial SMOTEENN**

![image](https://user-images.githubusercontent.com/104289098/187091639-2ae6627e-56e4-45ab-ad3d-3e7d6bc6756f.png)

  - *Balanced accuracy score*: **0.67 Low**
  - *Precision*: High for low risk, extremely low for high risk.
  - *Recall*: Low for both high and low risk.

- **BalancedRandomForestClassifier**

![image](https://user-images.githubusercontent.com/104289098/187091669-0afc88b1-db3c-46e6-970c-1220f0734229.png)

  - *Balanced accuracy score*: **0.79 Low**
  - *Precision*: High for low risk, low for high risk.
  - *Recall*: high for low risk low for high risk.

- **EasyEnsembleClassifier**

![image](https://user-images.githubusercontent.com/104289098/187091696-a61fc28e-8611-409f-81f8-85d62df4490a.png)

  - *Balanced accuracy score*: **0.93 High**
  - *Precision*: High for low risk, extremely low for high risk.
  - *Recall*: High for both high and low risk.


## Summary: Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. If you do not recommend any of the models, justify your reasoning.
