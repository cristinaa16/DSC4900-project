# DSC4900 - Predicting Hospital Readmission using Machine Learning Models

<h2>Description</h2>
Hospital readmissions are a growing concern for healthcare systems due to their financial cost and impact on patient outcomes. This project uses machine learning models and analytical techniques and assesses their effectiveness in predicting readmission outcomes. This project predicts hospital readmissions using demographic and clinical data from 130 hospitals between 1999–2008. I tested 3 machine learning models: Logistic Regression, Random Forest, and Gradient Boosting, focusing on AUC scores.
<br />


<h2>Languages and Utilities Used</h2>

- <b>Python</b> 
- <b>Tableau</b>

<h2>Dataset</h2>

- <b>https://www.kaggle.com/datasets/brandao/diabetes?select=diabetic_data.csv</b>
- Data from 1999–2008
- 130 U.S. hospitals
- Data from around 100,000 patients
- 50+ features: demographics, diagnoses, medications, procedures

Target Variable: 
- Original target: readmitted (<30, >30, NO) 
  - Re-encoded as: 
    - 1 = Readmitted (<30 or >30 days) 
    - 0 = Not readmitted ("NO")
<br />

<h2>Project walk-through:</h2>

Code contained in: 
Hospitalreadmission.ipynb, hospitalinpatient.twbx

Data cleaning:
- Replaced "?" with NaN
- Dropped ID columns and columns with excessive missing values

Feature engineering:
- Created binary target (readmitted_binary)

Dependencies: 
- pandas
- numpy
- scikit-learn
- matplotlib
- seaborn

Advanced Skills:
- Feature engineering (0.5)
- Logistic regression (0.5)
- Random forest (1)
- Gradient boosting (1)
- ROC AUC curves (1)
- Cross validation (0.5)
- Tableau (1)


**Results**:

Logistic Regression ROC:  <br/>
<img src="https://i.imgur.com/nvmJJi2.png" height="40%" width="40%" alt="Logistic Regression ROC model"/>

The logistic regression's ROC AUC curve shows the performance of the logistic regression model in distinguishing between patients who were readmitted versus not readmitted. The performance is better than random guessing, as shown by the AUC of 0.65, which is greater than 0.5.

Random Forest ROC: <br/>
<img src="https://i.imgur.com/0M9Vz8X.png" height="40%" width="40%" alt="Random forest ROC model"/>

When compared to logistic regression, the random forest model's ROC AUC curve shows better class separation than the logistic regression model with an AUC of 0.68. Initially, some overfitting was detected, which was addressed through hyperparameter tuning, and the final model achieved consistent AUC scores across training and testing datasets.

Gradient Boosting ROC:  <br/>
<img src="https://i.imgur.com/pahsXf7.png" height="40%" width="40%" alt="Gradient Boosting ROC model"/>

Out of all the models tested, Gradient Boosting performed the best with an AUC of 0.70. It showed the strongest ability to rank patients by their risk of readmission.

Feature Importance plot:  <br/>
<img src="https://i.imgur.com/JqgqHNR.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

This feature importance plot shows which patient characteristics had the greatest influence on the Gradient Boosting model’s ability to predict hospital readmissions. Variables such as number_inpatient, dicharge_disposition_id, diag_1, were among the strongest predictors.

- number_inpatient: the number of times a patient has been admitted to the hospital as an inpatient previously. More prior hospitalizations typically indicate worse health status and a higher likelihood of being readmitted.
- discharge_disposition_id: a code representing the type of discharge (e.g., discharged to home, transferred to another hospital, left against medical advice). A higher risk of readmission is linked to specific discharge types, such as being admitted to a nursing home.
- diag_1: the primary diagnosis recorded during the hospital visit. This feature captures the main reason for hospitalization (e.g., heart failure, diabetes complications). Specific diagnoses are highly predictive of readmission risk due to their severity.

Histogram of number of inpatient stays:  <br/>
<img src="https://i.imgur.com/md845ge.png" height="40%" width="40%" alt="Gradient Boosting ROC model"/>

According to this distribution of inpatient stays, the majority of readmitted patients had either zero or one previous inpatient visit. The likelihood of readmission clearly increases with the number of previous inpatient visits. Number_inpatient was one of the most important predictive features in my models because it implies that patients who are hospitalized more frequently may be at a higher risk of readmission in the future.

<br />
</p>

## Conclusion
  
Among the models tested, Gradient Boosting achieved the highest and most consistent performance, with an AUC of 0.70. Random Forest following with an AUC of 0.68 and Logistic Regression is the lowest performing model with an AUC of 0.65. From my feature importance chart, I identified key factors influencing readmission risk, such as prior inpatient admissions, discharge disposition, and the primary diagnosis.  


<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
