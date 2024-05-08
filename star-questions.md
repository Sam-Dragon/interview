# Questions

# Spring Boot
1. How to prevent DDOS attacks using spring boot? </br>
   https://danielangel22.medium.com/fighting-ddos-attacks-implementing-custom-rate-limiting-in-your-api-with-spring-boot-1a038b8124e7

2. How to prevent XSS attacks using spring boot? </br>
   https://danielangel22.medium.com/preventing-xss-attacks-in-your-spring-boot-api-c266a175e011   

3. Additional security to which can be provided to system on login page ? [Question focus on system attacks] <br>
A. DOS attack which can be solved using resiliency. Basically it counts the number of hits from particular api and block if required once threshould is reached

4. How is serilization working in spring boot ? <br>
A. Spring boot normally uses JSON library Jackson to serialize and deserialize the objects

5. Default dataSource connection pool
A. Hikari connection pool with pool size of 10

6. If we configure two urls with different path param. what will happen ? <br>
i.e /employee/{id} & /employee/{name}
A. Application wont start as these are conflicting url's

# Web
1. How to solve the problem when request param contains '&' ? [& is delimeter for request params] <br>
A. Just encode it and send

# Java
1. Difference b/w Out Of Memory error raised by pemgen or by heap space [Variation in JDK versions]

2. Can we access variables/methods outside the package without making it as public ? <br>
A. Yes, using protected but condition is class must be inherited 

3. if all try / catch & finally throws exception, which exception message is printed to caller method ? [Assume exception message contains text as try for try block and so on.] <br>
A. It will show messages thrown from finally block

# Kafka
1. If i have to take down applications, whether kafka server also will go down or do we need to terminate ? <br>
A. No, kafka server needs to be explicily stopped that to gracefully, failing to do so we may see older pods will continue to consume new messages and we may lose that data  

2. Which partitions will messages goes if the replica set is 3 ? <br>
A. It will depend on the messages u send. <br>
  &nbsp;&nbsp;&nbsp; - If the message is has plain text, it will go to any of the partition & we may lose updates <br>
  &nbsp;&nbsp;&nbsp; - If the message is provided in form ket-value pair, it will go to specific partition ensuring updates are sequencial  

3. Can to maintain order in kafka messages ? If yes, How ? <br>
A. By producing message on same key [Ex: Account credit/debit based on account no] 

4. Can kafka send synchronous request. Basically it is only used asynchronously ? <br>
A. Yes. by using completable future method of 'completableFuture.join()' or  using directly reading sendResult.get(Timeout)

# Database
6. Why redis ? whats the advantage ?

