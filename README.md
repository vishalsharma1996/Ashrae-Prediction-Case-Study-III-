# Ashrae-Prediction-Case-Study-III-
EDA-->During this analysis of the meter readings is done for each site.Important observations were that the air temperature for 13 different sites was not in alignment with the local timestamp of the meter readings.Meter readings for site 0 and meter 0 have been started taken from May 20 2016 and readings before that needs to be removed.We have to remove buildings which are showing inconsistent or very high meter readings for the individual sites.

IMPUTATION AND FEATURE ENGINEERING-->After doing an indepth EDA we also found that the weather variables and building metadata are having missing values which needs to be imputed.The features which have more than 80 % missing data are dropped.Now for the remaining features median and interpolation method are used to fill the missing values.Now coming to the feature engineerig i have includeed features such as relative humidity,weekday,is_weekday,is_pub_holiday,busy_hours and basic time features such as day month and hour.Here i have also aligned the timestamp for all the 13 different sites.

MODEL AND HYPERPARAMETER TUNING-->Models which i have tried till now is LGBM,CATBOOST,XGBOOST AND RANDOMFOREST.Hyperparameter tuning is performed for each and every model.The model which performed best is the LGBM.Further I have also tried custom ensembling and simple multilayer perceptron models to compare with the previous model scores.

MODEL DEPLOYMENT-->Finally I have deployed my model using flask on google colab


