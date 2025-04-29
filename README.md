# DSC4900 - Predicting Hospital Readmission using Machine Learning Models

<h2>Description</h2>
Hospital readmissions are a growing concern for healthcare systems due to their financial cost and impact on patient outcomes. This project uses machine learning models and analytical techniques and assesses their effectiveness in predicting readmission outcomes. This project predicts hospital readmissions using demographic and clinical data from 130 hospitals between 1999–2008. I tested 3 machine learning models: Logistic Regression, Random Forest, and Gradient Boosting, focusing on AUC scores.
<br />


<h2>Languages and Utilities Used</h2>

- <b>Python</b> 
- <b>Tableau</b>

<h2>Dataset Used </h2>

- <b>https://www.kaggle.com/datasets/brandao/diabetes?select=diabetic_data.csv</b> 

<h2>Program walk-through:</h2>

<p align="center">
Logistic Regression ROC:  <br/>
<img src="https://i.imgur.com/NpyUnYp.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<br />
The logistic regression's ROC AUC curve shows the performance of the logistic regression model in distinguishing between patients who were readmitted versus not readmitted. The performance is better than random guessing, as shown by the area under the curve (AUC), which is greater than 0.5.
<br />
Random Forest ROC: <br/>
<img src="https://i.imgur.com/ZOG0KEJ.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<br />
When compared to logistic regression, the random forest model's ROC AUC curve shows better class separation than the logistic regression model with an AUC of 0.69. Initially, some overfitting was detected, which was addressed through hyperparameter tuning, and the final model achieved consistent AUC scores across training and testing datasets.
<br />
Gradient Boosting ROC:  <br/>
<img src="https://i.imgur.com/5FpO8p0.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<br />
Out of all the models tested, Gradient Boosting performed the best. With an average AUC of  0.70
<br />
Wait for process to complete (may take some time):  <br/>
<img src="https://i.imgur.com/LBcmk6H.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
This feature importance plot shows which patient characteristics had the greatest influence on the Gradient Boosting model’s ability to predict hospital readmissions. Variables such as number_inpatient, dicharge_disposition_id, number_diagnoses, were among the strongest predictors.
<br />
number_inpatient: the number of times a patient has been admitted to the hospital as an inpatient previously. More prior hospitalizations typically indicate worse health status and a higher likelihood of being readmitted.
<br />
discharge_disposition_id: a code representing the type of discharge (e.g., discharged to home, transferred to another hospital, left against medical advice). A higher risk of readmission is linked to specific discharge types, such as being admitted to a nursing home.
<br />
number_diagnoses: the total number of different diagnoses recorded for a patient during their hospital stay. Patients with multiple diagnoses often have more complex health conditions, increasing their chance of readmission.
<br />
</p>

## Conclusion
  
Among the models tested, Gradient Boosting achieved the highest and most consistent performance, with an AUC of 0.70. Random Forest followed closely with an AUC of 0.69 and Logistic Regression is the lowest performing model with an AUC of 0.66. From my feature importance chart, I identified key factors influencing readmission risk, such as prior inpatient admissions, discharge disposition, and the number of diagnoses.  


<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
