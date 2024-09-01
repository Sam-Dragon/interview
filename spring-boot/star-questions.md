# Star Questions

1. How to prevent DDOS attacks using spring boot? </br>
   https://danielangel22.medium.com/fighting-ddos-attacks-implementing-custom-rate-limiting-in-your-api-with-spring-boot-1a038b8124e7

2. How to prevent XSS attacks using spring boot? </br>
   https://danielangel22.medium.com/preventing-xss-attacks-in-your-spring-boot-api-c266a175e011   

3. Additional security to which can be provided to system on login page ? [Question focus on system attacks] <br>
A. DOS attack which can be solved using resiliency. Basically it counts the number of hits from particular api and block if required once threshould is reached

4. How is serilization working in spring boot ? <br>
A. Spring boot normally uses JSON library Jackson to serialize and deserialize the objects

5. Default dataSource connection pool ? <br>
A. Hikari connection pool with pool size of 10

6. If we configure two urls with different path param. what will happen ? 
i.e endpoints -> '/employee/{id}' & '/employee/{name}' <br>
A. Application wont start as these are conflicting url's

7. Spring bean scopes ? Explaing 'Request' & 'Session' with example <br>
A. singleton, prototype, request, session & global-session[Deprecated] <br>
Example: Try in editor

8. 
