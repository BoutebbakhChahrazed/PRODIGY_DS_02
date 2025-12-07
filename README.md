# Prodigy InfoTech Data Science Internship - Task 02
## Titanic Dataset: Data Cleaning & Exploratory Data Analysis (EDA)

This repository contains the Jupyter Notebook for **Task 02** of the Prodigy InfoTech Data Science Internship. The goal of this task is to perform data cleaning and exploratory data analysis (EDA) on the Titanic dataset to explore the relationships between variables and identify patterns and trends in survival rates.

### 📄 Project Overview
The Titanic dataset is a classic machine learning dataset often used for data science practice. In this notebook, we analyze the passenger data to understand:
- Missing values and how to handle them.
- Distributions of numerical and categorical features.
- Correlations between features and survival.
- How factors like **Class**, **Sex**, **Age**, and **Family Size** impacted survival chances.

### 📂 Dataset
The dataset is sourced from [Kaggle's Titanic - Machine Learning from Disaster](https://www.kaggle.com/c/titanic).
It consists of three CSV files:
- `train.csv`: Training set containing features and the target variable (`Survived`).
- `test.csv`: Test set for predictions.
- `gender_submission.csv`: Sample submission file.

### 🛠️ Libraries Used
The analysis is implemented in Python using the following libraries:
- **Pandas**: For data manipulation and analysis.
- **NumPy**: For numerical operations.
- **Matplotlib** & **Seaborn**: For data visualization.
- **Scikit-learn**: For feature engineering and preprocessing (e.g., `LabelEncoder`, `train_test_split`).

### 📊 Analysis Workflow

#### 1. Data Loading & Inspection
- Loaded the training and testing datasets.
- Inspected the data structure using `.head()`, `.info()`, and `.describe()`.
- Identified missing values in columns such as `Age`, `Cabin`, and `Embarked`.

#### 2. Data Cleaning
- **Cabin**: Dropped the column due to a high percentage (>77%) of missing values.
- **Age**: Imputed missing values using the **median** age.
- **Embarked**: Filled missing values with the **mode** (most frequent port).
- **Fare**: Filled missing values in the test set with the **median** fare.

#### 3. Feature Engineering
- **FamilySize**: Created a new feature combining `SibSp` (siblings/spouses) and `Parch` (parents/children).
- **IsAlone**: Binary feature indicating if a passenger was traveling alone.
- **Title Extraction**: Extracted titles (Mr, Mrs, Miss, etc.) from passenger names and grouped rare titles.
- **Encoding**: Mapped categorical variables (`Sex`, `Embarked`, `Title`) to numerical values for correlation analysis.

#### 4. Exploratory Data Analysis (EDA)
Visualized key relationships using Seaborn and Matplotlib:
- **Survival Count**: Distribution of survivors vs. non-survivors.
- **Survival by Gender**: Highlighted that females had a significantly higher survival rate.
- **Survival by Class (Pclass)**: Showed that 1st-class passengers were more likely to survive.
- **Age Distribution**: Histograms showing the age spread of passengers.
- **Correlation Heatmap**: Visualized correlations between numerical features and the `Survived` target.

### 📈 Key Insights
- **Gender**: Being female was the strongest predictor of survival.
- **Class**: Socio-economic status (Pclass) played a major role; 3rd class passengers had the lowest survival rate.
- **Family**: Passengers traveling alone had a lower survival rate compared to those with small families (1-3 members).

### 🚀 How to Run
1. Clone the repository or download the `PRODIGY_DS_02.ipynb` file.
2. Ensure you have the dataset files (`train.csv`, `test.csv`) in the input directory (or update the paths in the notebook).
3. Install the required libraries if not already installed:
pip install pandas numpy seaborn matplotlib scikit-learn
4. Open and run the notebook:
jupyter notebook PRODIGY_DS_02.ipynb

### 👤 Author
- **Name**: [Boutebbakh Chahrazed]
- **Internship**: Prodigy InfoTech Data Science Intern
- **Task**: 02
