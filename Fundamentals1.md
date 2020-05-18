A good system design is concerned with 3 things:

- Realiability: 
  - It should be fault-tolerant. Hardware faults can be tolerated by redundancy. For example having discs in RAID configuration
  - Software faults require tolerance which can be achieved by understanding business requirements and then deciding what to so ifsomething unacceptable happnes or by monitoring so that we know of warnings beforehand or better unit-testing also helps or by designing better abstractions or interfaces in order to isolate the problems when and if they occur(spearation of concerns)

- Scalability:
  - Measure of how well system performs under load. Load here can refer to read & write requests
  - Performance can be thought of as the system’s operating characteristic when system’s load parameter is changed. Can be measured by for example average response time under different loads or peak reads/writes or how much memory, cpu cycles etc. are being used at avg or at peak or how many database read, writes etc. are being done.
  
- Maintainability: 
  - How easy to read and add new features to code. 
  - Used design principles or SOLID design principle for development
  
  
  
  
References:
https://hackernoon.com/fundamentals-of-system-design-part-1-c87b1d2bfd31
