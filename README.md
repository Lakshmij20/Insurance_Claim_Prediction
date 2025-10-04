# 🚗 Insurance Claim Prediction  

This project builds a **machine learning classification model** to predict whether a customer will file an insurance claim during the policy period.  
It combines **data preprocessing, exploratory data analysis (EDA), multiple ML models, and business recommendations** to support insurance companies in risk management, pricing strategies, and customer engagement.  

---

## 🎯 Objective  
- Predict the likelihood of a customer filing an insurance claim.  
- Identify the most important customer, vehicle, and policy-related features driving claim risk.  
- Compare multiple machine learning models and select the most effective one.  
- Provide **business recommendations** to optimize pricing and reduce risk.  

---

## 🗂️ Files in Repository  
- `Insurance_Claim_Prediction.ipynb` → Jupyter Notebook with preprocessing, modeling, and evaluation.  
- `car_insurance.csv` → Dataset used for training and testing. 

---

## 🔨 Process Overview  
1. **Data Preprocessing**  
   - Removed irrelevant features (e.g., ID, postal code).  
   - Imputed missing values for `credit_score` and `annual_mileage`.  
   - Encoded categorical variables (gender, education, vehicle type).  
   - Scaled numerical features (income, age, mileage).  

2. **Exploratory Data Analysis (EDA)**  
   - Found **credit score** to be a strong predictor of claims: lower scores → higher claim likelihood.  
   - Studied **annual mileage vs past accidents** (moderate mileage clusters showed slightly more risk).  
   - Analyzed demographic and vehicle-related features.  

3. **Modeling**  
   - Built and compared multiple classifiers:  
     - Logistic Regression  
     - Decision Tree  
     - Random Forest  
     - Gradient Boosting  
     - Bagging Classifier (ensemble method)  
   - Hyperparameter tuning with cross-validation (`GridSearchCV`).  

4. **Evaluation**  
   - Metrics: Accuracy, Precision, Recall, F1-score, Confusion Matrix.  
   - Compared class-specific results for “Claimed” vs “Not Claimed”.  

---

## 🔑 Findings & Results  
- **Logistic Regression**:  
  - Best balance between precision & recall.  
  - Achieved **71% recall** and **74% F1-score** for the "Claimed" class.  
  - Strong interpretability (coefficients reveal feature impact).  

- **Random Forest**:  
  - High overall accuracy (**83%**) but **lower recall (63%)** for claims.  

- **Gradient Boosting**:  
  - Similar to Random Forest, good accuracy but imbalance issues.  

- **Decision Tree**:  
  - Prone to overfitting, weaker performance than ensembles.  

- **Bagging Ensemble**:  
  - Slight improvement to **85% accuracy**, maintained recall at 71%.  

📊 **Preferred Model → Logistic Regression**, due to balanced performance and interpretability.  

---

## 💡 Business Recommendations  
1. **Risk-Based Pricing**  
   - Implement dynamic premium pricing based on high-risk features (credit score, speeding violations, past claims).  
   - Offer discounts to low-risk customers to remain competitive.  
   - Incentivize safe drivers with reduced premiums.  

2. **Fraud Detection & Prevention**  
   - Use the model as a **triage system** to flag high-risk claims for further investigation.  
   - Invest in fraud-detection tech and adjuster training.  

3. **Prevention & Customer Education**  
   - Launch **safe driving campaigns** and workshops, especially for fleet customers.  
   - Partner with telematics providers (GPS, driving behavior trackers) to monitor habits and offer risk-based discounts.  

---

## 🛠️ Tools & Technologies  
- **Python** – Data analysis & ML.  
- **Pandas, NumPy** – Data preprocessing.  
- **Matplotlib, Seaborn** – Visualization.  
- **Scikit-learn** – ML models & metrics.  
- **Jupyter Notebook** – Interactive analysis.  
