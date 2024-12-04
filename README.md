# Short Story Assignment
---
# **Predicting COVID-19 Patient Survival Using Random Forest and Support Vector Machine Classifiers**
---
### **Quick Links**
- **[Research Paper](https://arxiv.org/pdf/2411.18759)**  
- **[Medium Article](https://medium.com/@shruthi.rajendrashetti/classification-of-deceased-patients-from-nondeceased-patients-using-random-forest-and-support-5717af839a4f)**  
- **[Slideshare Presentation](#)**  
- **[Video Presentation](#)**  

---
This project explores the use of machine learning to classify COVID-19 patients based on survival outcomes using demographic, laboratory, and preexisting condition data. The research employs Support Vector Machines (SVM) and Random Forest (RF) classifiers to identify critical predictors and achieve high accuracy in survival predictions.
---
## **Objective**
The goal of this project is to:
- Identify critical factors influencing patient survival.
- Demonstrate the application of machine learning in healthcare decision-making.
- Provide actionable insights for resource allocation in critical care.
---
## Key Highlights
### **Dataset**
- **Size**: 9,366 patient records.
- **Attributes**: Age, gender, lab results, comorbidities, and more.
- **Source**: De-identified COVID-19 patient data from Cerner AWS.

### **Top Predictors of Survival**
1. Oxygen Saturation
2. Erythrocyte Count
3. Acute Kidney Failure
4. INR Levels
5. Severe Sepsis

### **Model Accuracy**
- **SVM**: 99.78%
- **Random Forest**: 100%

### **Visual Results**
- Feature importance rankings.
- Clusters of deceased vs. non-deceased patients.
- ROC curve demonstrating model performance.
- ---

## **Technical Approach**
1. **Data Preprocessing**:
   - Normalization of lab values.
   - Feature selection using ExtraTreeClassifier.
   - Handling outliers with Local Outlier Factor (LOF).
2. **Machine Learning Models**:
   - **SVM**: Kernel-based classification with RBF kernel.
   - **Random Forest**: Ensemble decision trees for robustness.
3. **Validation**:
   - 10-fold cross-validation to ensure generalizability.

---

