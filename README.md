# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY
### NAME : P.SUDHISHNA
### REG NO: 212224040336
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
df=pd.read_csv("/content/titanic_dataset.csv")
df.head()

```
<img width="1483" height="239" alt="Screenshot 2025-11-10 102603" src="https://github.com/user-attachments/assets/5d4e7274-5f2c-42c0-9c18-3d333b94635a" />


### 1.Line Plot
```
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')

```
<img width="777" height="576" alt="Screenshot 2025-11-10 102834" src="https://github.com/user-attachments/assets/7352dd71-08e8-4463-a4b3-21f4fce45efc" />

### 2.MultiLine Plot

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
<img width="770" height="574" alt="Screenshot 2025-11-10 103005" src="https://github.com/user-attachments/assets/ec3461d6-c8ac-4534-af82-4bba27e6542b" />

### TO VISUALIZE RELATIONSHIPS

### 1.Bar Chart

```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```
<img width="907" height="606" alt="Screenshot 2025-11-10 103303" src="https://github.com/user-attachments/assets/79f71965-e8ad-4354-a4cb-8ca995bb153c" />

### 2.Scatter Plot

```
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```
<img width="807" height="583" alt="Screenshot 2025-11-10 103511" src="https://github.com/user-attachments/assets/96ea1186-1203-4805-a029-d2c23e059577" />

### 3.Bubble chart

```
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()

```
<img width="784" height="579" alt="Screenshot 2025-11-10 103650" src="https://github.com/user-attachments/assets/e1f62610-ac6f-407c-af0a-920a7f89fe24" />

### TO CAPTURE DISTRIBUTIONS

### 1.Histogram
```
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)

```

<img width="800" height="572" alt="image" src="https://github.com/user-attachments/assets/d801d100-4cf0-4f8a-a2d4-712ec88004ae" />

### 2.Box Plot

```
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")

```
<img width="757" height="605" alt="Screenshot 2025-11-10 104118" src="https://github.com/user-attachments/assets/85c052c4-4c34-4e81-abf0-50ab9ffb6d81" />

### 3.Violin Plot

```
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()

```

<img width="806" height="575" alt="Screenshot 2025-11-10 104237" src="https://github.com/user-attachments/assets/b04f306e-3bc2-41e9-9ccc-18b7f88a0867" />

### 4.Density Plot

```
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()

```
<img width="913" height="796" alt="Screenshot 2025-11-10 110326" src="https://github.com/user-attachments/assets/08318d0c-58be-4beb-86a7-f42afa70fc92" />

### 5.Heatmap

```
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()

```

<img width="886" height="644" alt="Screenshot 2025-11-10 110507" src="https://github.com/user-attachments/assets/eaed3f5e-4fd1-4473-8590-189007207645" />














# Result:
 Thus, the Data Visualization using seaborn python library for the given data is implemented successfully

 # Summary:
In this experiment, data visualization was performed using the **Seaborn** library in Python. The dataset was first loaded and analyzed to understand its structure. Various visualization techniques such as bar plots, histograms, scatter plots, and heatmaps were applied to identify patterns, correlations, and trends in the data. Each function was customized with proper parameters for better clarity and presentation. The experiment helped in interpreting complex data easily through visual insights. Overall, Seaborn proved to be an effective tool for clear and attractive graphical analysis.
