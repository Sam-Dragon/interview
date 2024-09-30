# Questions

1. Components of kafka <br>
A. producer, consumer, broker, message/event

2. What is kafka broker <br>
A. It can be physical computer or virtual machine which runs kafka processes. <br> 
  &nbsp;&nbsp;&nbsp; - Server which accepts events from producer & stores in its hard disk <br> 
  &nbsp;&nbsp;&nbsp; - It manages Kafka topics, handles the storage of data into topic partitions, manages replication of data for fault tolerance, and serves client requests (from both Producers and Consumers).

3. How kafka ensure data durability ? <br>
A. Replication mechanism give high availability & durability

4. Lets say broker of kafka goes down, what do you think will happen ? <br>
A. If we have single broker, requests wont be processed <br>
&nbsp;&nbsp;&nbsp;  If we have multiple broker, re-assignment will happen by electing another broker as leader 

6. Can we stop kafka server ? If yes, what can be the disadvantages ? <br>
A. Yes, we can stop kafka server gracefully using scripts but before that we must stop producers & consumer.<br> set property [controlled.shutdown.enable=true] <br>
&nbsp;&nbsp;&nbsp; If abruptly terminated, we may lose messages and get some error messages as well 
