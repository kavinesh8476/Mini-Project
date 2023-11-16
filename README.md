# Mini-Project

## AIM
To analyze billionaire statistics dataset using various data science techniques.

## PROCEDURE

1. import the necessary libraries.
2. Read the dataset.
3. Perform data cleaning.
4. Visulaize the data using various data visualization techniques.
5. Encode the text data.
6. Analyse it using various techniques.
   
## CODE AND OUTPUT
```
DEVELOPED BY:KAVINESH M
REGISTER NO:212222230064
```

```
import pandas as pd
df=pd.read_csv('/content/Billionaires_Statistics_Dataset.csv')
df
```
![image](https://github.com/Pranav-AJ/Mini-Project/assets/118904526/580e91f1-a044-41fe-aba6-9584193e1dc2)

```
df.info()
```
![image](https://github.com/Pranav-AJ/Mini-Project/assets/118904526/ccf6f184-0d44-483a-9388-12d4dc844957)

```
df.isnull().count()
```
![image](https://github.com/Pranav-AJ/Mini-Project/assets/118904526/63195faf-37e1-4f57-a477-587b24ca1641)

```
df.describe()
```
![image](https://github.com/Pranav-AJ/Mini-Project/assets/118904526/e00215fe-05bf-492f-a05f-d533421a748d)

```
df.shape
```
![image](https://github.com/Pranav-AJ/Mini-Project/assets/118904526/82717f0c-b400-4810-931c-9a2a68ea4671)


**DATA CLEANING**
```
df=df.dropna()
```
```
df.info()
```
![image](https://github.com/Pranav-AJ/Mini-Project/assets/118904526/81a69ec6-7063-462f-8b25-d591274a40a1)

**UNIVARIATE ANALYSIS**
```
import seaborn as sns
import matplotlib.pyplot as plt
```
```
sns.boxplot(x='finalWorth',data=df)
```
![image](https://github.com/Pranav-AJ/Mini-Project/assets/118904526/c99dec64-1bff-4bc3-882d-7645adeaf54b)

```
plt.figure(figsize = (50,50))
sns.countplot(y="country",data=df)
```
![image](https://github.com/Pranav-AJ/Mini-Project/assets/118904526/afa79370-e1d6-462b-894f-749c9f435750)

**MULTIVARIATE ANALYSIS**
```
sns.scatterplot(data=df,x='finalWorth',y='age')
```
![image](https://github.com/Pranav-AJ/Mini-Project/assets/118904526/dc159c77-fe75-44ca-9d5a-e57f21eda449)

```
plt.figure(figsize=(40,10))
sns.barplot(data=df,x='category',y='finalWorth')
```
![image](https://github.com/Pranav-AJ/Mini-Project/assets/118904526/f94c17d9-0e48-460e-9c95-8c8eeffbd3a0)

```
sns.heatmap(df.corr(),annot=True)
```
![image](https://github.com/Pranav-AJ/Mini-Project/assets/118904526/9454d247-4fa1-485d-a7d5-f32c5972c9c0)

```
from sklearn.preprocessing import LabelEncoder
```
```
df['category']
```
![image](https://github.com/Pranav-AJ/Mini-Project/assets/118904526/b8a12bff-4a3d-4b6f-9a38-f19c1ac6ef85)

```
le=LabelEncoder()
df['category']=le.fit_transform(df['category'])
df['category']
```
![image](https://github.com/Pranav-AJ/Mini-Project/assets/118904526/6b70ff02-04c2-4d48-8031-3f30ba2603c2)

## RESULT
Hence the billionaire statistics dataset was successfully analyzed
