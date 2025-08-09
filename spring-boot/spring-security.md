# Spring Security

<details>
<summary>BASIC</summary>
  
1. What is security? how do define in the system ?
- It the process of securing the application by provinding access to valid users
- It can be done via authentication followed by authorization

2. Authentication vs Authorization?
- Authentication is the mechanism via which user will access the system using credentials
- Authorization is the process of accessing the resources based on permissions

3. How to control access to api based on role?
- Role based authorization

</details>

<details>
<summary>JWT TOKEN</summary>

1. Explain what is token? how it is segregated?
- Token is another way of authenticating into the system
- It has 3 parts
  - Header: Metadata
  - Body: It contains user information
  - Signature: Inbuilt

2. How to do you refresh the token if the token is expired making sure it we dont pass credentials?
- using refresh token generated along with token 

</details>
<details>
<summary>GATEWAY</summary>

1. How many instances of gateway is required?
- more than one. Ideally 3

2. How to do you whitelist or blacklist an ipaddress?
- in gateway configuration

</details>
