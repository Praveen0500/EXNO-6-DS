# EX:6 DATA VISUALIZATION USING SEABORN LIBRARY

## Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

## EXPLANATION:
### Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

## Algorithm:

STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

## Coding and Output:
```
Developed By : PRAVEEN S
Reg.no: 212222240078
```
```py
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
df=pd.read_csv("titanic_dataset.csv")
df.head()
```

![328071862-8dc49211-169b-403a-abd3-cd8051e57e71](https://github.com/Praveen0500/EXNO-6-DS/assets/120218611/6c814432-04c7-4fae-a5a6-bae40853b5a0)



### 1.Line Plot
```py
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```
![328071870-7675337f-cc04-46cc-bf81-38262b270bd4](https://github.com/Praveen0500/EXNO-6-DS/assets/120218611/90fa8419-7976-4e39-b263-d6a37c22f5b9)


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

![328071893-869fd5a5-d8e2-48ae-95a2-465276214469](https://github.com/Praveen0500/EXNO-6-DS/assets/120218611/4b712cf0-acc4-4568-8725-39d92133891b)



## TO VISUALIZE RELATIONSHIPS
### 1.Bar Chart
```py
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```
![328071920-4045fe11-a43b-4c94-86f6-ef576a3478dd](https://github.com/Praveen0500/EXNO-6-DS/assets/120218611/e6918ed3-efe4-466e-959f-bf09b5f208ac)


### 2.Scatter Plot
```py
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```
![328071946-1bc6fb42-bd4f-4cd9-b311-f1a0891c079d](https://github.com/Praveen0500/EXNO-6-DS/assets/120218611/d4bb097a-5447-47a9-8d00-9eae748de7f2)


### 3.Bubble Chart
```py
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
```
![328071972-79145503-aa3d-4820-819d-84def2a4e3fc](https://github.com/Praveen0500/EXNO-6-DS/assets/120218611/9dfc585b-5551-4b72-ad84-a65cc199a2f4)


## TO CAPTURE DISTRIBUTIONS
### 1.Histogram
```py
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```
![328072018-05836fa5-bc95-446a-b909-9f1b03153162](https://github.com/Praveen0500/EXNO-6-DS/assets/120218611/9d89b706-a5ee-4770-b4fd-d3d290e928a8)


### 2.Box Plot
```py
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```
![328072030-c692e7e3-7559-457b-95e2-1028463ac63f](https://github.com/Praveen0500/EXNO-6-DS/assets/120218611/2e6e1b33-5578-436b-882e-f600cd26bf7e)


### 3.Violin Plot
```py
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```
![328072200-0e687cdd-8039-4084-860f-b1c2ed0cd626](https://github.com/Praveen0500/EXNO-6-DS/assets/120218611/ea29c47f-e403-4118-94a8-fafdc312a9f2)


### 4.Density Plot
```py
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```
![328072219-0de53228-f108-49a5-8682-b01fc241d5b7](https://github.com/Praveen0500/EXNO-6-DS/assets/120218611/c6f250ba-fe0c-471d-b55e-0d03abb7bfed)


### 5.Heatmap
```py
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```
![328072233-61ce4f2d-1e09-48e3-b27b-5e13d291f842](https://github.com/Praveen0500/EXNO-6-DS/assets/120218611/a1e6502d-b421-4a4e-a895-24b4bbe6eb28)



## Result:
  
  ### Thus, the Data Visualization using seaborn python library for the given data is implemented successfully

