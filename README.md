🚢 Titanic Dataset – Exploratory Data Analysis (EDA)

A complete Exploratory Data Analysis (EDA) project performed on a 1000-row Titanic dataset.
This project includes data cleaning, preprocessing, visualizations, insights, and summary findings using Python.

📁 Dataset
The dataset used in this project:
➡️ titanic_1000.csv
(Generated with 1000 synthetic passenger records for learning & practice)

🎯 Project Objective
Perform Exploratory Data Analysis (EDA) to:
*Understand dataset structure.
*Clean missing, incorrect, or inconsistent data.
*Identify patterns and trends.
*Visualize relationships between features.
*Extract insights useful for modeling.

🛠 Tools & Technologies Used
Tool / Library              	  Purpose
Python                     	Core Programming
Pandas                    	Data Cleaning & Processing
Matplotlib	                Basic Visualization
Seaborn                   	Advanced Visualization
Jupyter Notebook           	Running Analysis

📌 Step-by-Step Workflow
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
df = pd.read_csv("titanic_1000.csv")
df.head()
df.info()
df.describe()
df.isnull().sum()
df['Age'].fillna(df['Age'].median(), inplace=True)
df['Embarked'].fillna(df['Embarked'].mode()[0], inplace=True)
df.drop_duplicates(inplace=True)

📊 Visual Exploratory Data Analysis (EDA)
*Age Distribution
sns.histplot(df['Age'], kde=True)
*Gender Count
sns.countplot(x='Sex', data=df)
*Survival by Gender
sns.countplot(x='Sex', hue='Survived', data=df)
*Survival by Class
sns.countplot(x='Pclass', hue='Survived', data=df)
*Correlation Heatmap
sns.heatmap(df.corr(), annot=True)
*Pairplot
sns.pairplot(df[['Age', 'Fare', 'SibSp', 'Parch', 'Survived']], hue='Survived')

📈 Key Insights
🔍 Overall Findings:
*Most passengers were aged 20–40.
*Females had a higher survival rate.
*st Class passengers survived significantly more.
*Fare distribution shows large income differences.
*Number of siblings/parents affects survival.

📁 Repository Structure
📦 Titanic-EDA
 ┣ 📄 titanic_1000.csv
 ┣ 📄 EDA.ipynb
 ┣ 📄 README.md
 ┗ 📁 images/

📝 Future Enhancements
*Add machine learning models for survival prediction.
*Build interactive dashboards (Power BI / Tableau).
*Add more advanced statistical tests.
