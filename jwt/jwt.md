# JWT [Json Web Tokens]

- It is json object which securely transmits information over the web <br>
- It can be used for authentication & information exchange <br>

> Advantages
- To prevent user from constantly authenticating multiple times with senstive credentials
- It helps in managing sessions as well 

> Design
- It contains 3 sections <br>
  - header: it contains metadata information & encoded in BASE64 format <br> 
    i.e type - type of header [jwt] <br>
        alg - algorithm used [HS256 and RS256 ]. If alg is missing, then token is unsecured
        
  - payload: It contains user infromation<br>
  - signature: <br>
