- In-memeory datastructures like array and linked list are optimised for access, whereas permanent data storage is optimised for read/write 
- permanent storage is dependent on data-modelling which is of two types:
  - Relational: When your schema is fixed, know joins required beforehand, relatioships exist, indexing is required, ACID is imp.
  - NoSQL: When you have queries and schema is not fixed and indexing is not that much of a concern and ACID(mainly isolation and atomicity) is also not rquired, lots of many-to-many relationships are there
    - Document, KV, Graph etc. are some of the NoSQL databases
    - To model many-to-many relationship in a graph like structure easier done using no-sql database. No need to know joins beforehand which if required would have made the queries very messy.
  
  
  Reference: https://hackernoon.com/fundamentals-of-system-design-part-2-abbe437ce2dd
  
