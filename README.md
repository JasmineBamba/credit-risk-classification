# Credit Risk Classification Analysis

## Introduction to Supervised Machine Learning

Supervised machine learning is a type of algorithm that learns patterns from labeled training data, then makes predictions or identifications when provided with new, unlabeled data. In this method, the model is trained on a dataset where the correct outputs are known and learns to predict the outcome from new data.

![image](https://github.com/JasmineBamba/credit-risk-classification/assets/135666038/76321420-f251-41fa-8f5c-046171b70b8c)



## Table of Contents

- [Project Overview](#project-overview)
- [Steps Taken:](#steps-taken)
- [Splitting the Data into Training and Testing Sets](#splitting-the-data-into-training-and-testing-sets)
- [Logistic Regression Model Creation](#logistic-regression-model-creation)
- [Evaluation of Model Performance](#evaluation-of-model-performance)
- [Results:](#results)
- [Conclusion](#conclusion)

 
## Project Overview

The purpose of this project is to build and evaluate a supervised machine learning model for credit risk classification using historical lending data from a peer-to-peer lending services company. The model is designed to identify the creditworthiness of borrowers, distinguishing between 'healthy loans' (0) and 'high-risk loans' (1).

![image](https://github.com/JasmineBamba/credit-risk-classification/assets/135666038/f7aa7a24-0e6c-4ff2-a12d-0f0be2584177)


### Steps Taken:

#### Splitting the Data into Training and Testing Sets

- The lending_data.csv dataset was loaded into a Pandas DataFrame.
![image](https://github.com/JasmineBamba/credit-risk-classification/assets/135666038/00390a6a-fea7-4577-86b6-88e3accea607)

- Labels (y) were created from the “loan_status” column, distinguishing between healthy (0) and high-risk loans (1).
- Features (X) were formulated from the remaining columns.
- The data was divided into training and testing sets using the train_test_split method.
![image](https://github.com/JasmineBamba/credit-risk-classification/assets/135666038/d943e4fc-b469-4cb1-a088-6db32faf1374)


#### Logistic Regression Model Creation

- A logistic regression model was fitted using the training data.
- Predictions were made for the testing data labels using the trained model.
  
Model 1:

![image](https://github.com/JasmineBamba/credit-risk-classification/assets/135666038/0c9023d4-1f1c-4863-ab22-ef29cfc71cc6)

Model 2:

![image](https://github.com/JasmineBamba/credit-risk-classification/assets/135666038/0ae5023d-ebbb-4121-8c4c-00f9f7016f61)


#### Evaluation of Model Performance

- Confusion matrix was generated.
- Classification report was created to assess precision, recall, and accuracy scores.


Model 1:

![image](https://github.com/JasmineBamba/credit-risk-classification/assets/135666038/933f9f8f-1106-4797-871e-81554001f0a6)


Model 2:

![image](https://github.com/JasmineBamba/credit-risk-classification/assets/135666038/bd1e0813-72ec-48c7-a86c-9dc285c90b1c)



### Results:

Model 1
  
- **Accuracy Score:** 0.9520479254722232
- **Precision Score:** Healthy Loans: 1 , High-Risk Loans: 0.85
- **Recall Score:** Healthy Loans: 0.99 , High-Risk Loans: 0.91

Model 2

- **Accuracy Score:** 0.9936781215845847
- **Precision Score:** Healthy Loans: 1, High-Risk Loans: 0.85
- **Recall Score:** Healthy Loans: 0.99 , High-Risk Loans: 0.91

### Summary of Analysis:

Both Model 1 and Model 2 demonstrate similar and robust performance in credit risk assessment. These models achieve high accuracy scores of 99%, indicating their proficiency in distinguishing between 'healthy loans' and 'high-risk loans'. Moreover, the precision and recall metrics for both loan classes (0 and 1) remain consistent across both models, showcasing a strong ability to correctly classify loans.

The precision of 0.85 and recall of 0.91 for 'high-risk loans' in both models imply a good balance between correctly identifying actual high-risk loans and minimizing false negatives. These metrics are crucial, especially in the context of lending, where the accurate prediction of high-risk loans is pivotal to prevent potential losses.

## Conclusion

Based on the analysis:

**Preferential Use of Model 2:** Given its equivalent performance and the emphasis on correctly predicting high-risk loans, Model 2 is recommended due to its oversampling technique, making it a slightly better choice for credit risk assessment.

**Continuous Refinement:** While the logistic regression model demonstrates exceptional performance, it's prudent to continuously improve the model. Enhancing the dataset further, especially by adding more high-risk loan data, could potentially refine the model's accuracy and robustness.

**Real-time Validation and Pilot Testing:** Deploy the chosen model in a controlled setting to classify loan statuses in real time. This real-world pilot project will allow the model to be tested, evaluated, and potentially fine-tuned based on real data inputs.

In conclusion, the logistic regression model, particularly Model 2, is recommended for credit risk assessment. Its ability to accurately distinguish loan categories, especially high-risk loans, coupled with continuous refinement strategies, ensures a reliable tool for lenders in making informed decisions and mitigating risks in the lending process.
