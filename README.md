# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import pandas and matplotlib.pyplot
2.Read the dataset and transform it
3.Import KMeans and fit the data in the model
4.Plot the Cluster graph

## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: Vineela Shaik
RegisterNumber: 212223040243

import pandas as pd
import matplotlib.pyplot as plt
data = pd.read_csv("/content/Mall_Customers.csv")
data.head()
data.info()
data.isnull().sum()
from sklearn.cluster import KMeans
wcss = []  #Within-Cluster sum of square. 
for i in range(1,11):
  kmeans=KMeans(n_clusters = i,init = "k-means++")
  kmeans.fit(data.iloc[:,3:])
  wcss.append(kmeans.inertia_)
plt.plot(range(1,11),wcss)
plt.xlabel("No of Clusters")
plt.ylabel("wcss")
plt.title("Elbow Method")
km = KMeans(n_clusters = 5)
km.fit(data.iloc[:,3:])
y_pred = km.predict(data.iloc[:,3:])
y_pred
data["cluster"] = y_pred
df0 = data[data["cluster"]==0]
df1 = data[data["cluster"]==1]
df2 = data[data["cluster"]==2]
df3 = data[data["cluster"]==3]
df4 = data[data["cluster"]==4]
plt.scatter(df0["Annual Income (k$)"],df0["Spending Score (1-100)"],c="red",label="cluster0")
plt.scatter(df1["Annual Income (k$)"],df1["Spending Score (1-100)"],c="black",label="cluster1")
plt.scatter(df2["Annual Income (k$)"],df2["Spending Score (1-100)"],c="blue",label="cluster2")
plt.scatter(df3["Annual Income (k$)"],df3["Spending Score (1-100)"],c="green",label="cluster3")
plt.scatter(df4["Annual Income (k$)"],df4["Spending Score (1-100)"],c="magenta",label="cluster4")
plt.legend()
plt.title("Customer Segments")
*/
```

## Output:
#### data.head() function
![Screenshot 2024-04-24 194332](https://github.com/Aadithya2201/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/145917810/6bfa2030-f79d-4b14-8ddf-928beecf27fc)

#### data.info()
![Screenshot 2024-04-24 194343](https://github.com/Aadithya2201/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/145917810/dbb83c42-82cc-4d61-9b26-cc2d4139ef2b)

#### data.isnull().sum() function
![Screenshot 2024-04-24 194352](https://github.com/Aadithya2201/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/145917810/3bfe35c7-557b-439e-a88d-ff9483021dd7)

#### Elbow method Graph
![Screenshot 2024-04-24 194418](https://github.com/Aadithya2201/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/145917810/e0dfea46-a14f-429f-87c0-a31b10af0882)

#### KMeans clusters
![Screenshot 2024-04-24 194429](https://github.com/Aadithya2201/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/145917810/08cd9653-3816-4882-b577-ba64716026c0)
![Screenshot 2024-04-24 194444](https://github.com/Aadithya2201/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/145917810/43f220ae-dfaf-469f-adde-c9bb8a149a96)

#### Customer segments Graph
![Screenshot 2024-04-24 194500](https://github.com/Aadithya2201/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/145917810/e0adcac8-1900-41d4-9cad-7f2b980521fa)
## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
