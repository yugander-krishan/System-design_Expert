How the startegies mentioned for dealing with concurrent writes work. Taken from [here](https://medium.com/hackernoon/fundamentals-of-system-design-part-4-d6a62f3fa779):

   - Make the most recent write win
   - Write custom code on detecting conflicts in replication logs
   - Present the user with a list of values, and let the user decide the merge and discard strategy in case of a conflict
