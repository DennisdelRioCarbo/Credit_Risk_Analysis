# Credit_Risk_Analysis

## Overview 

In this project we  apply machine learning to solve a real-world challenge: credit card risk.

Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, we'll employ different techniques to train and evaluate models with unbalanced classes. We'll use imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.

Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, we’ll oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then, we’ll use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, we’ll compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. Once  done, we’ll evaluate the performance of these models and make a written recommendation on whether they should be used to predict credit risk.

## Results

- **RandomOverSampler**
   - *Balanced accuracy score*: **0.65 Low**
  - *Precision*: High precision for low risk 1.00, extremely low precision for high risk 0.01.
  - *Recall*: Low recall for low risk, low recall for high risk.
   
![image](https://user-images.githubusercontent.com/104289098/187091507-208f3234-a087-4b69-8ab2-9bd63284339b.png)


- **SMOTE Oversampling**
  - *Balanced accuracy score*: **0.66 Low**
  - *Precision*: High for low risk 1.00, extremely low for high risk 0.01.
  - *Recall*: Low for both high risk and low risk.
  
![image](https://user-images.githubusercontent.com/104289098/187091583-619ad4fd-00d9-4e78-8f6d-ca00a3fcb9ac.png)


- **Undersampling (ClusterCentroids)**
  - *Balanced accuracy score*: **0.54** Low
  - *Precision*: High for low risk 1.00, extremely low for high risk 0.01.
  - *Recall*: Low for both high and low risk.

![image](https://user-images.githubusercontent.com/104289098/187091611-9a64f122-ab82-4e92-a0f8-12c6212350cc.png)


- **Combinatorial SMOTEENN**
  - *Balanced accuracy score*: **0.67 Low**
  - *Precision*: High for low risk, extremely low for high risk.
  - *Recall*: Low for both high and low risk.
   
![image](https://user-images.githubusercontent.com/104289098/187091639-2ae6627e-56e4-45ab-ad3d-3e7d6bc6756f.png)


- **BalancedRandomForestClassifier**
  - *Balanced accuracy score*: **0.79 Low**
  - *Precision*: High for low risk, low for high risk.
  - *Recall*: high for low risk low for high risk.

![image](https://user-images.githubusercontent.com/104289098/187091669-0afc88b1-db3c-46e6-970c-1220f0734229.png)


- **EasyEnsembleClassifier**
  - *Balanced accuracy score*: **0.93 High**
  - *Precision*: High for low risk, extremely low for high risk.
  - *Recall*: High for both high and low risk.
  
![image](https://user-images.githubusercontent.com/104289098/187091696-a61fc28e-8611-409f-81f8-85d62df4490a.png)


## Summary 
- Most models have low *Balanced accuracy scores* which means they are not very good at predicting the classes except for **EasyEnsembleClassifier** .
- Except for **EasyEnsembleClassifier** the rest of the models rank low for *precision* and *recall* for *high risk* meaning they are not detecting high risks and when they do they are not detecting it accurately.
- Most models have high *precision* for *low risk* with low *precision* for *low risk* and low *recall* for both classes. This all translates in failing to detect high risks.

## Recommendation
The **EasyEnsembleClassifier** model is the only on that has high *balanced accuracy score*, with high *recall* for both high and low risk, high *precision* for *low risk* and and low *precision* for *high risk*. This is the most precise and maybe most dependable model of all but not without a trade off. It detects accurately which risks are high and which risks are low, but out of the high risks it predicts only 10% turn out to be true. 
