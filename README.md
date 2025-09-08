# 💊 High-Risk Polypharmacy Identification & Drug Load Prediction

This project focuses on identifying patients at risk of **polypharmacy** (≥5 prescribed drugs) and predicting **drug load** and **ICU length of stay** using the MIMIC-IV clinical dataset.  
It was developed as part of my MSc in Artificial Intelligence & Deep Learning.


## 🔍 Research & Technical Questions

- **Can machine learning models accurately identify patients at risk of polypharmacy?**  
  ✔️ Yes. The Random Forest Classifier achieved good performance in identifying patients with ≥5 prescribed drugs.  
  - Precision for high-risk patients: **0.33**  
  - Recall: **0.97** (very strong at capturing nearly all high-risk cases)  
  - F1-score: **0.49**  
  → The model is highly sensitive in detecting polypharmacy risk, although precision can be improved with further feature engineering or sampling strategies.

- **Which clinical and demographic features are most predictive of drug load?**  
  ✔️ The most informative predictors included:  
  - **Number of diagnoses per admission**  
  - **Length of stay in hospital**  
  - **Age group and gender**  
  - **Diagnosis groups (ICD-based)**  
  - **ICU stay count**  
  → These features strongly correlate with increased medication count.

- **Can ICU length of stay be predicted from patient-level features to support hospital resource allocation?**  
  ✔️ Yes. A Random Forest Regressor provided reliable predictions:  
  - **MAE (Mean Absolute Error): ~1.55 days**  
  - **MSE (Mean Squared Error): ~19.8**  
  - **R² Score: ~0.73**  
  → The model predicts ICU stay duration with solid accuracy, helping anticipate resource demand.
 

---

## 🛠️ Tools & Technologies

- **Languages**: Python (Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn)  
- **Models**: Random Forest Classifier & Regressor, Pipelines with preprocessing  
- **Data Source**: MIMIC-IV (Medical Information Mart for Intensive Care) – de-identified patient EHRs  
- **Platform**: Google Colab  

---

## 📊 Example Visualizations & Results

### Drug Count Distribution
![Drug Count Distribution](https://github.com/mbakos95/High-Risk-Polypharmacy-Identification-Drug-Load-Prediction/blob/main/Drug%20Count%20Distribution.png?raw=true)

### Polypharmacy Class Balance
![Polypharmacy Flag Distribution](https://github.com/mbakos95/High-Risk-Polypharmacy-Identification-Drug-Load-Prediction/blob/main/Polypharmacy%20Class%20Balance.png?raw=true)

### Top 10 Diagnosis Groups
![Top 10 Diagnoses](https://github.com/mbakos95/High-Risk-Polypharmacy-Identification-Drug-Load-Prediction/blob/main/Top%2010%20Diagnosis%20Groups.png?raw=true)


---

## 🔒 Data Privacy

The project uses **MIMIC-IV**, which contains **de-identified** healthcare data.  
Due to data use agreements, **raw data cannot be shared** in this repository.  
Notebooks and code are included so results can be reproduced with authorized access to MIMIC-IV.  

---

## 👨‍💻 Author

**Christos Zampakos**
Master’s in Artificial Intelligence & Deep Learning (AIDL01)
GitHub: [mbakos95](https://github.com/mbakos95)

