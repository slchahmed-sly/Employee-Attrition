# HR Employee Attrition Analysis & Prediction

## 📌 Project Overview
Employee attrition (turnover) is a significant cost for any organization. This project aims to analyze the factors that lead to employee attrition and build a Machine Learning model to predict whether an employee is likely to leave the company. 

By identifying these risk factors, HR departments can take proactive measures to retain valuable talent.

## 📂 Repository Structure
The repository contains the following files:
- **`Employee-Attrition.ipynb`**: The Jupyter Notebook containing the data cleaning, EDA, and Machine Learning models.
- **`Employee Attrition project.pdf`**: A detailed report on the findings and business impact.
- **`HR Employee Attrition Analysis.pptx`**: A presentation summary of the project.
- **`HR-Employee-Attrition.csv`**: The dataset used for training and testing.

## 📊 Key Insights & Exploratory Data Analysis (EDA)
After analyzing the data, several key factors were identified as strong indicators of attrition:

### 1. The Impact of Overtime
Employees working overtime showed a significantly higher rate of attrition compared to those who do not. Work-life balance appears to be a crucial factor.

<img width="799" height="591" alt="Screenshot 2026-01-15 at 23 23 09" src="https://github.com/user-attachments/assets/ed39b259-d016-4e52-83b1-ad33c2b4eb3a" />


### 2. Income and Job Role
Lower monthly income correlates with higher attrition rates. Specifically, **Sales Representatives** and **Laboratory Technicians** showed the highest turnover rates, whereas managerial roles were more stable.
<img width="794" height="595" alt="Screenshot 2026-01-15 at 23 24 13" src="https://github.com/user-attachments/assets/cde58861-bddd-4b59-af64-71bd6f5c0bb7" />

### 3. Correlation Analysis
I performed a correlation analysis to see how numerical features interact. 
<img width="1031" height="850" alt="Screenshot 2026-01-15 at 23 25 10" src="https://github.com/user-attachments/assets/6f383837-b5ce-4f1b-b20e-f4f84e737edf" />

**Other Observations:**
- **Age:** Younger employees are more likely to leave.
- **Marital Status:** Single employees have a higher attrition rate compared to Married or Divorced employees.
- **Tenure:** Employees with fewer years at the company are at higher risk.

## 🛠 Methodology
The project followed a standard Data Science lifecycle:

1.  **Data Preprocessing:** - Checked for missing values and data types.
    - Dropped zero-variance columns (`EmployeeCount`, `Over18`, `StandardHours`) that provided no predictive value.
2.  **Feature Engineering:**
    - Applied **Label Encoding** to convert categorical variables (like `BusinessTravel`, `Department`, `OverTime`) into numeric formats.
3.  **Data Splitting:**
    - Split the data into Training (75%) and Testing (25%) sets.
4.  **Feature Scaling:**
    - Used `StandardScaler` to normalize the feature range for better model performance.

## 🤖 Machine Learning Models
I implemented and compared three different classifiers to predict attrition:

| Model | Accuracy Score |
| :--- | :--- |
| **Logistic Regression** | **89.11%** |
| **Support Vector Machine (SVM)** | **89.11%** |
| **Random Forest Classifier** | 86.39% |

Both **Logistic Regression** and **SVM** performed best on this dataset.
<img width="391" height="134" alt="Screenshot 2026-01-15 at 23 26 26" src="https://github.com/user-attachments/assets/1b0c6985-1046-4a74-8591-6f72b032613e" />



## 🚀 How to Run
1. Clone the repository:
   ```bash
   git clone [https://github.com/your-username/repo-name.git](https://github.com/your-username/repo-name.git)
  
2. Install the required libraries:
   ```bash
   pip install pandas numpy seaborn matplotlib scikit-learn

3. Open the notebook:
   ```bash
   jupyter notebook Employee-Attrition.ipynb

##📢 Conclusion
To reduce attrition, the organization should focus on:

1. Reviewing the workload of employees working frequent Overtime.
2. Analyzing the compensation packages for Sales Representatives and entry-level roles.
3. Engaging with younger employees early in their tenure to improve retention.
