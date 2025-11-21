# EDA_EXP_4   Titanic Survival Analysis using Univariate Analysis

## Aim:

To perform univariate analysis on the Titanic dataset to understand the distribution and characteristics of individual variables (such as Age, Sex, Pclass, Fare, and Survived) and to draw insights about passengers and their survival patterns.


## Algorithm

**1)Import Libraries:**

Load the required Python libraries (pandas, numpy, matplotlib, seaborn).

**2)Load the Dataset:**

Read the Titanic dataset from available sources (e.g., seaborn’s built-in Titanic dataset or a CSV file).

**3)Data Inspection:**

View the first few rows using head().

Get dataset summary using info() and describe().

**4)Handle Missing Data:**
Identify missing values using isnull().sum() and handle them appropriately (e.g., fill or drop).

**5)Univariate Analysis:**
Perform univariate analysis for each variable:

**Categorical Variables: (e.g., Sex, Pclass, Survived, Embarked)**
Use frequency tables and count plots.

**Numerical Variables: (e.g., Age, Fare)**
Use histograms, box plots, and summary statistics.

**6)Interpretation:**
Analyze distributions, central tendencies, and spread.
Identify patterns (e.g., more passengers in 3rd class, survival differences by gender).


## **Program**

## Name : Subishesh P

## Reg No.:212223230220
```
import seaborn as sns
import pandas as pd
import matplotlib.pyplot as plt
df=sns.load_dataset('titanic')
df.info()
df.head()
df.describe()
df.isnull(), value counts()
sex=df['sex'].value_counts()
print(sex)
sur=df['survived'].mean()*100
print(sur, "%")
categories=['sex', 'survived', 'sibsp', 'embarked', 'class', 'who', 'adult_male', 'deck
for i in categories:
plt.figure(figsize=(6,4))
sns.countplot(data=df,x=i)
print(df[i].value_counts())
plt.xlabel(i)
plt.ylabel("Count")
plt.show()
meanage=df['age'].mean()
medianage=df['age'].median()
age_range=(df['age'].min(),df['age'].max())
print(meanage)
print(medianage)
print(age_range)
plt.figure(figsize=(10,10))
sns.histplot(df['age'].dropna(), bins=30, kde=True)
plt.xlabel('age')
plt.ylabel('count')
plt.show()
import seaborn as sns
numerical_features = ['age', 'fare']
for col in numerical_features:
plt.figure(figsize=(6,4))
sns.histplot (df [col], kde=True, bins=30)
plt.title(f'Distribution of {col}')
plt.show()
plt.figure(figsize=(6,4))
sns.boxplot(x=df[col])
plt.title(f'Boxplot of {col}')
plt.show()
print(f"\nSummary Statistics for {col}:\n", df[col].describe())
print("-"*50)
```

## **Output**
<img width="825" height="904" alt="Screenshot 2025-11-19 110645" src="https://github.com/user-attachments/assets/df4e0044-15c8-4e56-8851-5b2d80f37e9c" />

<img width="824" height="913" alt="Screenshot 2025-11-19 110717" src="https://github.com/user-attachments/assets/d5bea7e3-eb18-4c73-9777-b71f9900a459" />

<img width="833" height="807" alt="Screenshot 2025-11-19 110727" src="https://github.com/user-attachments/assets/e11c626a-627d-4fcc-8d95-1a768e6240ce" />

<img width="817" height="810" alt="Screenshot 2025-11-19 110735" src="https://github.com/user-attachments/assets/8cb6bf37-4f7b-49c6-aef9-d3458d0e7ef1" />

<img width="812" height="761" alt="Screenshot 2025-11-19 110744" src="https://github.com/user-attachments/assets/661f946e-d84e-47ab-8cb7-f979251ec3a6" />

<img width="774" height="710" alt="Screenshot 2025-11-19 110753" src="https://github.com/user-attachments/assets/a9df4db9-73cd-486d-b993-82f91f987d1d" />

<img width="730" height="912" alt="Screenshot 2025-11-19 110802" src="https://github.com/user-attachments/assets/342a08ea-7471-4f16-8707-e51b42fee174" />

<img width="811" height="319" alt="Screenshot 2025-11-19 110810" src="https://github.com/user-attachments/assets/71c517b1-bffc-45e4-b8ff-672f73f02e8f" />




## **Result**
From the univariate analysis:

Majority of passengers were male and in 3rd class.

Around 38% survived, majority being females and higher-class passengers.

Age is right-skewed with most passengers aged 20–40 years.

Fare distribution shows a few high outliers for 1st class passengers.

Thus, univariate analysis helps understand the distribution and spread of each individual feature in the Titanic dataset before moving to bivariate or multivariate analysis.

## Visualization:
Plot appropriate charts for each variable using Matplotlib/Seaborn.
