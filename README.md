# Credit Risk Analysis
## Overview
The purpose of this project is to employ machine learning techniques to predict credit card lending risk. The data is unbalanced as good loans outnumber risky loans so multiple appriaches were employed to determine which model is the most appropriate for determining credit risk.

## Results
<img width="748" alt="Summary" src="https://user-images.githubusercontent.com/85457256/135172904-df329df2-f3c3-4f04-9062-b2885e1d8ff7.png">

<img width="399" alt="confusion_matrixes" src="https://user-images.githubusercontent.com/85457256/135172922-2707cad4-e7da-4836-ba63-851737a332cc.png">
*The above images show data from the .ipynb files that are uploaded and are used as a means to consolidate the outputs.* 


Overall, the BalancedRandomForestClassifier has the highest balanced accuracy score of 0.95, while ClusterCentroids only has a score of 0.51 as shown in the first image.  Based on the images above summarizing the machine learning models' output for high credit risk predictions versus actual high credit risk...
- The EasyEnsembleClassifier model has the highest precision in predicting a high risk loan at 0.074, while ClusterCentroids has the lowest at 0.0052.
- The highest recall of 1.00 is achieved with the BalancedReandomForestClassifier model and the lowest is produced by the ClusterCetnroids at 0.586.  

Based on the images above summarizing the machine learning models' output for low credit risk predictions versus actual low credit risk...
- All of the models have a presicion of 1.00 which is likely explained by a larger sample of data from which to learn.  The sensitivity score, however, ranges from 0.43(ClusterCentroids) to 0.94 (EasyEnsembleClassifier).

## Summary
Having higher sensitivity in this project is more important than having higher precision.  This is becuase it is better to catch potential risks than determining from the model if every risk is classified correctly. In this way, a credit card lender is acting more conservatively and, therefore, more false positives (predicted high risk but actually low risk) are not going to be as much of a detriment to the lender as having less false negatives (predicted low risk but actually high credit risk). Thus, my recommendation is to use the BalancedRandomForestClassifier model as this achieves the highest sensitivity in determining credit risk, and it also achieved the highest accuracy score. 
