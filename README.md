# EXNO2DS
# AIM:
      To perform Exploratory Data Analysis on the given data set.
      
# EXPLANATION:
  The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis.
  
# ALGORITHM:
STEP 1: Import the required packages to perform Data Cleansing,Removing Outliers and Exploratory Data Analysis.

STEP 2: Replace the null value using any one of the method from mode,median and mean based on the dataset available.

STEP 3: Use boxplot method to analyze the outliers of the given dataset.

STEP 4: Remove the outliers using Inter Quantile Range method.

STEP 5: Use Countplot method to analyze in a graphical method for categorical data.

STEP 6: Use displot method to represent the univariate distribution of data.

STEP 7: Use cross tabulation method to quantitatively analyze the relationship between multiple variables.

STEP 8: Use heatmap method of representation to show relationships between two variables, one plotted on each axis.

## CODING AND OUTPUT
import pandas as pd  
df=pd.read_csv("titanic_dataset.csv")  
print(df)  

<img width="812" height="757" alt="Screenshot 2026-08-03 152019" src="https://github.com/user-attachments/assets/897eede8-3501-425f-83b0-8fb2aedae6d5" />

df.info()  
<img width="641" height="511" alt="image" src="https://github.com/user-attachments/assets/3a3658f7-8072-4bbf-aea2-38cd008f8190" />

df.describe()  
<img width="810" height="327" alt="image" src="https://github.com/user-attachments/assets/9c6ad0ca-667f-459f-a6d6-e40eeb85e39a" />

df.shape

<img width="255" height="37" alt="image" src="https://github.com/user-attachments/assets/5f74a648-5c3f-4e18-b3a8-4a55b87c8c21" />

df.dtypes

<img width="328" height="352" alt="image" src="https://github.com/user-attachments/assets/fa69f93a-a10b-4968-923e-787863938105" />

df.value_counts() 


<img width="1252" height="535" alt="image" src="https://github.com/user-attachments/assets/0ae8258d-888c-42e8-9f9d-0dbb7c83ea23" />

df["Survived"].value_counts()

<img width="352" height="81" alt="image" src="https://github.com/user-attachments/assets/701cc2ec-bea2-46e3-a502-be55b5a1ee48" />

df.nunique()

<img width="242" height="340" alt="image" src="https://github.com/user-attachments/assets/2f6b1266-a3d1-448c-b51f-8f4d75d79ace" />

import seaborn as sns  
sns.countplot(data=df,x="Survived")  
<img width="817" height="632" alt="image" src="https://github.com/user-attachments/assets/ce9d5374-2246-4d7c-9a86-6e03dcc410ce" />

sns.boxplot(data=df,x="Age")
<img width="813" height="707" alt="image" src="https://github.com/user-attachments/assets/1dea8f5c-7bc4-4c15-979b-e058613bd841" />

sns.histplot(data=df,x="Age")
<img width="813" height="647" alt="image" src="https://github.com/user-attachments/assets/5f48bee0-65a2-40b1-9fd1-fd2d054436c4" />

df.rename(columns={'Sex':'Gender'},inplace=True)  
print(df)  
<img width="820" height="828" alt="image" src="https://github.com/user-attachments/assets/7223fe1b-ab09-47b0-ba33-9091e8f7aadb" />

sns.catplot(x='Survived',hue="Gender",data=df,kind='count')
<img width="813" height="717" alt="image" src="https://github.com/user-attachments/assets/5984bace-dd2b-484d-98e1-5779b4e882a6" />

df.boxplot(column="Age",by="Survived")
<img width="817" height="702" alt="image" src="https://github.com/user-attachments/assets/4c73fb2a-7316-4044-87e2-0e5836607563" />

sns.scatterplot(x=df["Age"],y=df["Fare"])
<img width="820" height="637" alt="image" src="https://github.com/user-attachments/assets/a4fa68c0-be30-4c90-92ad-caeb3e14370e" />

sns.boxplot(x=df["Survived"],y=df["Fare"])
<img width="815" height="638" alt="image" src="https://github.com/user-attachments/assets/c4fb75b4-d91e-4972-88db-8249fe19a6d7" />

sns.barplot(x=df["Survived"],y=df["Fare"])
<img width="818" height="651" alt="image" src="https://github.com/user-attachments/assets/0186f633-fe45-488f-9b48-51d33b959b3e" />

sns.boxplot(x="Pclass",y="Age",hue="Gender",data=df)
<img width="818" height="657" alt="image" src="https://github.com/user-attachments/assets/85f61195-e6a9-4943-aa53-eb989db647aa" />

sns.catplot(data=df,col="Survived",x="Gender",hue="Pclass",kind="count")
<img width="818" height="397" alt="image" src="https://github.com/user-attachments/assets/fbd485a3-8327-4cb9-82f0-27bd2b98e4ca" />

sns.heatmap(df.corr(),annot=True)
<img width="797" height="657" alt="image" src="https://github.com/user-attachments/assets/50707034-1de0-4698-8b80-ad00cc99b999" />

# RESULT
        <<INCLUDE YOUR RESULT HERE>>
