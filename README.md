# credit_risk_analysis
## overview
Provided with a dataset by LendingClub, we were asked to build out several different algorithms for predicting credit risk.  Utilizing imbalanced learn and scikit learn libraries, we had three general approaches of prediction: resampling, combination of over/undersampling, and ensemble learners. Resampling methods include Naive Over Sampling, Smote Oversampling and Undersampling. The comnination sampling was performed using SMOTEEN.  The Ensemble learning methods include balanced randome forest classifier and the adaboost classifier.  The overall goal of all these methods was to find the most efficient tool for classification of the data provided. Classification being, provided features and a target, the tool will be able to determine whether or not there is credit risk. Ideally, they would like to find low credit risk opportunities.

## results
We will be looking at the accuracy score, precision and recall to determine the methods ability to classify the data appropriately.
Accuracy can be described as the methods ability to correctly predict the credit a low or high risk.(TP +TP)/(TP+TN+FP+FN)
Precision can be described as the methods ability to reliably classify as high risk.(TP as a % of TP and FP)
Recall can be described as the methods ability to successfully identify high risk credit (TP / (TP+FN))

naive random oversampling
>accuracy score: 64.5%
>high risk precision:
>low risk precision: .99
>recall: .69

SMOTE Oversampling
>accuracy score: 65.4%
>high risk precision:.01
>lowrisk precision: 1.0
>recall: .66

Undersampling
>accuracy score: 52.9%
>high risk precision:.01
>low risk precision: 1.0
>recall: .45

SMOTEEN combination
>accuracy score: 61.5%
>high risk precision: .01
>low risk precision: 1.0
>recall: .54

Balanced Random Forrest
>accuracy score: 78.7%
>hgih risk precision: .04
>low risk precision: 1.0
>recall: .91

ADABOOST
>accuracy score: 93.1%
>high risk precision:.04
>low risk precision: 1.0
>recall: .91


## Summary
While there are clear differences in these methods ability to classify information, one must also consider which of these summary statistics are most relevant to the goal at hand: which is to determine if there is credit risk. For this company, it is much more important to successfully identify low credit risk opporunities.  This can determined by looking at the low risk precision.  With all these methods having a 99% or 100% low risk precision (reliability of the classification), we will have to look deeper into the summary stats.  Recall would tell us whether or we successfully identified all low risk opportunities.  Looking at all these methods, the ensemble methods of random forrest and ADABOOST were drastically better at this at 91%. The final distinguisher would be accuracy, which ADABOOST reigns supreme at 93.1%.  These could be successful tools for identifying low risk opportunies, but absolutely terrible at identifying high risk.  
