# 📊 Predictive Analysis of Insurance Charges using Multiple Linear Regression

## 📌 Overview
This project applies **Multiple Linear Regression** to predict insurance charges based on an individual's **health and economic conditions**. Using **statistical data analysis**, the project provides insights into **how different factors impact insurance costs** and builds a regression model to predict future charges.

## 📂 Contents
1. [Introduction](#-introduction)  
2. [Data Understanding](#-data-understanding)  
3. [Regression Analysis](#-regression-analysis)  
4. [Prediction](#-prediction)  
5. [Conclusion](#-conclusion)  
6. [References](#-references)  

---

## 📖 Introduction
Healthcare costs have been increasing for years, making **insurance coverage a necessity** for many individuals. This study aims to:  
✔ **Analyze** how personal attributes (age, BMI, smoker status, etc.) affect insurance charges.  
✔ **Develop** a **Multiple Linear Regression model** to predict individual medical costs.  

The dataset consists of **1,338 records** with **7 attributes**:
- **Age**: Primary beneficiary’s age.  
- **Sex**: Gender of the insurance contractor.  
- **BMI**: Body Mass Index (kg/m²).  
- **numChild**: Number of dependents covered by insurance.  
- **Smoker**: Whether the individual is a smoker (Yes/No).  
- **Region**: Residential region (Northeast, Northwest, Southeast, Southwest).  
- **Charges**: Medical costs billed by health insurance (USD) (Dependent Variable).  

---

## 🔍 Data Understanding

### **📊 Sample Data & Key Statistics**
✔ **Dataset contains 1,338 entries and 7 attributes.**  
✔ **No NULL values present** in the dataset.  
✔ **4 numerical variables (Age, BMI, numChild, Charges) and 3 categorical variables (Sex, Smoker, Region).**  
✔ **Charges range from $1,121.87 to $63,770.43.**  
✔ **Right-skewed distribution** of **charges** due to high medical expenses for certain individuals.  

### **📈 Statistical Analysis & Data Visualization**
✔ **Numerical Variables & Correlations**:
   - **All numerical variables show a positive relationship** with insurance charges.
   - **Age, BMI, and smoker status have a significant impact** on medical costs.  
✔ **Categorical Variables Impact**:
   - **Smokers** have significantly **higher insurance charges** than non-smokers.
   - **Gender and region show minimal impact** on charges.

---

## 📉 Regression Analysis

### **🛠 Data Preparation**
✔ **Categorical variables were transformed** into numerical values using **one-hot encoding**:
   - `sex` → `male`, `female`  
   - `smoker` → `smoker_yes`, `smoker_no`  
   - `region` → `northeast`, `northwest`, `southeast`, `southwest`  

✔ **Dataset was split into training (80%) and testing (20%) subsets.**  

### **📏 Model Formulation**
The **Multiple Linear Regression Model** is expressed as:  

![image](https://github.com/user-attachments/assets/8ab05e3b-858a-4646-bc12-a4e0beb11c7a)

where:  
- **y** = Insurance Charges (Dependent Variable)  
- **x1, x2, ..., xn** = Predictor variables (age, BMI, smoker status, etc.)  

**Final Regression Equation**:

𝑦 = −1006.57 + 244.51𝑥1 + 364.95𝑥2 + 412.99𝑥3 + (-54.35)𝑥4 + 54.35𝑥5 + (-11827.95)𝑥6 + 11827.95𝑥7 + 423.93𝑥8 + 524.81𝑥9 + (-489.06)𝑥10 + (-459.68)𝑥11


### **🔬 Findings**
✔ **Smoker status is the most influential factor** affecting insurance charges.  
✔ **Age and BMI contribute significantly** to higher costs.  
✔ **Number of dependents and region have a weaker correlation** with charges.  

---

## 🎯 Prediction

After training the model, the test dataset was used to evaluate the predictions.  

✔ **Comparison between Actual vs. Predicted Charges**:  
A visualization of **expected vs. predicted values** shows that the model captures the trend well.  

✔ **Error Analysis**:  
- **Mean Absolute Error (MAE):** 4036.865772278072
- **Mean Squared Error (MSE):** 33748606.755860314

-> Findings: 
- The **MAE of ~$4,037** suggests that while the model provides a **general estimate**, individual predictions may still be off by a few thousand dollars.  
- The **high MSE value** indicates that some **extremely high medical costs** (possibly from smokers or elderly individuals) are harder to predict accurately.  
- **Potential Improvements:**  
  - Might apply **Polynomial Regression** or **Non-Linear Models** for better accuracy.  
  - Explore **feature engineering** (e.g., interaction terms between BMI & smoker status).  
  - Remove or transform **high-cost outliers** to reduce error impact.  

📌 **Despite these errors, the model still answers the given question and provides valuable insights into how factors like age, BMI, and smoking status influence insurance costs.** 🚀  

---

## 📌 Conclusion  
This project demonstrates how **statistical analysis and regression modeling** can **predict insurance charges** based on personal attributes.  
✔ **Smoker status, age, and BMI are key predictors** of high medical costs.  
✔ **Multiple Linear Regression successfully models the relationship** between insurance costs and independent variables.  
✔ **Further enhancements** could include advanced models like **Polynomial Regression or Machine Learning approaches** for better accuracy.  

---

## 📚 References
- [Kaggle: Linear Regression Tutorial](https://www.kaggle.com/code/sudhirnl7/linear-regression-tutorial/notebook)  
- [Kaggle: Dataset & Analysis](https://www.kaggle.com/code/sudhirnl7/linear-regression-tutorial/data)  

---

## 🚀 How to Use This Repository
1. **Clone the repository**:  
   ```sh
   git clone https://github.com/your-repo-name.git
