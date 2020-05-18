- Partitioning/(sharding of databases) and replication helps in scaling and availability
- Using partitioning we can divide our databases and distributing it across many disks. Or we can use partitioning we can have particular server for secific requests
- Partitioning are good but may lead to **hot-spots**. For-example: on e-retail website we may have one node for food, other node for electronics and in case people are buying more elctronics it may cause problems.
- In order to solve this problem we can partition using hash and can allocate a hash-ranghe to the nodes. So that a data in a particular range will go to specific node. But in this case it may again lead to **hot-spots**
- In order to fix issue with hash we can again add random digits so that data on that specific node will be distributed again. It may lead to no hostpsot but reads will take more time as now data to be gathered from multiple nodes.

- Basically two strategies for partitioning(Read from url shortner):

  - Range based partition
  - Hash based partition
  - Both of the baove have issues specifically: addition/removal of servers, redistribution of data when a server is added/removed and hotspots
    - In order to fix this **Consistent HAshing is used**



References: https://medium.com/hackernoon/fundamentals-of-system-design-part-5-c27b617cd532
