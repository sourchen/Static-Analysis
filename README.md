# Static-Analysis

Static program analysis is the analysis of computer software that is performed without actually executing programs, in contrast with dynamic analysis, which is analysis performed on programs while they are executing.

### Data Description
Since I cannot receive real malware, I use the pefile analysis result saved in a dictionary (by calling `pefile_dump()` ) .
This dataset is composed of 40 malware samples, which are actually **from 4 families**. However, there is no class label of each item, so I can not perform classification and clustering might be a feasible solution.

> Therefore, in this project I try to cluster these 40 malwares into 4 groups. 

### What I did in this project... 
1. I extract some useful information from PE file by writing parsers. 
2. Next, I do data preprocessing by one hot encoding, two-grams one hot and label encoding to make data more useful, and do PCA to reduce dimension. 
3. To cluster data, I use k-means to cluster malwares into 4 malware families.

I use these information as features to cluster.

Section | Value | 
----------|:-----:|
FILE_HEADER | TimeDateStamp |
FILE_HEADER |  NumberOfSections |
PE Sections | MD5 |
PE Sections         | Flags |
PE Sections         | SizeOfRawData |
PE Sections         | Misc |
PE Sections         | Name |
OPTIONAL_HEADER | CheckSum |
