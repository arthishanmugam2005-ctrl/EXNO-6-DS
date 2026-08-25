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
df=pd.read_csv("titanic_dataset.csv")
df.head()
```

<img width="998" height="182" alt="image" src="https://github.com/user-attachments/assets/a5debf58-b213-45c9-a619-d3303b4e52d7" />

```
#1.Line Plot
```
x=[1,2,3,4,5] 
y=[3,6,2,7,1] 
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```

<img width="571" height="476" alt="image" src="https://github.com/user-attachments/assets/3eca8ab1-0bc6-47ad-9294-06e5ac77d4ae" />


#2.Multi Line Plot 
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

<img width="552" height="473" alt="image" src="https://github.com/user-attachments/assets/097d3b96-d454-4ec1-b91b-0fb304e19eea" />


#TO VISUALIZE RELATIONSHIPS
#1.Bar Chart
```
plt.figure(figsize=(8,5)) 
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow') 
plt.title("Fare Of Passenger By Embarked Town")
```
<img width="625" height="462" alt="image" src="https://github.com/user-attachments/assets/0cd8dd58-f82f-400d-86d1-5181b76eeb33" />
#2.Scatter Plot 
```
sns.scatterplot(x="Age", y="Fare", data=df) 
plt.title('Scatterplot of Age vs Fare')
plt.show()
```

<img width="618" height="456" alt="image" src="https://github.com/user-attachments/assets/edcbe494-c045-4e1d-a04e-d6b2cccb48e3" />
#3.Bubble Chart
```
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class') 
plt.show()
```

<img width="601" height="457" alt="image" src="https://github.com/user-attachments/assets/659aa5e3-e332-4a50-8154-cfe022a49766" />
#TO CAPTURE DISTRIBUTIONS 
#1.Histogram 
```
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```

<img width="593" height="471" alt="image" src="https://github.com/user-attachments/assets/4d2c1739-5711-4cd6-afe0-f1b39a6f4586" />
#2.Box Plot 
```
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow') 
plt.title("Age By Passenger Class")
```

<img width="585" height="502" alt="image" src="https://github.com/user-attachments/assets/971fe756-8fe7-4d2b-b6ec-5883eaf49af7" />

#3.Violin Plot 
```
sns.violinplot(x="Pclass", y="Fare", data=df) 
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```

<img width="611" height="462" alt="image" src="https://github.com/user-attachments/assets/c2f10efb-de65-44cc-9fdd-cd9781040020" />

#4.Density Plot
```
sns.kdeplot(data=df['Age'], shade=True) 
plt.title('Density Plot of Passenger Ages')
plt.show()
```

<img width="606" height="450" alt="image" src="https://github.com/user-attachments/assets/73036b36-6bec-4ba9-9b63-849d85ced977" />
#5.Heatmap 
```
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr() 
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm') 
plt.title('Heatmap of Titanic Dataset') 
plt.show()
```

<img width="612" height="522" alt="image" src="https://github.com/user-attachments/assets/7dce8943-b9ea-4654-bb44-c702ebe603a4" />


# Result:
 Include your result here
