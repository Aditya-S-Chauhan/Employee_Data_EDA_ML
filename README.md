About Dataset
Context:
This dataset contains information about employees in a company, including their educational backgrounds, work history, demographics, and employment-related factors. It has been anonymized to protect privacy while still providing valuable insights into the workforce.

Columns:

Education: The educational qualifications of employees, including degree, institution, and field of study.

Joining Year: The year each employee joined the company, indicating their length of service.

City: The location or city where each employee is based or works.

Payment Tier: Categorization of employees into different salary tiers.

Age: The age of each employee, providing demographic insights.

Gender: Gender identity of employees, promoting diversity analysis.

Ever Benched: Indicates if an employee has ever been temporarily without assigned work.

Experience in Current Domain: The number of years of experience employees have in their current field.

Leave or Not: a target column

The project uses python's pandas, numpy, seaborn and matplotlib to perform Exploratory Data Analysis (EDA) and create
visualizations of insights. The project uses sklearn to implement models such as Logistic Regression, Support Vector Classifier,
Decision Tree Classifier and Random Forest Classifier to check accuracy for Leave Or Not.

Potential Research Questions:

What is the distribution of educational qualifications among employees?
How does the length of service (Joining Year) vary across different cities?
What is the gender distribution within the workforce?
Are there any patterns in leave-taking behavior among employees?

Imported libraries:

import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
from sklearn.model_selection import train_test_split
from sklearn.preprocessing import StandardScaler
from sklearn.metrics import accuracy_score
from sklearn.linear_model import LogisticRegression
from sklearn.model_selection import GridSearchCV
from sklearn.svm import SVC
from sklearn.tree import DecisionTreeClassifier
from sklearn.ensemble import RandomForestClassifier

Exploratory Data Analysis (EDA) overview:

Check the data using info and describe 
Check for NA and duplicate values
Sorting the data by Joining Year
Visualizations : histogram of Age, countplot for Gender, boxplot of Experience In Domain, scatterplot of Experience in Domain and Age, 
violinplot of Age Distribution by Payment Tier, pairplot of Age-Expeience in Domain-Joining Year, boxpllot of Gender-Experience in Domain,
kernel density estimate plot for Joining Year, bar plot of Education and Average Experience in Domain, areaplot of joining year Benched vs Not Benched,
boxplot of Education Benched vs Not Benched, facet grid of Experience in Domain by City, line plot of Joining Year by City.

Key Insights:
Employees with PHD have more Experience in Domain than those with Masters, who in turn have more Experience in Domain than Bachelors. 

Male employees with the same Education level had more Experience in Domain than Female employees. 

See visualization for trend of Joining Year-Age in different Cities 

See visualization of Age-Experience in Domain-Joining Year

In every city except Pune, more employees were in 'Leave' than 'Not Leave'. In Pune the numbers were nearly half for both categories.


Machine Learning:
X = df.loc[:, df.columns != 'LeaveOrNot']

X = X.drop(columns = ['JoiningYear', 'City', 'Age']) X 

y = df.loc[:, 'LeaveOrNot']

Label encoding on Gender, EverBenched and Education 

Logistic Regression : Accuracy score in model is 0.6654611211573237

Grid Search: Accuracy score in model is 0.6672694394213382

Decisiojn Tree Classifier: Accuracy score in model is 0.6618444846292948


Random Forest Classifier: Accuracy score in model is 0.6708860759493671 * The winning model



