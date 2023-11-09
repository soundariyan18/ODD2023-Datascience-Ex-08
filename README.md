# Ex-08-Data-Visualization-
# AIM
To Perform Data Visualization on a complex dataset and save the data to a file.

# Explanation
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# ALGORITHM
## STEP 1
Read the given Data

## STEP 2
Clean the Data Set using Data Cleaning Process

## STEP 3
Apply Feature generation and selection techniques to all the features of the data set

## STEP 4
Apply data visualization techniques to identify the patterns of the data.

## CODE AND  OUTPUT

```
NAME: SOUNDARIYAN M.N

REG: 212222230146
```


import matplotlib.pyplot as plt
x_values=[0,1,2,3,4,5]
y_values=[0,1,4,9,16,25]
plt.plot(x_values,y_values)

![image](https://github.com/soundariyan18/ODD2023-Datascience-Ex-08/assets/119393307/33fafaed-c1a2-436b-b09a-715cbcada30d)

x=[1,2,3]
y=[2,4,1]
plt.plot(x,y)
plt.xlabel('x-values')
plt.ylabel('y-values')
plt.title('My first graph')


x1=[1,2,3]
y1=[2,4,1]
x2=[1,2,3]
y2=[4,1,3]
plt.plot(x1,y1,label='line 1')
plt.plot(x2,y2,label='line 2')
plt.xlabel('x-values')
plt.ylabel('y-values')
plt.title('Two lines on same graph')

![image](https://github.com/soundariyan18/ODD2023-Datascience-Ex-08/assets/119393307/8df63f40-a86b-4af6-882f-a000f2fcca1b)

x=[1,2,3,4,5,6]
y=[2,4,1,5,2,6]

plt.plot(x,y,color='green',linestyle='dashed',linewidth=3,marker='o',markerfacecolor='blue',markersize=12)
plt.ylim(1,8)
plt.xlim(1,8)
plt.xlabel('x-values')
plt.ylabel('y-values')
plt.title('some cool customizations')

![image](https://github.com/soundariyan18/ODD2023-Datascience-Ex-08/assets/119393307/f298cb5d-ef00-4a70-aa1d-cc2f550c8672)

yield_apples=[0.8,0.91,0.919,0.926,0.929,0.93]
plt.plot(yield_apples)

![image](https://github.com/soundariyan18/ODD2023-Datascience-Ex-08/assets/119393307/30de0f5f-77b5-49e4-a1c1-aefa902f96df)

years=[2010,2011,2012,2013,2014,2015]
yield_apples=[0.895,0.91,0.919,0.926,0.929,0.931]
plt.plot(years,yield_apples)

![image](https://github.com/soundariyan18/ODD2023-Datascience-Ex-08/assets/119393307/55b7d4aa-3da0-48f2-91d2-73f1d4cad6c1)

x=[1,2,3,4,5]
y1=[10,12,14,16,18]
y2=[5,7,9,11,13]
y3=[2,4,6,8,10]
plt.fill_between(x,y1,color='blue')
plt.fill_between(x,y2,color='yellow')
plt.plot(x,y1,color='black')
plt.plot(x,y2,color='white')
plt.legend(['y1','y2'])

![image](https://github.com/soundariyan18/ODD2023-Datascience-Ex-08/assets/119393307/14552e98-1a48-4634-a54c-a404c1b8b718)

import seaborn as sns
import matplotlib.pyplot as plt

x=[1,2,3,4,5]
y=[3,6,2,7,1]

sns.lineplot(x=x,y=y)

![image](https://github.com/soundariyan18/ODD2023-Datascience-Ex-08/assets/119393307/a6bf5c9f-a759-4e59-8857-7c022e522cb5)

x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]

sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title("Multi-Line Plot")
plt.xlabel("X Label")
plt.ylabel("Y Label")

![image](https://github.com/soundariyan18/ODD2023-Datascience-Ex-08/assets/119393307/05cb01c7-ff8a-45c2-895d-3fac23d1db4c)

import matplotlib.pyplot as plt
values=[5,6,3,7,2]
names=["A","B","C","D","E"]
plt.bar(names,values,color="green")
plt.show()

![image](https://github.com/soundariyan18/ODD2023-Datascience-Ex-08/assets/119393307/fdde978e-159e-4fbf-9cb6-ee5248592753)

plt.barh(names,values,color="black")
plt.show()

![image](https://github.com/soundariyan18/ODD2023-Datascience-Ex-08/assets/119393307/ce4384fc-545f-49bb-a194-081541789ba9)

height=[10,24,36,40,5]
names=["one","two","three","four","five"]
c1=["red","green"]
c2=["b","g"]
plt.bar(names,height,width=0.8,color=c1)
plt.xlabel("x-axis")
plt.ylabel("y-axis")
plt.title("My Bar chart!!!!!!!!!!!!")

![image](https://github.com/soundariyan18/ODD2023-Datascience-Ex-08/assets/119393307/7eaf3654-0194-43af-bfb7-ff46434045ff)

import seaborn as sns
import matplotlib.pyplot as plt
tips= sns.load_dataset("tips")
avg_total_bill = tips.groupby("day")['total_bill'].mean()
avg_tip =tips.groupby('day')['tip'].mean()
plt.figure(figsize=(8, 6))
p1 = plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill')
p2 = plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label='Tip')
plt.xlabel('Day of the Week')
plt.ylabel('Amount')
plt.title("Average total bil and tip by day")
plt.legend()

![image](https://github.com/soundariyan18/ODD2023-Datascience-Ex-08/assets/119393307/5fdaf6ad-2f24-48b2-9864-de1c5807b073)

import seaborn as sns
dt=sns.load_dataset("tips")
sns.barplot(x="day",y="total_bill",hue="sex",data=dt,palette="Set1")
plt.xlabel('Day of the Week')
plt.ylabel('Total bill')
plt.title("Total bill by day and gender")

import pandas as pd
tit=pd.read_csv("/content/titanic_dataset.csv")

![image](https://github.com/soundariyan18/ODD2023-Datascience-Ex-08/assets/119393307/72f523d3-5242-431d-b083-78989937f923)


plt.figure(figsize=(8,5))
sns.barplot(x="Embarked",y="Fare",data=tit,palette="rainbow")
plt.title("Fare of passengers by embarked town")

![image](https://github.com/soundariyan18/ODD2023-Datascience-Ex-08/assets/119393307/328d4162-08a4-46a4-a6b7-523ec1db325c)

import matplotlib.pyplot as plt
x_values = [0,1,2,3,4,5]
y_values = [0,1,4,9,16,25]
plt.scatter (x_values, y_values, s=30, color="blue")
plt.show()

![image](https://github.com/soundariyan18/ODD2023-Datascience-Ex-08/assets/119393307/c04da072-3ff1-4c3d-bd8f-df4b367bf483)

x = [1,2,3,4,5,6,7,8,9,10]
y = [2,4,5,7,6,8,9,11,12,12]
plt.scatter(x,y,label = "stars",color='green',marker='*',s=30)
plt.title("scatter plot")
plt.legend()

![image](https://github.com/soundariyan18/ODD2023-Datascience-Ex-08/assets/119393307/df1dc2ae-8eea-4064-9b8c-83c022aa8f80)


import seaborn as sns
tips = sns.load_dataset('tips')
sns.scatterplot(x= 'total_bill', y='tip', hue='sex',data=tips)
plt.xlabel('Total Bill')
plt.ylabel('Tip Amount')
plt.title('Scatter Plot of Total Bill vs. Tip Amount')

![image](https://github.com/soundariyan18/ODD2023-Datascience-Ex-08/assets/119393307/4fd1ee7a-58d2-4d88-b0ae-eca73a5b54bf)


import matplotlib.pyplot as plt
ages=[2,5,70,40,30,45,50,45,43,40,44,60,7,13,57,18,90,77,32,21,20,40]
range=(0,100)
bins=10
plt.hist(ages,bins,range,color="green",histtype="bar",rwidth=0.8)
plt.xlabel("age")
plt.ylabel("No.of.People")
plt.title("My Histogram")

![image](https://github.com/soundariyan18/ODD2023-Datascience-Ex-08/assets/119393307/821e264f-761e-4798-bb5d-7d1f327fe77a)


x=[2,1,6,2,4,2,4,8,9,4,2,4,10,6,4,5,7,7,3,2,7,5,3,5,9,2,1]
plt.hist(x,bins=10,color="black",alpha=0.5)

![image](https://github.com/soundariyan18/ODD2023-Datascience-Ex-08/assets/119393307/8422d1b3-a0cf-46ed-a138-a7f34e1191c1)

import seaborn as sns
import numpy as np
import pandas as pd

np.random.seed(1)
num_var=np.random.randn(1000)
num_var=pd.Series(num_var,name="Numerical Variable")
num_var

![image](https://github.com/soundariyan18/ODD2023-Datascience-Ex-08/assets/119393307/f6297fdb-6658-4716-a22c-5ef9bf4b08fd)

sns.histplot(data=num_var,kde=True)

![image](https://github.com/soundariyan18/ODD2023-Datascience-Ex-08/assets/119393307/25c047ed-d7fe-48f5-bb92-b32f3f39b465)

import pandas as pd
import seaborn as sns
df=pd.read_csv("/content/titanic_dataset.csv")

sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)

![image](https://github.com/soundariyan18/ODD2023-Datascience-Ex-08/assets/119393307/3d176394-cd28-4f03-9235-d8f761253ae8)

import matplotlib.pyplot as plt
import numpy as np

np.random.seed(0)
data=np.random.normal(loc=0,scale=1,size=100)
data

![image](https://github.com/soundariyan18/ODD2023-Datascience-Ex-08/assets/119393307/90bcdffc-dc2a-4f85-bc15-a010f29564ad)

fig,ax=plt.subplots()
ax.boxplot(data)
ax.set_xlabel("Data")
ax.set_ylabel("Values")
ax.set_title("Boxplot")

![image](https://github.com/soundariyan18/ODD2023-Datascience-Ex-08/assets/119393307/48f397d9-67bc-41ee-93be-45f8fc7c8308)

import seaborn as sns
import pandas as pd
tips = sns.load_dataset('tips')
sns.boxplot(x=tips["day"], y=tips["total_bill"], hue=tips["smoker"], data = tips)

![image](https://github.com/soundariyan18/ODD2023-Datascience-Ex-08/assets/119393307/346b5763-ca89-4ed2-be3a-6626cf9c69b4)

sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6,boxprops={"facecolor": "lightblue", "edgecolor": "darkblue"},
whiskerprops={"color": "black", "linestyle":"--", "linewidth": 1.5 },capprops={"color": "black", "linestyle": "--", "linewidth":1.5})

![image](https://github.com/soundariyan18/ODD2023-Datascience-Ex-08/assets/119393307/7f33540f-7ee5-4489-bd7f-267ebb7c5c7d)

sns.boxplot(x='day',y='total_bill',data= tips)
plt.title("Age by Passenger Class, Titanic")

![image](https://github.com/soundariyan18/ODD2023-Datascience-Ex-08/assets/119393307/b565a073-3d2c-4170-a0e3-ceb9ab1ecbe8)

sns.violinplot (x="day", y="total_bill", hue="smoker", data= tips, linewidth=2, width=0.6,)


data = np.random.randint(low = 1, high = 100, size = (10,10))
print("The data to be plotted: \n")
print (data)

![image](https://github.com/soundariyan18/ODD2023-Datascience-Ex-08/assets/119393307/be51949f-ae94-4322-981e-95827a1225f4)

hm=sns.heatmap(data=data)

![image](https://github.com/soundariyan18/ODD2023-Datascience-Ex-08/assets/119393307/4b82b1a2-0eb5-47d6-b178-d96ca3414f07)

import pandas as pd
import seaborn as sns
df=pd.read_csv("/content/titanic_dataset.csv")

import matplotlib.pyplot as plt
ages= [2,5, 70, 40, 30, 45, 50,45, 43, 40,44, 60, 7,13, 57, 18, 90, 77,32, 21, 20, 40]
range = (0, 100)
bins = 10
sns.histplot(data=df,x="Pclass",hue="Survived")
plt. xlabel ('age')
plt.ylabel ('No. of people')
plt. title ('My histogram')
plt.show()

![image](https://github.com/soundariyan18/ODD2023-Datascience-Ex-08/assets/119393307/b9117246-723f-4818-9ba0-8754392675f6)
```

## Result:
Hence the data visualization method for the given dataset applied successfully.
