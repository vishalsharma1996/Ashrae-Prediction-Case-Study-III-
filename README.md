# Ashrae-Prediction-Case-Study-III-
EDA-->During this analysis of the meter readings is done for each site.Important observations were that the air temperature for 13 different sites was not in alignment with the local timestamp of the meter readings.Meter readings for site 0 and meter 0 have been started taken from May 20 2016 and readings before that needs to be removed.We have to remove buildings which are showing inconsistent or very high meter readings for the individual sites.

IMPUTATION AND FEATURE ENGINEERING-->After doing an indepth EDA we also found that the weather variables and building metadata are having missing values which needs to be imputed.The features which have more than 80 % missing data are dropped.Now for the remaining features median and interpolation method are used to fill the missing values.Now coming to the feature engineerig i have includeed features such as relative humidity,weekday,is_weekday,is_pub_holiday,busy_hours and basic time features such as day month and hour.Here i have also aligned the timestamp for all the 13 different sites.

MODEL AND HYPERPARAMETER TUNING-->Models which i have tried till now is LGBM,CATBOOST,XGBOOST AND RANDOMFOREST.Hyperparameter tuning is performed for each and every model.The model which performed best is the LGBM.Further I have also tried custom ensembling and simple multilayer perceptron models to compare with the previous model scores.

MODEL DEPLOYMENT-->Finally I have deployed my model using flask on google colab

FILE DESCRIPTION
Eda_for_Energy_Consumption.ipyb-->It contains the code for detailed data visualization

Final(1).ipynb-->It contains the final productionizable code which will predict the meter readings for four different types

LGBM_Base_Model(1).ipynb-->It contains the code for the base model used in the ensembling method and also the hyperparameter tuning

Meta_Model(1).ipynb-->It contains the code for the meta-model(LGBM) which uses the prediction of the base model in the ensembling method and also the hyperparameter tuning

Simple_MLP(1).ipynb-->It contains the code for the multilayer preceptron model along with its predictions on the test dataset

Test_Ensemble_predictions.ipynb-->It contains the code for the predictions on the test set on my final ensemble model

Test_Feature_Engineering_Imputation_1.ipynb-->It contains the code for filling the missing values and doing feature engineering on the test dataset

Test_Pred_LGBM_2.ipynb-->It contains the code for predictions on the test dataset using LGBM model

Test_Prediction_Catboost(1).ipynb-->It contains the code for predictions on the test dataset using CATBOOST model

Test_Prediction_RF.ipynb-->It contains the code for predictions on the test set using the RANDOM-FOREST model

Test_Prediction_XGBOOST.ipyb-->It contains the code for predictions on the test dataset using XGBOOST model

Test_Results_All_Models_Modified(1).ipynb-->It contains the code for comparison of predictions of all models on the test dataset

Train_Cleaned_Imputed(1).ipynb-->It contains the code for cleaning up the train data and filling up the missing values

Train_Feature_Engineering_1.ipynb-->It contains the code for feature engineering on the train dataset

Tuning_Catboost(1).ipynb-->It contains the code for hyperparameter-tuning of the CATBOOST model

Tuning_LGBM_2(1).ipynb-->It contains the code for hyperparameter tuning of LGBM model


Tuning_RFregressor(1).ipynb-->it contains the code for hyperparameter tuning for the RANDOM-FOREST Model

XGB_CATBOOST_Base_Model.ipynb-->It contains the code for base model and hyperparameter tuning of it to be used in the ensembling method.
