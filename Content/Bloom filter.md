- **Probabilistic** data structure
- It can tell if item is eiher 
  - may be presnt
  - definitely not preseny
  
- It is very useful to know if an item not present for sure which saves a lot of time as it can have applications:
  - Know if an email id already exists
  - list of malicious urls
  
- In above examples we don't want a definite answer. Just a probabilistic answer is enough. It may lead to false-positives(giving a true when it should have returned false)

Application:
- Cassandra: reads from sstables. saves a lot of time
- Content recommendation system

Advantages of Bloom Filters:
- Space efficient
- Saves expensive scanning time


References: https://medium.com/datadriveninvestor/bloom-filter-a-simple-but-interesting-data-structure-37fd53b11606
