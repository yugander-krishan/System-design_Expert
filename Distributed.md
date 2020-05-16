- In master-slave to decrease the probability of master crashing the master node can have more expensive hardware like a RAID
-  if high availability is a concern, a peer-to-peer network might be the best solution. If you can manage your big data using batch jobs that run in off hours, then the simpler master-slave model might be best. Referenced from [here](https://sungsoo.github.io/2014/06/07/choosing-distribution-models-mater-slave-versus-peer-to-peer.html)

- Master-slave or peer-to-peer has no effect on the distributed or non-distributed databases. These both are techniques which can be used in distributed databases. For example Mongo db is a nosql(document based) db employing single master-slave architecture whereas cassandra employs peer-to-peer architecture. Read [this](https://hackernoon.com/fundamentals-of-system-design-part-4-d6a62f3fa779) article for more details

- Mongo db vs Cassandra read [this](https://stackoverflow.com/q/47970547/6407858)
