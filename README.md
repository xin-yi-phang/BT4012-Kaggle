# BT4012-Kaggle
Kaggle Competition for BT4012

As I have split my workflow up into separate files, please find the directory below

Final submission:
* `e1138548.ipynb`: Final submission code, producing the 2 selected submissions

Other files in home directory:
* `EDA.ipynb`: Preliminary EDA
* `final_testing.ipynb`: to check that the final submission code's output matches the submission

Part 1: Retrospective labelling (`\retrospective_label`):
* `data_prep.ipynb`: data processing (three levels of data processing: keep as raw vs drop highly correlated/low variance / fully process with skew treatment and scaler)
* `model_compare_dataset.ipynb`: compare performance of several models (Logistic Regression, CatBoost, LightGBM, KNN, Random Forest, MLP Classifier) on the 3 levels of data processing
* `model_hyperparam_tune_log_loss.ipynb`: tuned hyperparameters for the 6 models scoring on log-loss
* `model_hyperparam_tune_pr_auc.ipynb`: tuned hyperparameters for the 6 models scoring on pr-auc
* `model_hyperparam_tune_ensemble.ipynb`: tuned hyperparameter weights for the best log-loss and best pr-auc model
* `soft_laeblling.ipynb`: deploying the best ensemble model to label the NA rows and storing them

Part 2: Forward Classification (`\forward_classify`):
* `window_hyperparam.ipynb`: selecting the best validation split (rolling vs expanding w recency weights)
* `soft_label_weight_tune.ipynb`: selecting the best soft label weight, confidence cutoff, and weighting method
* `forward_facing_predict_weight_tune.ipynb`: (did not proceed as results were bad), selecting the best forward predicting weight andconfidence cut off
* `model_hyperparam_tune.ipynb`: hyperparameter tuning selected models (LightGBM, XGBoost, ExtraTrees)
* `final_predict_code.ipynb`: predicting test data with best performing model and its hyperparameters (LightGBM)
* `final_predict_code_ensemble.ipynb`: predicting test data with the best performing ensemble weights