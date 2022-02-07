# Prediciton Student Study Period

**Problem**\
-Based on data until 2021, the level of student study period in master X is relatively late\
-The impact is related to accreditation and the quality of related study programs\

**Solution**\
-Utilizing data to predict student study period\
-The study period is for semesters 3, 4, 5, and 6

**Dataset**\
-Taken from the admission selection of prospective students\
-There are 97 rows and 24 columns (features)\
-Distribution for each class is 11:41:36:11

**Methodology**\
-*random forest* as the main machine learning algorithm\
-*synthetic minority over-sampling technique* is used for *resampling dataset*\
-*random forest - recursive feature elimination (RF-RFE)* used for feature selection\
-*particle swarm optimization* is used for *hyper-parameter optimization*

**Result**\
-*Resampling* using SMOTE gives additional dataset to 160 rows\
-Implementation of RF-RFE feature selection provides the most optimal results when using 20 of the 23 available features\
![alt text](https://i.ibb.co/GCQBXLb/RF-RFE.png)

-*Hyper-parameter tuning* using *particle swarm optimization* produces the following values
| *hyper-parameters Tuning* | *Value*  |
| :---:   | :-: |
| *boostrap* | *true* |
| *max_depth* | None  |
| *max_features* | 2 |
| *min_samples_leaf* | 2 |
| *min_samples_split* | 5  |
| *n_estimators* | 162 |

-The results of the *Random Forest Classifier* (RFC) are as follows\
![alt text](https://i.ibb.co/r2bJrjL/Screenshot-2022-02-07-113010.png)

-Performance improvements over the addition of other algorithms are as follows\
![alt text](https://i.ibb.co/864LgFN/Screenshot-2022-02-07-113116.png)

-Comparison with other algorithms is as follows\
![alt text](https://i.ibb.co/n8RzkkY/Screenshot-2022-02-07-113259.png)

**Limitation**\
-Increasing the number of data rows as the number of graduates increases\
-Explore other heuristic methods such as genetic algoritm, ant colony, and so on
