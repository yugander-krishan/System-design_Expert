- One of the most important thing for scalability is replication
  - Others reasons include:
    - You want to keep data geographically close to users
    - Balance read/write across multiple machines to prevent throttling of a single database server
    - Build redundancies within your system
- Replication means making your data redundant using multile machines which can lead to high-availability also
- one of the most imortant thing to consider is **replication lag**

- There are various replication configurations:
  - Master-slave
  - Multi-master
  - No master/ peer to peer
  
- Master-slave: 
  - we have one master machine and many slaves. The writes can go to master and reads can go to master as well as slaves.
  - writes Can be synchronous as well as asynchronous
  - with synchronous writes a master write and pass the data to slaves and wait for acknowledgement. But it can cause problems if connectivity to one node is affected due to low-internet or netwrok partition
  - Async writes are very fast. But then the issue with the replication lag. So after write if read goes to the salve where data is not yet replicated will cause problems. In order to solve this problem you can send read requests initially to master node.
  - Async writes have one more problem that is if one read-request goes to one slave where data has been replicated but if second request goes to other slave where data is still not replicated so in order to solve this problem send request from same client to same slave initially.
  
- Multi-master:
  - Pros:
    - It leads to better durability as well as availability. As if one master goes down then second amster is stiil there
  - Cons:
    - Problem with concurrent writes(same time multiple inserts, updates, deletes)
    
- Peer to peer / no master:
  - It can cause problem with respect to both read and writes as writes can read both have concurrency issues
  

References: https://medium.com/hackernoon/fundamentals-of-system-design-part-4-d6a62f3fa779
