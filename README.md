# 🏥 Insurance Cost Prediction using Linear Regression

This project demonstrates how to build a **Linear Regression model** using Python and scikit-learn to predict **insurance charges** based on personal attributes such as age, BMI, smoking status, etc.

It is a beginner-friendly machine learning project focused on understanding:
- Data preprocessing
- Train–test split
- Model training
- Prediction and evaluation
- Avoiding common mistakes like data leakage

---

## 📂 Dataset

The dataset used is **insurance.csv**, which contains the following columns:

- `age` – Age of the individual  
- `sex` – Gender (male/female)  
- `bmi` – Body Mass Index  
- `children` – Number of children  
- `smoker` – Smoking status (yes/no)  
- `region` – Residential region  
- `charges` – Medical insurance cost (**target variable**)

---

## 🛠️ Technologies Used

- Python  
- Pandas  
- NumPy  
- scikit-learn  
- Jupyter Notebook  

---

## 🚀 Project Workflow

1. **Import libraries**
2. **Load the dataset**
3. **Separate features and target**
4. **Split data into training and testing sets**
5. **Train Linear Regression model**
6. **Make predictions**
7. **Compare Actual vs Predicted values**
8. **Evaluate model performance**

---

## 📌 Important Concept: Data Leakage

During development, a common issue was encountered where **Actual and Predicted values were exactly the same**.

This happened because:
- The target column (`charges`) was mistakenly included in the feature set (`X`).

✅ This was fixed by properly separating features and target:

```python
X = df.drop(columns=['charges'])
y = df['charges']
