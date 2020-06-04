
# Assignment 5 - Spark 

For this exercise, we'll use Spark on an AWS EC2 machine. 

### AWS Machine Specs 
The machine is a T2 Extra Large machine with fore cores and 16GB of RAM.

### Spark Setup
We'll use PySpark with two partitions. We are running four cores, and Spark with use these to run parallel jobs

### Objective
The objective of this exercise is to compare an Apache Spark distributed setup with my local computer and compare efficiency. We'll compare the PySpark model against our trusty Surprise Package. Let's once again use the [Beer Recommender](https://github.com/pburkard88/DS_BOS_06/tree/master/Data) data.

## Summary 
We could see that the Spark distributed computing model (12 seconds) outperformed the Surprise package (19 seconds) thanks to parallel processing. However, the gains are small, so we may disregard it even for a dataset for this size. We did not use a super massive dataset (1.5 million rows), so the incremental benefit of using Spark was not terribly visible. The biggest benefit came from using the AWS EC2 instance. Perhaps if we had a dataset with 15-20 million rows, distributed computing would have been more beneficial.
