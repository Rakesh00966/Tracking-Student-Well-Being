# 🎓 Tracking Student Well-Being | Machine Learning [Link](https://github.com/Rakesh00966/Tracking-Student-Well-Being/blob/main/Tracking_Student_Well_Being.ipynb)

## 📘 Project Overview
This project focuses on predicting **students' stress levels** based on various mental, physical, and environmental factors.  
By analyzing data from the **StressLevelDataset.csv**, the goal was to identify the most influential parameters affecting student well-being and build a reliable machine learning model to classify their stress levels.

---

## 🧠 Objectives
- Analyze factors that influence student stress levels  
- Visualize relationships between features and stress levels  
- Train and evaluate multiple machine learning models  
- Select and save the best performing classifier for future predictions  

---

## 📂 Dataset Information
**Dataset:** `StressLevelDataset.csv`  
**Total Records:** 1100  
**Total Features:** 21  

### 🔑 Feature Descriptions
| Feature | Description |
|----------|-------------|
| anxiety_level | Level of anxiety reported by the student |
| self_esteem | Student's self-esteem score |
| mental_health_history | 1 if history of mental health issues, else 0 |
| depression | Level of depression reported |
| headache | Frequency/severity of headaches |
| blood_pressure | Blood pressure level |
| sleep_quality | Quality of sleep |
| breathing_problem | Indicates breathing problems (0/1) |
| noise_level | Noise level in the student's environment |
| living_conditions | Quality of living conditions |
| safety | Feeling of safety |
| basic_needs | Access to basic needs |
| academic_performance | Academic performance level |
| study_load | Study load level |
| teacher_student_relationship | Quality of teacher-student relationship |
| future_career_concerns | Level of career concern |
| social_support | Amount of social support |
| peer_pressure | Level of peer pressure |
| extracurricular_activities | Involvement in activities |
| bullying | Bullying experience (0/1) |
| **stress_level** | **Target variable — student stress level** |

---

## ⚙️ Project Workflow

### 1️⃣ Data Loading & Inspection
- Loaded dataset using **Pandas**
- Checked for null values, data types, duplicates, and descriptive statistics  
- No missing or duplicate records were found  

### 2️⃣ Data Visualization
- **Histograms:** Visualized distributions of `anxiety_level`, `self_esteem`, and `depression`  
- **Correlation Heatmap:** Analyzed relationships among all features  
- Identified strong correlations between stress level and features like **depression**, **anxiety level**, and **self-esteem**

### 3️⃣ Data Preprocessing
- Separated features (`X`) and target (`y`)  
- Performed an **80/20 train-test split**  
- Scaled data using **StandardScaler**  

### 4️⃣ Model Training & Optimization
Trained multiple models using **RandomizedSearchCV** with **Stratified K-Fold Cross-Validation (k=5)**:
- Gradient Boosting  
- Random Forest  
- Logistic Regression  
- K-Nearest Neighbors  
- Decision Tree  
- Support Vector Classifier  

**Evaluation Metrics:**  
Accuracy, F1-Score, Recall, Precision, and ROC-AUC

---

## 🏆 Model Comparison Results

| Model | Accuracy | F1-Score | Recall | Precision | ROC-AUC |
|-------|-----------|----------|---------|------------|----------|
| **Logistic Regression** | **0.8864** | **0.8864** | 0.8864 | 0.8866 | 0.9782 |
| Random Forest | 0.8773 | 0.8774 | 0.8773 | 0.8786 | 0.9834 |
| Gradient Boosting | 0.8773 | 0.8772 | 0.8773 | 0.8772 | 0.9831 |
| SVC | 0.8636 | 0.8640 | 0.8636 | 0.8652 | 0.9807 |
| Decision Tree | 0.8500 | 0.8504 | 0.8500 | 0.8534 | 0.9772 |
| KNN | 0.8500 | 0.8500 | 0.8500 | 0.8501 | 0.9480 |

✅ **Best Model:** Logistic Regression  
✅ **Best F1-Score:** 0.8864  

---

## 📊 Classification Report (Best Model)

| Class | Precision | Recall | F1-Score | Support |
|--------|------------|---------|-----------|----------|
| 0 | 0.87 | 0.88 | 0.88 | 76 |
| 1 | 0.88 | 0.88 | 0.88 | 73 |
| 2 | 0.91 | 0.90 | 0.91 | 71 |

**Overall Accuracy:** 0.89  
**Macro Avg F1:** 0.89  
**Weighted Avg F1:** 0.89  

---
