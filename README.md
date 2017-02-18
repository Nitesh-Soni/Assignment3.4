1. Explain the importance of Namenode in Hadoop cluster

The NameNode is the centerpiece of an HDFS file system. It keeps the directory of all the files in the file system, and tracks where across the cluster the file data is kept. It does not store the data of these files itself.
Client applications talk to the namenode whenever they wish to locate a file, or when they want to add, copy, delete, move a file. The NameNode responds the successful requests by returning  a list of relevant DataNode servers where the data lives.
The NameNode is a single point of failure HDFS Cluster. HDFS is not currently a High Availability system. When the NameNode goes down, the file system goes offline. There is an optional SecondaryNameNode that can be hosted on a separate machine. It only creates checkpoints of the namespace by merging the edits file into the fsimage file and does not provide any real redundancy. 
