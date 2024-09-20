# Star Questions

# Kafka
1. If i have to take down applications, whether kafka server also will go down or do we need to terminate ? <br>
A. No, kafka server needs to be explicily stopped that to gracefully, failing to do so we may see older pods will continue to consume new messages and we may lose that data  

2. Which partitions will messages goes if the replica set is 3 ? <br>
A. It will depend on the messages u send. <br>
  &nbsp;&nbsp;&nbsp; - If the message is has plain text, it will go to any of the partition & we may lose updates <br>
  &nbsp;&nbsp;&nbsp; - If the message is provided in form key-value pair, it will go to specific partition ensuring updates are sequencial  

3. Can to maintain order in kafka messages ? If yes, How ? <br>
A. By producing message on same key [Ex: Account credit/debit based on account no] 

4. Can kafka send synchronous request. Basically it is only used asynchronously ? <br>
A. Yes. by using completable future method of 'completableFuture.join()' or  using directly reading sendResult.get(Timeout)

