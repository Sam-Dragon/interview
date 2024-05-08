# Questions

1. components of kafka <br>
A. producer, consumer, broker, message/event

2. what is kafka broker <br>
A. It can be physical computer or virtual machine which runs kafka processes. <br> 
  &nbsp;&nbsp;&nbsp; - Server which accepts events from producer & stores in its hard disk <br> 
  &nbsp;&nbsp;&nbsp; - It manages Kafka topics, handles the storage of data into topic partitions, <br>
  &nbsp;&nbsp;&nbsp;&nbsp;   manages replication of data for fault tolerance, and serves client requests (from both Producers and Consumers).

3. can we stop kafka server ? If yes, what can be the disadvantages ? <br>
A. Yes, we can stop kafka server gracefull using scripts. It abruptly terminated, we may lose messages and get some error messages as well 
