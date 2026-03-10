# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.1.Data Preparation: Load and explore customer data. 
2.Determine Optimal Clusters: Use the Elbow Method to find the best number of clusters.
3.Apply K Means Clustering: Perform clustering on customer data.
4.Visualize Segmented Customers: Plot clustered data to visualize customer segments. 

## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: kavya
RegisterNumber:  212225240110
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
from sklearn.cluster import KMeans
data = pd.read_csv("C:/Users/acer/Downloads/Mall_Customers (1).csv")
print(data.head())
X = data.iloc[:, [3, 4]].values
wcss = []
for i in range(1, 11):
    kmeans = KMeans(n_clusters=i, init='k-means++', random_state=42)
    kmeans.fit(X)
    wcss.append(kmeans.inertia_)
plt.figure(figsize=(8,5))
plt.plot(range(1, 11), wcss, marker='o')
plt.title('Elbow Method')
plt.xlabel('Number of Clusters')
plt.ylabel('WCSS')
plt.show()
kmeans = KMeans(n_clusters=5, init='k-means++', random_state=42)
y_kmeans = kmeans.fit_predict(X)
plt.figure(figsize=(8,6))
plt.scatter(X[y_kmeans == 0, 0], X[y_kmeans == 0, 1], s=100, c='red', label='Cluster 1')
plt.scatter(X[y_kmeans == 1, 0], X[y_kmeans == 1, 1], s=100, c='blue', label='Cluster 2')
plt.scatter(X[y_kmeans == 2, 0], X[y_kmeans == 2, 1], s=100, c='green', label='Cluster 3')
plt.scatter(X[y_kmeans == 3, 0], X[y_kmeans == 3, 1], s=100, c='cyan', label='Cluster 4')
plt.scatter(X[y_kmeans == 4, 0], X[y_kmeans == 4, 1], s=100, c='magenta', label='Cluster 5')
*/
```

## Output:
<img width="819" height="149" alt="image" src="https://github.com/user-attachments/assets/111f08a5-b24f-4a5f-b1f9-07933fce781b" />
<img width="718" height="541" alt="image" src="https://github.com/user-attachments/assets/eff2142f-a108-4d7b-a1ce-bad6c269fce3" />
<img width="696" height="532" alt="image" src="https://github.com/user-attachments/assets/244fab37-9a19-4da4-b7f6-92be3fc931af" />


## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
