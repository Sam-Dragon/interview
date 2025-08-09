# Spring Security

<details>
<summary>BASIC</summary>
  
1. What is security? how do define in the system ? <br>
A. It the process of securing the application by provinding access to valid users. <br>
   It can be done via authentication followed by authorization

2. Authentication vs Authorization ? <br>
A. Authentication is the mechanism via which user will access the system using credentials <br>
   Authorization is the process of accessing the resources based on permissions

3. How to control access to api based on role ? <br>
A. Role based authorization [RBAC]

</details>
<details>
<summary>ATTACKS</summary>

1. Tell me something about DOS attack ? When does it effect the system ? How to prevent ? <br>
A. DOS [Deniel Of Service], this attack comprises of flood of requests sent to server effecting system performance even system crashes
<br> **Solution**: It can be prevented by 'Rate limiters & throttlers'

2. Tell me something about Man in Middle Attack > How to prevent ? <br>
A. MIM [Man In Middle], this attack comprises of insecure way of data transmission which can lead to other problems like Impersonation, Data alteration etc. 
<br> **Solution**: It can be prevented by 'HTTPS' protocol

3. Tell me something about SQL Injection Attack > How to prevent ? <br>
A. SQL Injection, this attack comprises of scripts to execute funtion on server which can lead to server crash or unauthorized access. 
<br> **Solution**: It can be prevented by 'validation' of data formats

4. Tell me something about Authentication issues > what are better approaches ? <br>
A. Authentication, it is a way to access the system
<br> **Solution**: It can be addressed using JWT [Java Web Tokens], Short-lived tokens etc..

5. Tell me something about Authorization issues > what are better approaches ? <br>
A. Authorization, it is a way to access the resources of the system
<br> **Solution**: It can be addressed using OAUTH, RBAC etc..

</details>
<details>
<summary>JWT TOKEN</summary>

1. Explain what is token? how it is segregated ? <br>
A. Token is another way of authenticating into the system
* It has 3 parts
  - Header: Metadata
  - Body: It contains user information
  - Signature: Inbuilt

2. How to do you refresh the token if the token is expired making sure it we dont pass credentials ? <br>
A. Using refresh token generated along with token

3. How to communicate to other services securily ? <br>
A. We can use static API token, JWT Propagation, TLS certificates, kubernetes interally

4. How to communicate to external services securily ? <br>
A. We can use Basic Auth, Sessions, Token Based Authentication [JWT or OAuth2 bearer tokens], api keys

</details>
<details>
<summary>GATEWAY</summary>

1. How many instances of gateway is required ? <br>
A. more than one. Ideally 3

2. How to do you whitelist or blacklist an ipaddress ? <br>
A. in gateway configuration, using global filters or gateway filters

3. How to do you limit the number of requests from client ? <br>
A. in gateway configuration, using rate limiter config

</details>
