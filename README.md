# Credit_Risk_Analysis
Using supervised machine learning to assess credit risk


## Overview of Analysis
This analysis was commishened by LendingClub (client) to a peer-to-peer lending service that is looking to add some 
supervised machine learning to its lending analysis portfolio. They have commishened us to determine the most effective
algorithm to use in their future lending assessment. Those algorithms are as follows:

- RandomOverSamlper
- SMOTE
- ClusterCentroids
- SMOTEENN
- BalancedRandomForestClassifier
- EasyEnsembleClassifier

## Resources
This analysis was performed using
- Jupyter Notebook 6.4.12
- Data found here

## Results
The results of the analysis will be placed in ascending order, culminating with the algorithm that has highest scores.
A screen shot of the accuracy scores and classification reports will be included for each algorithm.

### ClusterCentroids

![screenshot of clustercentroids accuracy score](https://github.com/dh4rt/Credit_Risk_Analysis/blob/main/images/us_accuracy.png)

![screen shot of clustercentroids classification](https://github.com/dh4rt/Credit_Risk_Analysis/blob/main/images/us_classification.png)
- The accuracy score is 54% which is not good.
- The precision score is low for for high_risk loans and high for low_risk loans.
- The recall scores do little to inspire any added confidence. With lower scores in this field indicating a 
greater portion of false negatives.

### RandomOverSampler

![screenshot of randomoversampler accuracy score](https://github.com/dh4rt/Credit_Risk_Analysis/blob/main/images/nro_accuracy.png)

![screenshot of randomoversampler classification](https://github.com/dh4rt/Credit_Risk_Analysis/blob/main/images/nro_classification.png)

- The accuracy score is 64.6% a full ten percentage points better than last place and still underwhelming.
- the precision score are again very low for high_risk and very high for low_risk.
- the recall for both categories is better with low_risk recall being 18% better than previous but still missing 
what amounts to four of ten.

### SMOTEENN

![screenshot of SMOTEENN accuracy] (https://github.com/dh4rt/Credit_Risk_Analysis/blob/main/images/teen_accuracy.png)



![screenshot of SMOTEENN classification] (https://github.com/dh4rt/Credit_Risk_Analysis/blob/main/images/teen_classification.png)
- Has an accuracy score of 64.8% a marginal increase on the previous algorithm.
- The precision score follow the same pattern of low for high_risk and high for low_risk.
- The recall scores for both categories only moved one point in either direction for both risk levels. Meaning that while
better for the high_risk category it is a touch worse for the low_risk category but is overall a bit better, than previous.

### SMOTE


![screenshot of SMOTE accuracy] (https://github.com/dh4rt/Credit_Risk_Analysis/blob/main/images/smote_accuracy.png)


![screenshot of SMOTE classification] (https://github.com/dh4rt/Credit_Risk_Analysis/blob/main/images/smote_classification.png)

- Has an accuracy score of 65.8% an entire percentage point high than previous.
- The precision scores remain so far unchanged.
- The recall scores here are significantly better for low_risk and worse for high_risk which is an unnerving prospect,
but the improved accuracy score does lend some greater confidence.

### BalancedRandomForestClassifier


![screenshot of brfc accuracy] (https://github.com/dh4rt/Credit_Risk_Analysis/blob/main/images/brfc_accuracy.png)


![screenshot of brfc classification] (https://github.com/dh4rt/Credit_Risk_Analysis/blob/main/images/brfc_classification.png)

- Has an accuracy score of 77.8% which is a huge improvement over previous.
- The precision score improved slightly for the high_risk borrowers and remained high for the low_risk category.
- The recall scores are where a huge improvment as well, the high_risk score still needs work but the low_risk is now
approaching a realm that instills confidence.

### EasyEnsembleClassifier


![screenshot of eec accuracy] (https://github.com/dh4rt/Credit_Risk_Analysis/blob/main/images/eec_accuracy.png)


![screenshot of eec classification] (https://github.com/dh4rt/Credit_Risk_Analysis/blob/main/images/eec_classification.png)

- The highest accuracy score of the bunch with 92.3% a score further from second place than second is to fifth.
- The precision scores are better overall.
- The recall scores are where this algorithm truly shines. Remember higher recall scores means lower chance of a false
negative.

## Summary
When considering all of the resuts in totality it is important to remember that these numbers have been scaled between 0
and 1, with scores closer to 1 indicating more successful measures. The precision and recall scores are also judged by
the same scoring, with that in mind it is clear to see that the EasyEnsembleClassifier is the best option for the client
to use going forward. They should however reassess routinely, as new techniques can be developed.
