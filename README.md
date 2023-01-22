# Credit_Risk_Analysis
## Overview
The purpose of this project is to use machine learning and a variety of algorithms to predict credit risk. The data used is from LendingClub, a peer-to-peer lending services company. The data is imbalanced, with a vast majority of the data being low risk. The data is cleaned and then split into training and testing data. The data is then run through a variety of algorithms to determine which is the most accurate. The algorithms used are: RandomOverSampler, SMOTE, ClusterCentroids, SMOTEENN, BalancedRandomForestClassifier, EasyEnsembleClassifier.

## Results
### Naive Random Oversampling
- The balanced accuracy score is 61.7%
- The precision for high risk is 1%
- The recall for high risk is 63%
- The precision for low risk is 100%
- The recall for low risk is 62%
<img width="759" alt="Fig1a" src="https://user-images.githubusercontent.com/109715441/213896349-eb23b5cd-ee1b-4a6b-be4b-681b15a0a43c.png">
<img width="826" alt="Fig1b" src="https://user-images.githubusercontent.com/109715441/213896357-4e979346-d84d-47ac-85f7-a3917ece033d.png">


### SMOTE Oversampling
- The balanced accuracy score is 62.1%
- The precision for high risk is 1%
- The recall for high risk is 54%
- The precision for low risk is 100%
- The recall for low risk is 70%
<img width="846" alt="Fig2a" src="https://user-images.githubusercontent.com/109715441/213896377-527e138d-92b8-4aa5-835e-4e50b34dfd9b.png">
<img width="823" alt="Fig2b" src="https://user-images.githubusercontent.com/109715441/213896384-0e3169c4-41db-435a-8bd4-35b5dbe37783.png">



### Undersampling: Cluster Centroids
- The balanced accuracy score is 50.6%
- The precision for high risk is 0%
- The recall for high risk is 48%
- The precision for low risk is 100%
- The recall for low risk is 53%
<img width="826" alt="Fig3a" src="https://user-images.githubusercontent.com/109715441/213896409-9fd0868a-8a00-48c6-9b29-1e98ffdef66c.png">
<img width="893" alt="Fig3b" src="https://user-images.githubusercontent.com/109715441/213896417-fb90f2b5-6f01-4fbc-81b7-a30a46c9fe8f.png">

### Combination Sampling: SMOTEENN
- The balanced accuracy score is 62.7%
- The precision for high risk is 1%
- The recall for high risk is 63%
- The precision for low risk is 100%
- The recall for low risk is 62%
<img width="975" alt="Fig4a" src="https://user-images.githubusercontent.com/109715441/213896466-631f72d2-bba5-4492-8a49-72d395541c9b.png">
<img width="962" alt="Fig4b" src="https://user-images.githubusercontent.com/109715441/213896467-97bbb3b9-ecc4-462f-9ddc-6174170a8a20.png">

### Balanced Randon Forest Classifer
- The balanced accuracy score is 78.8%
- The precision for high risk is 3%
- The recall for high risk is 70%
- The precision for low risk is 100%
- The recall for low risk is 87%
<img width="864" alt="Fig5" src="https://user-images.githubusercontent.com/109715441/213896491-f592b6b6-4d61-4ad4-a948-1ca7590f9bb6.png">

### Easy Ensemble AdaBoost Classifer
- The balanced accuracy score is 93.2%
- The precision for high risk is 9%
- The recall for high risk is 92%
- The precision for low risk is 100%
- The recall for low risk is 94%
<img width="869" alt="Fig6" src="https://user-images.githubusercontent.com/109715441/213896507-527b8edd-9544-49f1-8378-57703550bd13.png">

## Summary
Overall, most of the machine learning models do not preform particularly well. All 6 of the models had a precision rate of 100% for low risk, as precision is a measure of how reliable a positive classification is, this means that the models were able to correctly predict low risk 100% of the time. However, for this data this statistic is irrelevant. As the data is extremely imbalanced, with about 0.5% of the data being high risk, even if a model predicted all high risk as low risk, the precision rate would still be 100%.

Both of the oversampling models had recall rates from between 54%-70% and only 1% precision rate for high risk. Both of their balanced accuracy scores were around 62%. While this accuracy score is not particularly good, their precision rate for high risk also disqualifies them as usable models.

The undersampling model using cluster centroids had a high risk recall rate of 48%, a low risk recall rate of 53% and a high risk precision rate of 0%. With an even worse balanced accuracy score of 50.6%, this model is also not usable.

The final resampling model, SMOTEENN, which is a combination of over and under sampling, had a high risk recall rate of 63%, a low risk recall rate of 62% and a high risk precision rate of 1%. With a balanced accuracy score of 62.7%, this model is also not usable.

Finally, both ensemble models had a significant improvement over the resampling models. While both precision rates for low risk were still 100%, the balanced random forest classifier had a high risk recall rate of 70%, a low risk recall rate of 87% and a high risk precision rate of 3%. With a balanced accuracy score of 78.8%, this model is much better than the previous, but did not preform quite as well as the final model.

The easy ensemble AdaBoost classifier had a high risk recall rate of 92%, a low risk recall rate of 94% and a high risk precision rate of 9%. With a balanced accuracy score of 93.2%, this model is the best of the 6 models. With a balanced accuracy score of 93.2%, this is the best model of the 6 models. While other models not explored here may have a higher precision rate for high risk, of the 6 models here, this can be recommended as the best model to use.
