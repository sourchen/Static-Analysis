# Static-Analysis

### Data Description
Since I cannot receive real malware, I use the pefile analysis result saved in a dictionary (by calling `pefile_dump()` ) .
This dataset is composed of 40 malware samples, which are actually **from 4 families**. However, there is no class label of each item, so I can not perform classification and clustering might be a feasible solution.

> Therefore, in this project I try to cluster these 40 malwares into 4 groups. 

### What I did in this project... 
In this project, I extract some useful information from PE file by writing parsers. Next, I do data preprocessing by one hot encoding, label encoding to make data more useful, and do PCA to reduce dimension. At last, I cluster malwares by using k-means to cluster 4 malware families.
