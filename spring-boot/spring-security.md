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
<summary>JWT TOKEN</summary>

1. Explain what is token? how it is segregated ? <br>
A. Token is another way of authenticating into the system
- It has 3 parts
  - Header: Metadata
  - Body: It contains user information
  - Signature: Inbuilt

2. How to do you refresh the token if the token is expired making sure it we dont pass credentials ? <br>
A. Using refresh token generated along with token 

</details>
<details>
<summary>GATEWAY</summary>

1. How many instances of gateway is required ? <br>
A. more than one. Ideally 3

2. How to do you whitelist or blacklist an ipaddress ? <br>
A. in gateway configuration

</details>
