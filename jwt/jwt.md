# JWT [Json Web Tokens]

> JWT
- It is json object which securely transmits information over the web
- It can be used for authentication & information exchange 
- Meant for stateless sessions
- It must be sent over the **header**, not recommended to send over url or body
  
> Advantages
- Requires only one time authentication. rest will be taken care by tokens

> Good Scenarios
- Used for accessing api securely & will be helpful for creating sessions

> Bad Scenarios 
- Dont use them in cookies
- Not suitable for session management
- Dont use long live tokens
- Prevent putting informations such as permissions or application data in header

> Design
- It contains 3 sections separated by dots(.)
  - header: it contains metadata information & encoded in BASE64 format <br>
    i.e type - type of header [jwt] <br>
        alg - algorithm used [HS256 and RS256 ]. If alg is missing, then token is unsecured 
        
  - payload: It contains user infromation & token related info. Dont put **sensative information**
    i.e sub: subject of the token <br>
        exp: token expiry time <br>
        iat: issued at <br>
     
  - signature: This checks authenticity of the token. It specify hashing algorithm with your **secret key**. It combines header & payload with base64 encoding along with hash algorithm <br>
      i.e  HASHINGALGO( base64UrlEncode(header) + “.” + base64UrlEncode(payload),secret)
    

Example: Put this in "https://jwt.io/" <br>
Token: eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkpvaG4gRG9lIiwiaWF0IjoxNTE2MjM5MDIyfQ.SflKxwRJSMeKKF2QT4fwpMeJf36POk6yJV_adQssw5c <br>

# Best Practices
- Use short-lived tokens
- Use refresh tokens to regeneration rather than user sensetive information
