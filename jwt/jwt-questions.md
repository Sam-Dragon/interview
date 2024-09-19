JWT

1. Why JWT tokens ? Advantages ? <br>
A. Json Web tokens are internet standard to exchange data securily between two parties<br>
   Advantages: Simplies authentication mechanism <br>

2. Can i create unsecured token ? If yes, how ? <br>
A. Yes. If we keep algo tag header section to 'None' <br>

3. Can we temper the token ? <br>
A. No, hashing algo uses a secret key mentioned by developer<br>

4. What would you do if the user token is expired? <br>
A. We need to use refresh token & regenerate new token <br>

5. Is is good to use long live tokens ? <br>
A. No, it is not recommended as it results in security threat <br>

6. If we have api to be exposed to third party, we can secure by tokens. what alterantive do we have ? <br>
A. In such cases, we can do couple of things <br>
   - Allow specific ip's to access the api [Not recommended]
   - Having agreement between the systems using certificates [public-private key certs]
   
7. Can we revoke the token or blacklist it? <br>
A. Yes, but generally not a good practice
