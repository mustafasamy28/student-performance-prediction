# Student Performance Prediction

## Project Overview
This machine learning project predicts student academic outcomes based on demographic, academic, and socioeconomic factors. The model analyzes various features to determine whether students will graduate, drop out, or face other academic outcomes, helping educational institutions identify at-risk students early and provide targeted support.

## 📊 Dataset
The dataset contains student information including:
- Demographics (age, gender, nationality)
- Academic background (previous qualifications, admission grades)
- Family context (parents' education and occupation)
- Economic factors (scholarship status, debtor status)
- Academic performance (curricular units enrolled, approved, grades)
- Economic context (unemployment rate, inflation rate, GDP)

## 🛠️ Skills & Technologies Used
- **Python** with libraries:
  - Pandas & NumPy for data manipulation
  - Scikit-learn for machine learning models
  - Matplotlib/Seaborn for visualization
- **Machine Learning Techniques**:
  - Feature selection using Recursive Feature Elimination with Cross-Validation (RFECV)
  - Data balancing with SMOTE
  - Model training and evaluation
  - Cross-validation
- **Data Preprocessing**:
  - Outlier detection and handling using IQR method
  - Feature scaling
  - Data splitting

## 🔍 Key Features Selected
Our feature selection process identified these 15 most important predictors:
1. Application mode
2. Previous qualification grade
3. Mother's qualification
4. Admission grade
5. Tuition fees up to date
6. Gender
7. Scholarship holder
8. Age at enrollment
9. Curricular units 1st sem (enrolled)
10. Curricular units 1st sem (approved)
11. Curricular units 1st sem (grade)
12. Curricular units 2nd sem (enrolled)
13. Curricular units 2nd sem (approved)
14. Curricular units 2nd sem (grade)
15. Inflation rate

## 📈 Results

### Model Performance (Before Cross-Validation)
| Model | Accuracy | Precision | Recall | F1 Score | ROC AUC |
|-------|----------|-----------|--------|----------|---------|
| Logistic Regression | 0.7232 | 0.7647 | 0.7232 | 0.7372 | 0.8699 |
| Random Forest | 0.7605 | 0.7694 | 0.7605 | 0.7632 | 0.8718 |
| Gradient Boosting | 0.7492 | 0.7604 | 0.7492 | 0.7531 | 0.8774 |
| SVM | 0.7469 | 0.7727 | 0.7469 | 0.7552 | 0.8634 |
| KNN | 0.6520 | 0.7046 | 0.6520 | 0.6715 | 0.7941 |

### Model Performance (With Cross-Validation)
| Model | Mean Accuracy | Std Accuracy |
|-------|---------------|--------------|
| Logistic Regression | 0.7382 | 0.0079 |
| Random Forest | 0.8172 | 0.0099 |
| Gradient Boosting | 0.7816 | 0.0078 |
| SVM | 0.7606 | 0.0085 |
| KNN | 0.7425 | 0.0122 |

## 🏆 Best Performing Model
**Random Forest** achieved the highest performance with:
- 81.7% mean accuracy with cross-validation
- Strong precision and recall metrics
- Good stability across different data splits

## 💡 Insights & Applications
- Early identification of students at risk of dropping out
- Personalized intervention strategies based on key factors
- Resource allocation optimization for student support services
- Improved understanding of factors affecting academic performance

## 🚀 Future Improvements
- Hyperparameter tuning for model optimization
- Exploration of additional features like study habits or psychological factors
- Time-series analysis for prediction at different points in academic journey
- Deployment as a web application for educational institutions

## 🧰 Repository Structure
```
student-performance-prediction/
│
├── notebooks/
│   └── student_performance_analysis.ipynb    # Main analysis notebook
│
├── src/
│   ├── data_preprocessing.py                 # Data cleaning and preparation
│   ├── feature_engineering.py                # Feature creation and selection
│   ├── model_training.py                     # Model training and evaluation
│   └── utils.py                              # Helper functions
│
├── README.md                                 # Project documentation
└── requirements.txt                          # Dependencies
```

## ⚙️ Setup & Installation
```bash
# Clone the repository
git clone https://github.com/your-username/student-performance-prediction.git

# Change to project directory
cd student-performance-prediction

# Create and activate virtual environment (optional)
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
```

## 📝 License
This project is open source and available under the [MIT License](LICENSE).
