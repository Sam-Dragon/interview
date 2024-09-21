# Questions

1. components of kafka <br>
A. producer, consumer, broker, message/event

2. what is kafka broker <br>
A. It can be physical computer or virtual machine which runs kafka processes. <br> 
  &nbsp;&nbsp;&nbsp; - Server which accepts events from producer & stores in its hard disk <br> 
  &nbsp;&nbsp;&nbsp; - It manages Kafka topics, handles the storage of data into topic partitions, <br>
  &nbsp;&nbsp;&nbsp;&nbsp;   manages replication of data for fault tolerance, and serves client requests (from both Producers and Consumers).

3. Hou kafka ensure data durability ? 
A. Replication mechnism give high availability & durability

4. Lets say broker of kafka goes down, what do you think will happen ? <br>
A. If we have single broker, kafka will be down <br>
&nbsp; If we have multiple broker, re-assignment will happen by electing another broker as leader 

6. can we stop kafka server ? If yes, what can be the disadvantages ? <br>
A. Yes, we can stop kafka server gracefull using scripts. It abruptly terminated, we may lose messages and get some error messages as well 
