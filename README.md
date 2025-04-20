# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

# Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
 ```
import pandas as pd
df=pd.read_csv("/content/titanic_dataset.csv")
df.head()
import seaborn as sns
import matplotlib.pyplot as plt
```
![Screenshot 2024-05-06 112538](https://github.com/23013743/EXNO-6-DS/assets/161271714/a4475a72-1d46-4d49-aacf-b8ba0cfa0ba7)


## 1.Line Plot
```
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```

![Screenshot 2024-05-06 112627](https://github.com/23013743/EXNO-6-DS/assets/161271714/25594849-322f-4331-bff3-6847349f70e5)


## 2.Multi Line Plot
```
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi Line Plot')
```
![Screenshot 2024-05-06 112705](https://github.com/23013743/EXNO-6-DS/assets/161271714/4e55f654-9bfe-45e6-b4b1-f745d4b13461)


## TO VISUALIZE RELATIONSHIPS

## 1.Bar Chart
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```
![Screenshot 2024-05-06 112748](https://github.com/23013743/EXNO-6-DS/assets/161271714/6153a7da-c9dc-4d33-9e44-235da7a4c346)


## 2.Scatter Plot
```
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```
![Screenshot 2024-05-06 112845](https://github.com/23013743/EXNO-6-DS/assets/161271714/8baa88f2-16b0-417e-ae9a-208ae99b99e9)


## 3.Bubble Chart
```
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
```

![Screenshot 2024-05-06 112924](https://github.com/23013743/EXNO-6-DS/assets/161271714/49b815bb-30a9-4807-b419-45f339802a58)


## TO CAPTURE DISTRIBUTIONS
```
1.Histogram
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```
![Screenshot 2024-05-06 112953](https://github.com/23013743/EXNO-6-DS/assets/161271714/dbe8221c-0580-463f-9488-3928e6e798b9)


## 2.Box Plot
```
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```
![Screenshot 2024-05-06 113210](https://github.com/23013743/EXNO-6-DS/assets/161271714/c3a2f069-9752-4b50-a41f-09b19ce0db87)

## 3.Violin Plot
```
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```
![Screenshot 2024-05-06 113242](https://github.com/23013743/EXNO-6-DS/assets/161271714/b4879da5-5c39-472d-bf5c-3686ff26da27)


## 4.Density Plot
```
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```
![Screenshot 2024-05-06 113445](https://github.com/23013743/EXNO-6-DS/assets/161271714/46c1d0a4-b1df-4494-96f7-72d229c0c763)

## 5.Heatmap
```
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```
![Screenshot 2024-05-06 113554](https://github.com/23013743/EXNO-6-DS/assets/161271714/e2e7beb4-f549-49ad-b105-93cf6393c15f)



# Result:
 Include your result here
