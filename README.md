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
```py
import pandas as pd
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt
```
## Line Plot
```py
# Create line plot using seaborn
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
```

<img width="534" height="413" alt="image" src="https://github.com/user-attachments/assets/deebc73e-0a71-47f9-940e-640132a441fa" />

```py
x = [1, 2, 3, 4, 5]
y1 = [3, 5, 2, 6, 1]
y2 = [1, 6, 4, 3, 8]
y3 = [5, 2, 7, 1, 4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi Line Plot')
```
<img width="534" height="433" alt="image" src="https://github.com/user-attachments/assets/c5d40d17-1310-4c09-aac7-7b90e07b172a" />

## Bar Chart
```py
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=tit,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```
<img width="687" height="468" alt="image" src="https://github.com/user-attachments/assets/b601fe07-ebfa-40a8-9894-b85e7fdb4c02" />

## Scatter Plot
```py
sns.scatterplot(x="Age", y="Fare", data=tit)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```
<img width="571" height="453" alt="image" src="https://github.com/user-attachments/assets/5543d15a-29c9-4e74-a219-f1afe1a8b552" />

```py
sns.scatterplot(x="total_bill", y="tip", data=tips)
plt.title('Scatterplot of Total Bill vs tip amount')
plt.xlabel('Total Bill')
plt.ylabel('Tip Amount')
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
plt.show()
```
<img width="563" height="453" alt="image" src="https://github.com/user-attachments/assets/19b2e736-9f04-47cd-b20e-cf0a36f39d03" />

## Volin Plot
```py
sns.violinplot(x="Pclass", y="Fare", data=tit)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```

<img width="571" height="453" alt="image" src="https://github.com/user-attachments/assets/81333681-d782-4316-9ae0-0cebccbfa417" />

## Histogram
```py
sns.histplot(data=tit,x="Pclass",hue="Survived",kde=True)
```

<img width="571" height="432" alt="image" src="https://github.com/user-attachments/assets/0502b36e-6fe1-4331-bd4b-70208a5482fe" />

## Density Plot
```py
sns.kdeplot(data=tit['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```
<img width="585" height="453" alt="image" src="https://github.com/user-attachments/assets/e9b0ce79-e337-462a-b363-493eb1abe8aa" />

## Heat Map
```py
numeric_df = tit.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```

<img width="597" height="503" alt="image" src="https://github.com/user-attachments/assets/003188d2-b37e-4fb6-bccc-02d5842ad27a" />

# Summary:
From this Experiment, I have explored the diffent types of visulaization techniques in seaborn and each of that helped in understanding the various aspects of the data. 
 - Firstly Line Plot shows trends over time
 - Secondly bar chart compares the catogories of data
 - Thirdly Scatter Plots reveal the relationships between numeric variables and lastly volin and histogram shows the distribution
