# Databases Indexes

- Databases indexes are an abstraction over databases which provide higher read-throughput.
- We cannot index every column as that would mean slow writes as lot of computations will be required
- There are two different types of indexes:
  - Indexes in relational dbs uses B trees.
  - Non-relational dbs like Cassandra, Hbase, elastic search etc. uses a different indexing technique technique - Log Structured Merge Trees. Writes in 
    - The data is first stored in in-memeory balanced sorted trees like AVL, Red-Black trees. This is known as memtable. 
    - Once memtable is full data is flushed to disc/permanant storage into structure SSTables. SSTables are key-value data structures where value is sorted balanced tree(AVL or Red-Black)
    - Now there can be multiple SSTables in permanant storage and they are combined together by a process known as Compaction.
    - Merging multiple SSTables is easier as they all are sorted thereofre merge sort helps.
    - This is very good when write-throughput is higher as data is just added to the in-memeory data structure but not good for reads as for reads there can be multiple SSTables which all needs to be read for the required data using bloom filters.
    
    
Traditional indexing B Trees vs Log Structured Merge Trees:
- Reads:
  - Traditional indexing B trees are fatser inm reads as data is present at a speciifc location only. Also B trees are sorted balanced trees like AVL or Red-Black trees
  - Log Structured Merge Trees are slower for reads as data if not presnt in memtables needed to be searched in all the SStables of a partition whcih may make reads a bit slowere but still fatser compared to manhy others as it makes use of **Bloom-filters**
  
- Writes:
  - Traditional indexing B trees are slower in writes as they need to **seek** the specific key where the data needs to be stored. Also we know seek on discs is slower in nature. Along with that B trees stores data in WAL(write-ahead logs) which also slows down the writes
  - Log Structured Merge Trees indexing scheme is faster as data is appenden in memeory and also appended to **commit log** on disc. As we know appending is very fast.
  
- Performance:
  - Write-performance is better in no-sql but the write scheme may affect read-throughput if number of writes is very high which may mean lot of sstables
  - Read-performance is better in tarditional indexing as the key is at a specidic place
 
- Choice:
  - If ACID is your concern then raditional indexing is better as in case of Log Structured Merge tree(LSMT) as in LSMT there can be multiple keys in various differrent SSTAbles.
  
  
  
 References: https://medium.com/hackernoon/fundamentals-of-system-design-part-3-8da61773a631
