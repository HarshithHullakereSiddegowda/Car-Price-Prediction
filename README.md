# Car-Price-Prediction
The objective of this Project is to assist the sellers, buyers,  in the used car market. 

## objective
The objective of this project is to assist the sellers, buyers, 
in the used car market. Based on the information provided by the users, it 
may then provide a relatively accurate price estimate, understand what are all 
the attribute feature effect on the price of a car, selecting the right features 
which plays a significant role in predicting the price of a car. The dataset for 
automobile prices utilised in the study was obtained from kaggle. This dataset 
contains automobile pricing from year 1939 until 2020. The descriptive feature include 
This dataset has 17 features and 19237 observations in total. Target variable is continous 
numeric variable.


## Overview Of Methodology

We consider the following regression model to predict our target feature:

    1) KNN Regressor

    2) Decision Tree

    3) Random Forest Regressor

    4) Regression Models (Linear, Ridige, Lasso)

Our modeling strategy begins by transforming the full dataset cleaned in Phase 1. This transformation includes encoding categorical descriptive features as numerical and then scaling of the descriptive features. We first randomly sample 5K rows from the full dataset and then split this sample into training and test sets with a 70:30 ratio. This way, our training data has 3.5K and test data has 1.5K. To be clear, our terminology here is that

    1) The 3.5K rows of data used during the hyper parameter tuning phase is 
       called the training data.

    2) The 1.5K rows of data used during the performance comparison phase is 
       called the test data. 

Before fitting a particular classifier on the training data, we select the best feature using the powerful Random Forest Importance method inside a pipeline. we have search over 10, 20, and the full set of 17 features to determine which number of features works best with each classifier. Using feature selection together with hyper-parameter search inside a single pipline, we conduct a RepeatedStratified cross-validation to fine-tune hyper-parameters of each regressor using R2 and MAE as the performance metric. We build each model using parallel processing with "-2" cores. We also examine sensitivity of each model with respect to its hyperparameters during the search.

Regressor with the best set of hyper-parameter values as identified via grid search using the training data are called tuned Regressor. Once we identify the Four tuned Regressor( with the best hyper-parameter values), we 'fit' them on the test data using cross-validation in a paired fashion and we perform paired t-tests to see if any performance difference is statistically significant. In addition, we are comparing the regressor wit respect to their r2 and MAE scores and confusion matrices on the test data.


Overview Of Methodology

We consider the following regression model to predict our target feature:

    1) KNN Regressor

    2) Decision Tree

    3) Random Forest Regressor

    4) Regression Models (Linear, Ridige, Lasso)

Our modeling strategy begins by transforming the full dataset cleaned in Phase 1. This transformation includes encoding categorical descriptive features as numerical and then scaling of the descriptive features. We first randomly sample 5K rows from the full dataset and then split this sample into training and test sets with a 70:30 ratio. This way, our training data has 3.5K and test data has 1.5K. To be clear, our terminology here is that

    1) The 3.5K rows of data used during the hyper parameter tuning phase is 
       called the training data.

    2) The 1.5K rows of data used during the performance comparison phase is 
       called the test data. 

Before fitting a particular classifier on the training data, we select the best feature using the powerful Random Forest Importance method inside a pipeline. we have search over 10, 20, and the full set of 17 features to determine which number of features works best with each classifier. Using feature selection together with hyper-parameter search inside a single pipline, we conduct a RepeatedStratified cross-validation to fine-tune hyper-parameters of each regressor using R2 and MAE as the performance metric. We build each model using parallel processing with "-2" cores. We also examine sensitivity of each model with respect to its hyperparameters during the search.

Regressor with the best set of hyper-parameter values as identified via grid search using the training data are called tuned Regressor. Once we identify the Four tuned Regressor( with the best hyper-parameter values), we 'fit' them on the test data using cross-validation in a paired fashion and we perform paired t-tests to see if any performance difference is statistically significant. In addition, we are comparing the regressor wit respect to their r2 and MAE scores and confusion matrices on the test data.

![car](https://github.com/HarshithHullakereSiddegowda/Data__Visualization/assets/100402681/524196fe-b58e-43c4-b48e-d7c1baf4099f)


## Summary of Findings:

The RFI approach finds the most relevant characteristics, allowing the Random Forest model to focus on the factors that have the most influence when generating predictions.The Random Forest Regressor has a better r2 score, showing its capacity to successfully collect and generalise patterns in previously unexplored data.the entire dataset has the potential to reduce overfitting.Models trained on a bigger dataset may have superior convergence qualities and produce more consistent and interpretable results.

On the training data, the Random Forest Regressor with the top ten features chosen using the Random Forest Importance (RFI) technique has the greatest cross-validation r2 score. Furthermore, when tested on real-world data, the Random Forest Regressor outperforms the KNN Regressor, Decision Tree, and Regression models (Linear, Ridge, Lasso) in terms of r2 score. Working with the complete dataset, on the other hand, has the potential to minimise overfitting and provide models that are easier to train and comprehend.

## Conclusions:

The study intends to uncover the essential factors that significantly contribute to forecasting automobile prices by analysing this information. The project attempts to give insights and assistance for used vehicle vendors and consumers by utilising machine learning models and data analysis approaches.

The case study intends to equip users with relevant information that may assist in making educated decisions about the price and purchase of used automobiles by meeting the objectives described above.In essence, the research strives to connect the dots among automotive industry, data analysis, and artificial intelligence models. By employing these methods, the project aims to equip users with an all-encompassing comprehension of the aspects that influence car prices, empowering them to make more informed pricing and purchasing choices.


