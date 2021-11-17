## EC2 INSTANCE TYPES - OVERVIEW

- AWS have 7 different types (General Purpose, Compute Optimized, Memory Optimized, Accelerated Computing, Storage Optimized, Instance Features, Measuring Instance Performance)
- For each type of instance we have different families
- Naming convention:

<p align="center">
  <img src="/Journey/10202/ec2.PNG" width="300" height="140"></p>

### GENERAL PURPOSE:
(Mac, T4g, T3, T3a, T2, M6g, M5, M5a, M5n, M4, A1, ...)
- Great for a diversity of workloads such as web servers or code repositories
- With a good balance between Compute - Memory - Networking

### COMPUTE OPTIMIZED:
(C6g, C6gn, C5, C5a, C5n, C4)    C: COMPUTE <br/>
Great for compute-intensive task that require high performance processors 
- Batch processing workloads
- Media transcoding
- High performance web servers
- High performance computing (HPC)
- Scientific modeling & machine learning
- Dedicated gaming servers)

### MEMORY OPTIMIZED
(R6g, R5, R5a, R5b, R5n, R4, X1e, X1, HighMemory, z1d)    R: RAM
Fast performance for workloads that process large data sets in memory
- High performance, relational/non relational databases
- Distributed web scale cache stores
- In memory databases optimized for BI
- Applications performing real-time processing of big unstructured data 

### STORAGE OPTIMIZED
(l3, l3en, D2, D3, D3en, H1)
Great for storage-intensive tasks that require high, sequential read and write access to large data sets on local storage
- High frequency online transaction processing (OLTP) systems
- Relational & NoSQL databases
- Cache for in-memory databases (for example, REDIS)
- Data warehousing applications
- Distributed file systems
