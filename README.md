# EX:6 DATA VISUALIZATION USING SEABORN LIBRARY

## Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

## EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

## Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

## Coding and Output:
```
Name: HARISH R
Reg.no: 212224230085
```
```py
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
df=pd.read_csv("titanic_dataset.csv")
df.head()
```
<img width="840" height="213" alt="image" src="https://github.com/user-attachments/assets/cb878be6-5e4f-46ae-9335-5bd4d8a0120e" />



### 1.Line Plot
```py
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```
<img width="453" height="387" alt="image" src="https://github.com/user-attachments/assets/d399e792-cb49-4a16-9d15-9a38e832f85e" />


### 2.Multi Line Plot
```py
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi Line Plot')
```
<img width="451" height="379" alt="image" src="https://github.com/user-attachments/assets/875cca09-f4e9-4a3d-ac40-70740d6b2b2d" />


## TO VISUALIZE RELATIONSHIPS
### 1.Bar Chart
```py
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```
<img width="577" height="423" alt="image" src="https://github.com/user-attachments/assets/71c95c5d-5cc8-4326-9b81-2fc580a74acb" />


### 2.Scatter Plot
```py
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```
<img width="476" height="380" alt="image" src="https://github.com/user-attachments/assets/b0529c5f-61dc-4de0-8a90-b1fe0c1e8630" />

### 3.Bubble Chart
```py
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
```
<img width="475" height="377" alt="image" src="https://github.com/user-attachments/assets/7f4edacd-08b8-4f2a-a90f-43e022a86a43" />

## TO CAPTURE DISTRIBUTIONS
### 1.Histogram
```py
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```
<img width="473" height="352" alt="image" src="https://github.com/user-attachments/assets/2555f313-0698-4157-bee8-badeca42edce" />

### 2.Box Plot
```py
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```
<img width="467" height="410" alt="image" src="https://github.com/user-attachments/assets/216115eb-e587-4597-a87c-11a3d5b2c1ec" />


### 3.Violin Plot
```py
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```
<img width="471" height="377" alt="image" src="https://github.com/user-attachments/assets/08b24018-928d-4871-bdaf-e606b71a882f" />


### 4.Density Plot
```py
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```
<img width="487" height="394" alt="image" src="https://github.com/user-attachments/assets/03cb66c8-ccdb-43a2-920e-17707f3c56c9" />

### 5.Heatmap
```py
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```
<img width="494" height="415" alt="image" src="https://github.com/user-attachments/assets/72203d23-67e9-4f3c-94c7-850c4f11e8d4" />



## Result:
  Thus, the Data Visualization using seaborn python library for the given data is implemented successfully

