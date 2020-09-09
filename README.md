# ACM Research Coding Challenge (Fall 2020)

## No Collaboration Policy

**You may not collaborate with anyone on this challenge.** You _are_ allowed to use Internet documentation. If you _do_ use existing code (either from Github, Stack Overflow, or other sources), **please cite your sources in the README**.

## Submission Procedure

Please follow the below instructions on how to submit your answers.

1. Create a **public** fork of this repo and name it `ACM-Research-Coding-Challenge`. To fork this repo, click the button on the top right and click the "Fork" button.
2. Clone the fork of the repo to your computer using . `git clone [the URL of your clone]`. You may need to install Git for this (Google it).
3. Complete the Challenge based on the instructions below.
4. Email the link of your repo to research@acmutd.co with the same email you used to submit your application. Be sure to include your name in the email.

## Question One

![Image of Cluster Plot](ClusterPlot.png)
<br/>
Given the following dataset in `ClusterPlot.csv`, determine the number of clusters by using any clustering algorithm. **You're allowed to use any Python library you want to implement this**, just document which ones you used in this README file. Try to complete this as soon as possible.

Regardless if you can or cannot answer the question, provide a short explanation of how you got your solution or how you think it can be solved in your README.md file.

MY EXPLANATION >>

To be honest, I have zero experience with python or machine learning, and I wasn't able to get this done without a lot of help from google. My main source for the code is an article called "K-Means clustering in Python" by Bahar K. Uzan (LINK DOWN BELOW). It took me way longer than expected to read up on Python and the K-Means Algorithm and I tried my best to understand what the code was doing to determine the clusters.

Based on what I read from the article, I understand that the K-Means function genrates k random centroids on the plot(k being the number of clusters). Each value on the plot is assigned to the closest centroid and thus seperating the values into k amount of clusters. Since the png file of the plot explicitly shows two seperate clusters, I chose to just keep the k value at 2. However, we could find the optimum k value by comparing plots with various amounts of clusters and finding the average distance between a cluster's points and their's centroids. The choice I made to keep the k value at 2 resulted in a few discrepencies in the cluster seperation as you can probably notice at the end of the 'clustering.ipynb' file in my repo. 

To complete this program, I utiltized the 'numpy', 'panda', 'matplotlib', and 'sklearn' libraries. The first step was to import the csv file into a pandas object called data, with the V1 and V2 columns. Second step would be to build a K-Means model with 2 as the k value and plot points to create 2 random centroids behind the scenes and assign all the points to the center that they are closest to. Then I visualized the plot points seperated into two clusters. This is where I ended the program to keep the solution simple for this plot. For more accurate results, I need to build more KMeans models with higher K values. If you record the mean distance between the centers the points in their clusters with each K value and record the results in a graph, you will notice a trend that looks like an elbow as the K value increases. The K value at the end of the decline of average distance would be the elbow point as it is at the bottom of the elbow shape. This elbow point yields the optimum k value for a given plot and would result in the most accurate categorization of clusters.

Link to source article: https://bigdatascienc.wordpress.com/2017/12/29/k-means-clustering-in-python/
