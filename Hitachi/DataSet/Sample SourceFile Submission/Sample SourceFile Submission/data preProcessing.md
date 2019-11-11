**1. How did you approach the data pre-processing, data cleaning and data normalization? Attach the Queries used here.** [10 marks]
Approach.
1. Sort the data based on timestamp(As time passes the data population and commuter count will also changes.
2. Base on lattitude and logitude of source we will create the clusters.
3. Name those clusters and add a column in the data.
4. Skipped the portion of hyper parameter tunning of cluster distance because of time constraints.
5. Divide the data into two parts which have categorical data and numerical data.

**2. How did you approach the problem statement? Explain briefly** [5 Marks]
6. For categorical data we will use one hot encoding.
7. For numerical data we will use standard scaler.
8. Hyper parameter tune based on the xgboost.
9. Predict the value for the best answer in hyper parameter tunning.

**3.a. Give an example of similar data available on a larger scale and your recommended Hadoop architecture to maintain the data.** 
If data is available in large scale. we can easily divide the data base on cluster size.
For each cluster we have to generate a time series features such as single exponential and multi exponential.
Applying XGboost on these features will give a very good accuracy and f1 score.

**3.b. What is your recommended maintenance activity for the architecture mentioned above** [5 Marks]
For maintainence The architecture must be distributed between different servers. So if one is in training phase queries can be answered by the mirror servers.

