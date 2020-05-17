# System-design_Expert

- When thinking on db's think about the type of schema you require. That will decide what kind of databases you can use like sql or no-sql. Then you can use master-slave or multi-master techniques on sql and nosqls like cassandra are KV and scalable and distributed or mongo db is document based.

- In databses for scaling master-slave architecture we can use sharding.

- When thinking about servers you want to use different concepts like distributed using consistent hashing or using sharded for handling different requests.

- System design doesn't mean distributed systems. Distributed systems is a type of system which comes into picture when we start scaling and thus bring multiple nodes into picture.

- Lean to estimate roughly about the servers, space, network bandwidth etc. Can refer [this](https://www.codementor.io/@robinpalotai/back-of-the-envelope-calculation-for-system-design-interviews-z4ljbsp5l)

- [Solve a system design](https://softwareengineering.stackexchange.com/a/384749/276844)
