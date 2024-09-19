1. Can i create unsecured token ? If yes, how ? <br>
A. Yes. If we keep algo tag header section to 'None' <br>

2. What would you do if the user token is expired> How do you regenerate? <br>
A. We need to use refresh token & regenerate new token <br>

3. If we have api to be exposed to third party, we can secure by tokens. what alterantive do we have ? <br>
A. In such cases, we can do couple of things <br>
   - Allow specific ip's to access the api [Not recommended]
   - Having agreement between the systems using certificates [public-private key certs]

4. Can we revoke the token or blacklist it ?
A. Yes, but generally not a good practice
