# Fatty Liver Assessment Using Ultrasound Multi-features Based on Machine Learning

## Abstract
　　Fatty liver is a disease which excess fat accumulates in the liver. If it is not improved through a healthy diet and exercise as early as possible, it may become terminal liver diseases such as cirrhosis and cancer. Pathology was considered as the gold standard method of diagnosing fatty liver in the past, but due to its invasive side effects and controversies, it was gradually replaced by non-invasive medical imaging diagnosis. Considering price, safety and convenience, ultrasound is the most suitable diagnostic tool.  
　　But there are many limitations in traditional ultrasonic parameters which make it not suitable in most circumstances. In view of this, we extracted three different physical characteristics of ultrasound tissue characteristics parameters from the original signal to help diagnosing the fatty liver, including the integrated backscatter (IB, a measure of backscatter signal intensity), the Q factor of the Hilbert-Huang transition (Q factor , a new parameter for observing frequency decay), and the homogeneity factor (HF, a new parameter for quantifying fat evenness).  
　　However, the single parameter still has its limitations in physical meaning; therefore we use the three kernel functions of the support vector machine in machine learning as an algorithm to combine the above three parameters (features), attempting to break the limitations by combining multiple features. Groups A (111 samples) and B (74 samples) are used as training and test data in machine learning respectively, and 10% steatosis is used to judge whether it was a significant fatty liver.  
　　The results show that the extracted parameters also have a good ability to judge fatty liver in their respective performances. Except for sensitivity, all diagnostic parameters can be improved by combining multiple features. The accuracy of identification between normal and fatty patients come to 86.49%, and the area under the ROC curve reach to 0.8929. Also, we find the two combinations of features that are suitable to assist in suspecting and excluding disease respectively. This study provides a method for judging fatty liver with high versatility, low computational complexity, and high accuracy with developing potential in the diagnosis of fatty liver and good clinical application value.  

## Data analysis steps
The analysis process of this study can be summarized into six steps:   
1. Remove the data without label, and let the scores made by different pathologists change into same form.  
2. Three different physical meaning parameters are extracted from the ultrasonic original signal as features. (In MATLAB)  
3. Features are represented by graphics for easily observe and analyze.  
4. The parameters of the group A and the corresponding steatosis values are used as training data to establish the model.  
5. The parameters of the group B and the corresponding steatosis values are used as test data to judge whether the model was good or bad.  
6. The test results were analyzed by statistical methods.  

## Simple code description
Here are just some brief description, please see the code below for details:
1. [Cases recorded](https://github.com/Lance0218/Fatty-liver-classifier/blob/master/Cases%20recorded.ipynb): sort out and display data.  
2. [Effect of different scaling type](https://github.com/Lance0218/Fatty-liver-classifier/blob/master/Effect%20of%20different%20scaling%20type.ipynb): show the influence of different data scaling method.  
3. [Scatter plot](https://github.com/Lance0218/Fatty-liver-classifier/blob/master/Scatter%20plot.ipynb): observe the relationship between feature and steatosis or feature and other feature.  
4. [Box plot](https://github.com/Lance0218/Fatty-liver-classifier/blob/master/Box%20plot.ipynb): observe the relationship between feature and steatosis in several stages.  
5. [SVM](./SVM): bulid & test model, then calculate confuse matrix & ROC curve. & calculate several diagnostic evaluation parameter.  
6. [Bar plot](https://github.com/Lance0218/Fatty-liver-classifier/blob/master/SVM/LOO%20for%20Pathology_NPathology/Bar%20plot.ipynb): comparison of single and multi-features of each diagnostic evaluation parameter.  
