# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import pandas as pd and matplotlib.pyplot as plt
2. Get the info and also obtain the sum of any null values
3. Importing KMeans from sklearn.cluster we group the similar datas
4. Grouping similar datas gives us a elbow shaped graph which is called the Elbow method.
5.Print the number of clusters obtained
6. Giving the clustered data differnet colors and presenting as a scatter plot
7. Print the obtained graph.

## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: Meetha Prabhu
RegisterNumber: 212222240065

**
import pandas as pd
import matplotlib.pyplot as plt
data =pd.read_csv("/content/Mall_Customers (1).csv")
**
**
data.head()
**
**
data.info()
**
**
data.isnull().sum()
**
**
from sklearn.cluster import KMeans
wcss=[]
for i in range(1,11):
  kmeans = KMeans(n_clusters = i,init = "k-means++")
  kmeans.fit(data.iloc[:,3:])
  wcss.append(kmeans.inertia_)

plt.plot(range(1,11),wcss)
plt.xlabel("No. of Clusters")
plt.ylabel("wcss")
plt.title("Elbow Method")
**
**
km = KMeans(n_clusters = 5)
print("K-Means")
km.fit(data.iloc[:,3:])
**
**
y_pred = km.predict(data.iloc[:,3:])
print("Array:")
y_pred
**
**
data["cluster"] = y_pred
df0 = data[data["cluster"]==0]
df1 = data[data["cluster"]==1]
df2 = data[data["cluster"]==2]
df3 = data[data["cluster"]==3]
df4 = data[data["cluster"]==4]
plt.scatter(df0["Annual Income (k$)"],df0["Spending Score (1-100)"],c="red",label="cluster0")
plt.scatter(df1["Annual Income (k$)"],df1["Spending Score (1-100)"],c="yellow",label="cluster1")
plt.scatter(df2["Annual Income (k$)"],df2["Spending Score (1-100)"],c="pink",label="cluster2")
plt.scatter(df3["Annual Income (k$)"],df3["Spending Score (1-100)"],c="green",label="cluster3")
plt.scatter(df4["Annual Income (k$)"],df4["Spending Score (1-100)"],c="purple",label="cluster4")
print("Customer Segments")
print("Customer Segement")
plt.legend()
plt.title("Customer Segments")
**


*/
```

## Output:
![image](https://github.com/Meetha22003992/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119401038/6d5290a4-2365-4927-98a6-d4d9a0ce5a65)

![image](https://github.com/Meetha22003992/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119401038/80962773-d911-41e6-be11-30f97ba24301)

![image](https://github.com/Meetha22003992/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119401038/c19bb3ed-fd99-481b-8012-828b427143e9)

![image](https://github.com/Meetha22003992/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119401038/63c3508d-2dcb-4df9-815c-c7d3586ad56d)

![image](https://github.com/Meetha22003992/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119401038/fe94d64d-686c-441d-9e5c-b1d33da887bf)

![image](https://github.com/Meetha22003992/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119401038/18f98161-5470-41b8-a32a-ffc2a882eb54)

![image](https://github.com/Meetha22003992/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119401038/908a914a-d53d-4e9c-a637-a6af94c2e0f1)


## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
