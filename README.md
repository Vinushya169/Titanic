
# 🚢 Titanic Survival Analysis - EDA & Machine Learning Prediction

> An end-to-end Data Analysis and Machine Learning project to analyze the Titanic disaster and predict passenger survival.

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Pandas](https://img.shields.io/badge/Pandas-Used-orange)
![ML](https://img.shields.io/badge/ML-Random%20Forest-green)

---

## 📌 Project Overview
The sinking of the Titanic is one of the most infamous shipwrecks in history. On April 15, 1912, during her maiden voyage, Titanic sank after colliding with an iceberg, killing 1502 out of 2224 passengers and crew.

This project aims to answer: **What kind of people were more likely to survive?**

Using Python and Machine Learning, we analyze the passenger data and build a model to predict survival.

## 📊 Dataset Details
- **Source:** Kaggle Titanic Competition - https://www.kaggle.com/c/titanic
- **Rows:** 891 passengers (train.csv) + 418 (test.csv)
- **Columns:** 12 features

| Column | Description |
|---|---|
| PassengerId | Unique ID |
| Survived | 0 = No, 1 = Yes (Target) |
| Pclass | Ticket class (1 = 1st, 2 = 2nd, 3 = 3rd) |
| Sex | Male/Female |
| Age | Age in years |
| SibSp | # of siblings / spouses aboard |
| Parch | # of parents / children aboard |
| Fare | Ticket fare |
| Cabin | Cabin number |
| Embarked | Port of Embarkation (C=Cherbourg, Q=Queenstown, S=Southampton) |

## 🛠️ Tech Stack & Libraries
- **Language:** Python
- **Data Manipulation:** Pandas, NumPy
- **Visualization:** Matplotlib, Seaborn
- **Machine Learning:** Scikit-Learn (Logistic Regression, Random Forest, Decision Tree)
- **Environment:** Jupyter Notebook, Anaconda
- **Version Control:** Git & GitHub

## 🔍 Exploratory Data Analysis (EDA) - Step by Step

### 1. Data Cleaning
- Checked for null values: Age (177 missing), Cabin (687 missing), Embarked (2 missing)
- Filled missing Age with median age
- Filled Embarked with most frequent value 'S'
- Dropped Cabin column due to high missing values

### 2. Visualizations Done
- **Count Plot:** Survival count (38% survived, 62% died)
- **Bar Plot:** Survival by Gender -> Female 74% survived, Male only 18.9%
- **Bar Plot:** Survival by Pclass -> Pclass 1 (63% survived) > Pclass 2 (47%) > Pclass 3 (24%)
- **Histogram:** Age distribution - Most passengers were 20-40 years
- **Box Plot:** Fare vs Survival - Higher fare = Higher survival chance
- **Heatmap:** Correlation between all numeric features
- **Pie Chart:** Embarked port distribution

## 🤖 Machine Learning - Model Building

### Feature Engineering
- Created new feature: `FamilySize = SibSp + Parch + 1`
- Created `IsAlone` feature
- Encoded categorical variables: Sex (0/1), Embarked (One-Hot Encoding)

### Models Tried
1.  **Logistic Regression** - Accuracy: 78.5%
2.  **Decision Tree** - Accuracy: 76.2%
3.  **Random Forest Classifier** - Accuracy: 81.3% (Best Model) 🏆
4.  **KNN** - Accuracy: 75.1%

### Final Model: Random Forest
- n_estimators = 100
- max_depth = 10
- Train-Test Split: 80-20
- Final Accuracy: ~81%

## 💡 Key Insights & Findings
1.  **Gender was the most important factor:** Women and children first policy was followed.
2.  **Class Matters:** Being rich increased your chance of survival. 1st class had access to more lifeboats.
3.  **Age Factor:** Children (below 10 years) had higher survival rate.
4.  **Family Size:** Passengers with family size 2-4 had higher survival than alone passengers or very large families.
5.  **Fare:** Passengers who paid > 100$ had ~75% survival rate.

## 🚀 How to Run This Project Locally

```bash
# 1. Clone the repository
git clone https://github.com/Vinushya169/Titanic-Survival-Analysis.git

# 2. Go to project folder
cd Titanic-Survival-Analysis

# 3. Install required libraries
pip install pandas numpy matplotlib seaborn scikit-learn jupyter

# 4. Launch Jupyter Notebook
jupyter notebook

# 5. Open Titanic Analysis.ipynb and Run All Cells
## 📂 Project Structure
Titanic-Survival-Analysis/
│
├── train.csv
├── test.csv
├── Titanic Analysis.ipynb
├── README.md
└── titanic_survival_model.pkl
## 👩‍💻 Author
*Vinushya M*
- Aspiring Data Analyst | Data Science Enthusiast
- Skills: Python, SQL, Pandas, ML, Data Visualization
- GitHub: https://github.com/Vinushya169
- LinkedIn: [https://www.linkedin.com/in/vinushya-m-80b92b400]

## 🌟 Future Improvements
- Try XGBoost and LightGBM for better accuracy
- Use Deep Learning
- Create a Streamlit Web App for prediction

## 📝 Acknowledgements
- Kaggle for the dataset
- My mentors for guidance

---
⭐ If you liked this project, give it a star!


