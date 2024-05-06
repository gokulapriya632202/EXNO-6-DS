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
import seaborn as sns
import matplotlib.pyplot as plt
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
```
![Screenshot 2024-05-06 135319](https://github.com/gokulapriya632202/EXNO-6-DS/assets/119560302/204225bb-c36d-4f3b-9b66-c3ed7bc928b4)

```
df=sns.load_dataset('tips')
df
```
![Screenshot 2024-05-06 135336](https://github.com/gokulapriya632202/EXNO-6-DS/assets/119560302/0460f242-82e5-4998-9e4b-744d3f4f58c0)

```
sns.lineplot(x='total_bill',y='tip',data=df,hue='sex',linestyle='solid',legend='auto')
```
![Screenshot 2024-05-06 135354](https://github.com/gokulapriya632202/EXNO-6-DS/assets/119560302/abc44a4e-8c37-46da-b7b2-2c1fc15e7fbd)

```
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi-Line Plot')
plt.xlabel('X Label')
plt.ylabel('Y Lbel')
```
![Screenshot 2024-05-06 135428](https://github.com/gokulapriya632202/EXNO-6-DS/assets/119560302/04a7ab2a-ef5b-4405-b8f2-ed701df8d8e2)

```
import seaborn as sns
import matplotlib.pyplot as plt
tips=sns.load_dataset('tips')
avg_total_bill=tips.groupby('day')['total_bill'].mean()
avg_tip=tips.groupby('day')['tip'].mean()
plt.figure(figsize=(8,6))
p1=plt.bar(avg_total_bill.index,avg_total_bill,label='Total Bill')
p2=plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip')
plt.xlabel('Day of the Week')
plt.ylabel('Amount')
plt.title("Average Total Bill and Tip by Day")
plt.legend()
```
![Screenshot 2024-05-06 135520](https://github.com/gokulapriya632202/EXNO-6-DS/assets/119560302/eaebc25a-61f4-4c18-b3ab-2bd38a611daa)

```
avg_total_bill=tips.groupby('time')['total_bill'].mean()
avg_tip=tips.groupby('time')['tip'].mean()
p1=plt.bar(avg_total_bill.index,avg_total_bill,label='Total Bill',width=0.4)
p2=plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip',width=0.4)
plt.xlabel('Time of Day')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Time of Day')
plt.legend()
```
![Screenshot 2024-05-06 135532](https://github.com/gokulapriya632202/EXNO-6-DS/assets/119560302/047b1c2a-81ec-4a8a-a209-0977b84f3739)

```
years=range(2000, 2012)
apples=[0.895, 0.91, 0.919, 0.926, 0.929, 0.931, 0.934, 0.936, 0.937, 0.9375, 0.9372, 0.939] 
oranges = [0.962, 0.941, 0.930, 0.923, 0.918, 0.908, 0.907, 0.904, 0.901, 0.898, 0.9, 0.896, ]
plt.bar(years, apples)
plt.bar(years, oranges, bottom=apples)
```
![Screenshot 2024-05-06 135547](https://github.com/gokulapriya632202/EXNO-6-DS/assets/119560302/5be3621c-9f31-42c4-9970-dccfde258e94)

```
import seaborn as sns
dt= sns.load_dataset('tips')
# Bar plot with hue parameter
sns.barplot(x='day', y='total_bill', hue='sex', data=dt, palette='Set1')
plt.xlabel('Day of the week')
plt.ylabel('Total Bill')
plt.title('Total Bill by Day and Gender')
```
![Screenshot 2024-05-06 135601](https://github.com/gokulapriya632202/EXNO-6-DS/assets/119560302/151b241d-e0a5-4739-b178-39e1680b252e)

```
tit=pd.read_csv("titanic_dataset.csv")
tit
```
![Screenshot 2024-05-06 135618](https://github.com/gokulapriya632202/EXNO-6-DS/assets/119560302/efca574a-0f6e-4ba3-83e5-68a649084b05)

```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow') 
plt.title("Fare of Passenger by Embarked Town")
```
![Screenshot 2024-05-06 135642](https://github.com/gokulapriya632202/EXNO-6-DS/assets/119560302/fe193fce-4b46-4374-b7db-410c880269c4)

```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow', hue='Pclass') 
plt.title("Fare of Passenger by Embarked Town, Divided by Class")
```
![Screenshot 2024-05-06 135704](https://github.com/gokulapriya632202/EXNO-6-DS/assets/119560302/0ab2eec6-324f-4f08-80c7-0358b9927a7f)

```
import seaborn as sns
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill',y='tip',hue='sex',data=tips)
plt.xlabel('Total Bill')
plt.ylabel('Tip Amount')
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```
![Screenshot 2024-05-06 135824](https://github.com/gokulapriya632202/EXNO-6-DS/assets/119560302/55f500ae-4f09-4396-b6ac-091883bcab9d)

```
num_var = np.random.randn(1000)
num_var=pd.Series(num_var, name = "Numerical variable")
num_var
```
![Screenshot 2024-05-06 135835](https://github.com/gokulapriya632202/EXNO-6-DS/assets/119560302/a0495bfe-d5ef-46f0-acdd-20f9807a09af)

```
sns.histplot(data = num_var, kde = True)
```
![Screenshot 2024-05-06 135846](https://github.com/gokulapriya632202/EXNO-6-DS/assets/119560302/99ba9d2c-e99b-41d5-b28a-c39904909c80)

```
df=pd.read_csv("titanic_dataset.csv")
sns.histplot(data=df,x="Pclass", hue="Survived", kde=True)
```
![Screenshot 2024-05-06 135857](https://github.com/gokulapriya632202/EXNO-6-DS/assets/119560302/07b994d6-7f25-4d4f-89a5-4ccd8c7baaf7)

```
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'], y=tips ['total_bill'], hue=tips['sex'])
```
![Screenshot 2024-05-06 135913](https://github.com/gokulapriya632202/EXNO-6-DS/assets/119560302/6cee15e2-368b-469f-9cf8-9dfed27da23a)

```
sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, boxprops={"facecolor": "lightblue", "edgecolor": "darkblue"},
whiskerprops={"color": "black", "linestyle": "--", "linewidth": 1.5}, capprops={"color": "black", "linestyle": "--", "linewidth": 1.5})
```
![Screenshot 2024-05-06 135924](https://github.com/gokulapriya632202/EXNO-6-DS/assets/119560302/ad160852-4ff0-406c-9b5f-0f9683130129)

```
sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6,
palette="Set3", inner="quartile")
plt.xlabel("Day of the week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```
![Screenshot 2024-05-06 135939](https://github.com/gokulapriya632202/EXNO-6-DS/assets/119560302/95a3b3cd-42d2-4427-b54f-898e617de288)

```
mart=pd.read_csv("titanic_dataset.csv")
mart
```
![Screenshot 2024-05-06 135954](https://github.com/gokulapriya632202/EXNO-6-DS/assets/119560302/6a469d20-2d55-465f-9c16-b58b3e9d7278)

```
mart=mart[['PassengerId', 'Survived', 'Age', 'Name', 'Ticket', 'Embarked']] 
mart.head(10)
```
![Screenshot 2024-05-06 140005](https://github.com/gokulapriya632202/EXNO-6-DS/assets/119560302/9e68b84d-f9a1-454c-a47b-f356a9f7a74f)

```
sns.kdeplot(data=mart,x='PassengerId')
```
![Screenshot 2024-05-06 140016](https://github.com/gokulapriya632202/EXNO-6-DS/assets/119560302/57ad8863-73d5-40f4-8411-114da815c493)

```
sns.kdeplot(data=mart,x='Age')
```
![Screenshot 2024-05-06 140027](https://github.com/gokulapriya632202/EXNO-6-DS/assets/119560302/16bf3f46-a294-4a3c-a2de-4b31f0eaf6cf)

```
sns.kdeplot(data=mart)
```
![Screenshot 2024-05-06 140039](https://github.com/gokulapriya632202/EXNO-6-DS/assets/119560302/9cf4a5c2-eebc-4f87-9695-2f743470d7a4)

```
sns.kdeplot(data=mart,x='PassengerId',hue='Survived',multiple='stack')
```
![Screenshot 2024-05-06 140051](https://github.com/gokulapriya632202/EXNO-6-DS/assets/119560302/b179c3ff-5873-42d0-809c-ae82a0ebf904)

```
sns.kdeplot(data=mart,x='PassengerId',y='Survived')
```
![Screenshot 2024-05-06 140102](https://github.com/gokulapriya632202/EXNO-6-DS/assets/119560302/046694c2-9d51-431a-8a8a-4c855fcc8b13)

```
data = np.random.randint(low = 1, high = 100, size = (10,10))
hm=sns.heatmap(data=data,annot=True)
```
![Screenshot 2024-05-06 140113](https://github.com/gokulapriya632202/EXNO-6-DS/assets/119560302/b8449819-987d-4016-acc1-ac10d3af7733)

```
hm=sns.heatmap(data=data)
```
![Screenshot 2024-05-06 140135](https://github.com/gokulapriya632202/EXNO-6-DS/assets/119560302/52738ec8-df7e-4af8-a709-dd3d328ee6b1)

# Result:
   Thus, all the data visualization techniques of seaborn has been implemented.


