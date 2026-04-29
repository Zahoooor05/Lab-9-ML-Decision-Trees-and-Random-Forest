# Lab-9-ML-Decision-Trees-and-Random-Forest

## Overview
This project analyzes loan data from LendingClub to predict whether a borrower will fully repay a loan or not. The goal is to build and evaluate machine learning models that help identify risky borrowers.

## Dataset
The dataset contains information about borrowers, including:
- Credit policy status
- Loan purpose
- Interest rate
- Income
- Debt-to-income ratio
- FICO score
- Credit history
- Loan repayment status (`not.fully.paid`)

Total records: 9,578  
Target variable: `not.fully.paid` (0 = paid, 1 = not fully paid)

## Steps Performed

### 1. Data Loading
- Loaded dataset using pandas
- Explored data using `.info()`, `.head()`, `.describe()`

### 2. Exploratory Data Analysis (EDA)
- Histogram of FICO scores by credit policy
- Histogram of FICO scores by loan repayment
- Countplot of loan purposes
- Jointplot of FICO vs interest rate
- LM plots to analyze relationships across categories

### 3. Data Preprocessing
- Converted categorical feature (`purpose`) using dummy variables
- Created final dataset for modeling

### 4. Train-Test Split
- Split data into training and testing sets (70% train, 30% test)

### 5. Models Used

#### Decision Tree
- Trained using `DecisionTreeClassifier`
- Evaluated using:
  - Classification report
  - Confusion matrix

#### Random Forest
- Trained using `RandomForestClassifier (n_estimators=600)`
- Evaluated using:
  - Classification report
  - Confusion matrix

## Results

### Decision Tree Performance
- Better at identifying both classes compared to Random Forest
- More balanced recall between classes

### Random Forest Performance
- High accuracy for class 0 (paid loans)
- Very poor recall for class 1 (default cases)
- Model biased toward majority class

## Conclusion
- Decision Tree performed better in detecting risky borrowers
- Random Forest achieved higher overall accuracy but failed to detect defaults effectively
- Class imbalance significantly affected performance

## Technologies Used
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

## How to Run
1. Open Google Colab or Jupyter Notebook
2. Upload `loan_data.csv`
3. Run cells step by step
4. Observe outputs and model performance

## Author
Zahra Al Ubaid
