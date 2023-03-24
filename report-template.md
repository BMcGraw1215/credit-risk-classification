# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
* Explain what financial information the data was on, and what you needed to predict.
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
* Describe the stages of the machine learning process you went through as part of this analysis.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * The model was more accurate for predicting lower risk loans than higher risk loans, likely due to sample size. 
  * The model also doesn't fit the HR loans as closely, with an f1 score of only .88. 
  * The Confusion Matrix showcases a large amount of False Positives/Negatives, which could be concerning with the small sample sizes for HR Loans.
  * The Balanced Acc score shows .95, which is okay, and acceptable but not great for definitive results. (I'd trust this model for healthy, but not HR loans)

* Machine Learning Model 2:
  * The 2nd model shows largely the same information as the 1st one, however the HR loans show a better fit to the model. 
  * The Confusion Matrix shows significantly less FP/FNs (only 2/3rds!), likely attributed to the better fit of the HR Loans.
  * The Balanced Acc score shows .99, showing good promise.
  
## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* The second Model looks to perform better, showcasing better scores all around. most significant to me would be the Confusion Matrix values, and the increase in the F1-score. 
* The Healthy Loans were predicted well to begin with, so the HR Loans were the ones in question. 

* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )
  * I'd say it does depend, but it's equally important to accurately predict "0s" vs "1s". Being too accurate leads to issues as seen in this example, with Healthy loans performing "perfect" in both examples, when in reality some of them were HR loans. This is exacerbated by the lack of HR Loans' sample size.
  * for this reason, I'd recommend and accept the second model, but still look for a better fitting model due to the HR Loans not being completely accurate.