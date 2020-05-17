- Used for uniform distribution of load

- Enables easy addition and removal of servers

- Removes the possibility of hotspots


Consistent hashing uses ring-like structure and has the complete key space mapped to it. Now using a hash function h1 the servers are mapped to the ring.
Now once the requests come then using the same hash function h1 the requests are mapped to the ring and they are ahndled by the closest server in clockwise-manner
This way the addition and removal of servers is handled

In order to remove the hotspots so that there is a uniform distribution we just use virtual servers. What it means that same servers are mapped to the ring using many different hash-functions and then using this we can just remove the chances of hotspot and also ensures uniform distribution of the keys.

Applications:
- Elastically adding/removing database servers
- Elastically adding/removing cache servers


References: https://www.acodersjourney.com/system-design-interview-consistent-hashing/
