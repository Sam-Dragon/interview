# Questions

1. components of kafka
- producer, consumer, broker

2. what is kafka broker
- It can be physical computer or virtual machine which runs kafka processes.
- Server which accepts events from producer & stores in its hard disk
- It manages Kafka topics, handles the storage of data into topic partitions, 
  manages replication of data for fault tolerance, and serves client requests (from both Producers and Consumers).

3. can we stop kafka server ? If yes, what can be the disadvantages ?
- Yes, we can stop kafka server gracefull using scripts
- It abruptly terminated, we may lose messages and get some error messages as well 

4. 

# Star Questions
1. If i have to take down applications, whether kafka server also will go down or do we need to terminate ?
- No, kafka server needs to be explicily stopped that to gracefully, failing to do so we may see older pods will continue to consume new messages and we may lose that data  

2. which partitions will messages goes if the replica set is 3
- It will depend on the messages u send.
  - If the message is has plain text, it will go across the partitions & we may lose updates
  - If the message is provided in form ket-value pair, it will go to specific partition ensuring updates are sequencial  

3. How to maintain order in kafka messages ?
- By producing message on same key [Ex: Account credit/debit based on account no] 

4. Can kafka send synchronous request ?
- Yes 

5. 
