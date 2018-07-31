# Train & test model

## Steps
The model training, test and analysis parts of this study was using Python (version 3.6.2), these process can be divided into four steps as shown as below:
1. Load group A and B for training and test respectively.  
2. Scaled the ultrasonic characteristic parameters of the training data to [0, 1], and the test data was scaled according to the scaling method of the training data as the features of machine learning to avoid result be leaded by features with large values, and classified as negative and positive by using the strict criteria of donating liver, 10% of steatosis as the label required for supervised learning.  
3. C was used to weigh the desire of the relationship between the maximum margin and the noise tolerance, γ was the parameters for adjusting the complexity of the model. From the parameter space such as {C = 2^−5, 2^−3, …, 2^15, γ = 2^−15, 2^−13, …, 2^3, degree = 1, 2, 3}, the optimal values are obtained by a grid search method to train the SVM using LeaveOneOut cross-validation on training data.  
4. The confusion matrix and ROC curve were plotted through the test results and used to generate diagnostic evaluation parameters to aid analysis.

## Simple code description 
1.I had use StratifiedKFold (10) & LeaveOneOut for training model, show in folder "10Fold for Pathology _ NPathology" & "LOO for Pathology_NPathology".  
2. Code title of "1" to "7" is the rough parameter setting.  
3. Code title of "'1" to "'7" is the fine parameter setting.
4. [Bar plot](https://github.com/Lance0218/Fatty-liver-classifier/blob/master/SVM/LOO%20for%20Pathology_NPathology/Bar%20plot.ipynb): comparison of single and multi-features of each diagnostic evaluation parameter.  
