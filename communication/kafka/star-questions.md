# Star Questions

# Kafka

#. Is kafka suitable for all scenarios ? If not, what is the alternate ?
 - It is not suitable in case where we just need P2P communication or single request-response model.
 - If it is UI driven, we will cache to store the data
 - If it is backend driven, we will use utilties like resttemplate, finclient etc..

#. Explain the difference between queue & kafka ? <br>
 - Order: Queue maintains FIFO order but kafka cannot as it is distributed in nature
 - Storage: Queue deletes the messages once consumed by all consumers whereas kafka storage is configurable due to advance storage systems & retention policies
 - Size: Queue has default size of 64KB whereas kafka has 1MB
 - Complexity: Queue is easy to learn and implement whereas kafka is very complex in nature
    
#. If i have to take down applications, whether kafka server also will go down or do we need to terminate ? <br>
 - No, kafka server needs to be explicily stopped that to gracefully, failing to do so we may see older pods will continue to consume new messages and we may lose that data 

#. Which partitions will messages goes if the replica set is 3 ? <br>
 - It will depend on the messages u send. <br>
    &nbsp;&nbsp;&nbsp; - If the message is has plain text, it will go to any of the partition & we may lose updates <br>
    &nbsp;&nbsp;&nbsp; - If the message is provided in form key-value pair, it will go to specific partition ensuring updates are sequencial

#. Can to maintain order in kafka messages ? If yes, How ? <br>
 - By producing message on same key [Ex: Account credit/debit based on account no] 

#. Can kafka send synchronous request. Basically it is only used asynchronously ? <br>
 - Yes. by using completable future method of 'completableFuture.join()' or  using directly reading sendResult.get(Timeout)

#. How would you decide number of partitions per topic? <br>
 - It can be equal to number of consumers or more than that & also replication factor also must be same

#. What is rule b/w partitions & consumers ?
 - Generally, the number of partitions must be equals to number of consumers
 - We can have more partitions against consumers
 - We cannot have more consumers than the partitions as the additional servers will sit idle

#. What happens if messages failed to be produced or consumed ? Where will you store & how will you retry ?
 - Ideally, error handler must be configured such that we can backup the failed record in topic called Dead Letter Topic[DLT]
 - Dead letter topic are designed for the purpose of storing the failed records, such that it can be reviewed and processed later

#. Let say due to workload traffic, i have scaled my application by increasing instances. How do you ensure duplicate messages are not consumed?
 - Consumer groups  

#. How to avoid duplicate messages in kafka? How would you achieve it
 - It can achieved by following ways
   - Make producer idempotent
   - Make consumer idempotent
   - Use Transactions

#. Can we read messages from certain point or data from topic? [**TRY THIS**] <br>
 - Yes, using partition & offset

#. where does kafka stores the messages ?
 - It is stored in logs [WAP]

#. Why cant we use databases to store kafka messages ?
 - As kafka process large set of records, we cannot store in databases as databases also has drawbacks
