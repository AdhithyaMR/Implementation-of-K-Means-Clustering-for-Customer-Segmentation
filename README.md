# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the necessary packages using import statement.
2. Read the given csv file using read_csv() method and print the number of contents to be displayed using df.head().
3. Import KMeans and use for loop to cluster the data.
4. Predict the cluster and plot data graphs.
5. Print the outputs and end the program

## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: Adhithya M R
RegisterNumber:  212222240002


import pandas as pd
import matplotlib.pyplot as plt
data = pd.read_csv("/content/Mall_Customers (1).csv")

data.head()

data.isnull().sum()

from sklearn.cluster import KMeans
wcss=[]

for i in range(1,11):
  kmeans=KMeans(n_clusters=i,init="k-means++")
  kmeans.fit(data.iloc[:,3:])
  wcss.append(kmeans.inertia_)

plt.plot(range(1,11),wcss)
plt.xlabel("No.of clusters")
plt.ylabel("wcss")
plt.title("Elbow Method")

km=KMeans(n_clusters=5)
km.fit(data.iloc[:,3:])

y_pred=km.predict(data.iloc[:,3:])
y_pred

data["cluster"]=y_pred
df0=data[data["cluster"]==0]
df1=data[data["cluster"]==1]
df2=data[data["cluster"]==2]
df3=data[data["cluster"]==3]
df4=data[data["cluster"]==4]
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
### Data.head()

![278858717-21ec9e1a-063b-41f3-89e0-4448b05b1403](https://github.com/AdhithyaMR/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/118834761/57ff5af0-e941-48a1-818a-c4f619470a51)

### Data.info()

![278859011-99cce45e-1d31-4b58-aadb-4e7e232a0124](https://github.com/AdhithyaMR/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/118834761/33d766f4-6481-462c-a2b6-5fd0a3416dae)

### Data.isnull.sum() function:

![278859029-f671bfe7-5eb8-4320-a2e7-9f385ed506c4](https://github.com/AdhithyaMR/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/118834761/4c13171b-b59e-40c0-9f26-38361f9dd1fd)

### Elbow Method Graph:
![278859129-7b9d6077-6dff-4792-a6f6-577c384d4ab7](https://github.com/AdhithyaMR/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/118834761/82c5a406-5a01-41c4-9fd5-040696498e0d)

### KMeans clusters:

![278859151-fb551b02-8440-47a5-96ed-ef757fe0b87f](https://github.com/AdhithyaMR/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/118834761/d0d08318-23ad-47ae-88d0-44566ab5e745)
### y_prediction:
![278859213-f70fca1e-ddbd-46d7-b7e2-30510c302825](https://github.com/AdhithyaMR/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/118834761/eecae550-4062-4d7e-801d-4a03c18b9b24)


### Customer Segments Graph:

![278859231-a57174c0-a293-494f-84d0-079c2ced8120](https://github.com/AdhithyaMR/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/118834761/4e075d51-0685-40b6-9f76-050b6b1a4c24)



## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
