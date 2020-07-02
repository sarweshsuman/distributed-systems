# Spark

## Notes From Paper: Resilient Distributed Datasets: A Fault-Tolerant Abstraction for In-Memory Cluster Computing(2012)

* RDD is Resilient Distributed Datasets.
* Provide Restricted Form of Shared Memory. But share memory with whom? multiple processes(executors) that work on this RDD at the same time.
* RDD provide coarse grained transformations rather than fine grained. Means you apply transformations on whole RDD instead of updating just one record in the RDD.
* In-memory computation
* Most suitable for iterative algorithms (batch analytics, machine learning) or interactive data mining.
* How do you reuse data between two different computations in MR, is by writing to external stable storage system and then next MR job reads it from external storage system. This incurs disk I/O overhead, replication overhead(in HDFS), serialization overhead (eventually written as binary).
