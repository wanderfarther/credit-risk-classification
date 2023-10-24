# credit-risk-classification
# Module 12 Report
## Overview of the Analysis

The prupose of this analysis was to create a model that could accurately and confidently predict whether a loan was at a high-risk of defaulting. The data included the loan size, interest rate, borrower information including income, debt to income ratio, number of accounts they hold, number of derogatory marks, the total debt of the borrower, and the health of the loan (0 = healthy, 1 = high risk of defaulting). I used this data to predict whether or not the loan was at risk for default. The training data had 75,036 healhty classified loans and 2,500 high risk loans. Using this data, I trained a logistic regression model to see how accurately it would predict if a loan was at risk of default. This gave us a good look at how accurate the model could be and at what threshold we began to have such a high "positive" prediction rate, we would get many false postives. This was possible due to the imbalanced amount of data. Using the RandomOverSampler module, I was able to resample the data with more evenly weighted positive and negative data. After this resampling, I ran the new data through the model and found that it report fewer false positives than the first model. 

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Logitistic Regression Model 1:
	* Accuracy: 95.2%
		This model had a high accuracy rate.
	* Precision: 
		* Healthy: 1.00
		This model predicted if a loan was healhty 100% of the time compared to the predicted healhty loans.
		* High Risk: 0.85
		This model predicted if a loan was at risk 85% of the time compared to the predicted high risk loans.
	* Recall: 
		* Healthy: 1.00
		This model accurately predicted if a loan was healhty 100% of the time compared to the actual number of healhty loans.
		* High Risk: 0.91
		This model accurately predicted if a loan was healhty 91% of the time compared to the actual number of high risk loans.

* Logitistic Regression Model 2:
	* Accuracy: 99.3%
		This model had a higher accuracy rate than the first model.
	* Precision: 
		* Healthy: 1.00
		This model predicted if a loan was healhty 100% of the time compared to the predicted healhty loans.
		* High Risk: 0.84
		This model predicted if a loan was at risk 84% of the time compared to the predicted high risk loans.
	* Recall:
		* Healthy: 1.00
		This model accurately predicted if a loan was healhty 100% of the time compared to the actual number of healhty loans.
		* High Risk: 0.99
		This model accurately predicted if a loan was healhty 99% of the time compared to the actual number of high risk loans.

## Summary

Model 2 performs the best out of the two models. It was ever so slightly worse at precisely predicting if a loan was at risk, but it reduced the number of falsely classifying a high risk loan as a healthy loan. Both models have a 100% precision of identifying the healthy loans, so the only differeing factor in these models is the number of falsely identified high risk loans there are. If a company was tyring to make sure that it did not ignore loans that became high risk, they would want a model that accurately predicts healthy loans, but also does not inaccuratley classify an at risk loan for a healthy loan. Although if a company was only interested in finding healthy loans and didn't mind a few high risk loans gettin wrongfully classified, they might prefer model 1. 
