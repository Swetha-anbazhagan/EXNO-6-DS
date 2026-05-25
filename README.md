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
import seaborn as sns
import matplotlib.pyplot as plt
df=pd.read_csv("titanic_dataset (2).csv")
df.head()
```
<img width="1204" height="412" alt="image" src="https://github.com/user-attachments/assets/0fd053f5-bef7-4508-ba21-8a1beef39694" />

```
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')

```
<img width="691" height="582" alt="image" src="https://github.com/user-attachments/assets/bf55af0e-9ba2-4c4e-90a4-12182b0a2cd0" />

````

x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi Line Plot')
````
<img width="698" height="577" alt="image" src="https://github.com/user-attachments/assets/cd57c362-2ed3-40fe-b9aa-9f14bc6eccf9" />

```

plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")

```

<img width="873" height="618" alt="image" src="https://github.com/user-attachments/assets/3ba1eaeb-0f34-4f4f-b181-2bb28c60742c" />

```
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()

```
<img width="733" height="587" alt="image" src="https://github.com/user-attachments/assets/62886391-3166-4c68-a2b4-3e9fe52d0491" />

```
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()


```
<img width="716" height="576" alt="image" src="https://github.com/user-attachments/assets/02902534-4668-4cb9-821c-13077a2a0d81" />

```
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)

```
<img width="733" height="575" alt="image" src="https://github.com/user-attachments/assets/927b6ab8-4f82-4829-8bbe-1ae93de3554e" />

```
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")

```

<img width="718" height="601" alt="image" src="https://github.com/user-attachments/assets/e017aa58-2fc0-4f26-893a-593f68124460" />

```
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()

```
<img width="685" height="544" alt="image" src="https://github.com/user-attachments/assets/629d4f3e-0994-4d84-b058-6b9c5daffb2e" />

```
sns.kdeplot(data=df['Age'], fill=True)
plt.title('Density Plot of Passenger Ages')
plt.show()

```
<img width="730" height="569" alt="image" src="https://github.com/user-attachments/assets/5bde86af-4a64-493d-be49-4c83182be635" />

```

numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()

```

<img width="748" height="634" alt="image" src="https://github.com/user-attachments/assets/0c0f3096-ba00-4497-b63a-6179c1ab15d9" />

# Result:
 Include your result here
