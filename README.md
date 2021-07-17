# Credit Risk Analysis
Machine learning analysis of good vs risky loans

## Overview:

The purpose of this analysis is to test different supervised machine learning
techniques for accuracy in predicting whether a loan is high or low risk. Specifically,
we want to be able to detect high risk loans with high accuracy. We want this test
to be more precise than sensitive because we don't want to decline too many people who
pay back their loans. A bank makes money on loans, so we don't want to turn away
business unnecessarily, nor do we want to offend people/make it more difficult for
them to get loans in the future due to a machine learning decline. 

## Results:

### Accuracy, recall, and precision scores

Recall and precision are taken from the classification report, a sample of which
is seen below

!["Classification Report]()

* Naive Random Oversampling
	* Accuracy: .64
	* Precision: .99
	* Recall: .67
* SMOTE Oversampling
	* Accuracy: .65
	* Precision: .99
	* Recall: .64
* Undersampling - Cluster Centroids
	* Accuracy: .54
	* Precision: .99
	* Recall: .40
* SMOTEENN Sampling
	* Accuracy: .54
	* Precision: .99
	* Recall: .40
* Balanced Random Forest Classifier
	* Accuracy: .80
	* Precision: .99
	* Recall: .88
* Easy Ensemble AdaBoost Classifier
	* Accuracy: .90
	* Precision: .99
	* Recall: .89

## Summary:

The Easy Ensemble AdaBoost Classifier is the best algorithm for determining 
high or low risk loans, but both ensemble learners performed well. This algorithm
combines many low accuracy models to create one high accuracy model. This process
works by iterating through classifications models. The computer learns which classifiers
give low accuracy, so the next iteration doesn't use that. After a number of iterations,
there is a model that uses the most accurate classifications to train the model with.
With a 90% accuracy rate, this would be a great filter for banks to use before deeply reviewing
any loan applications. 
