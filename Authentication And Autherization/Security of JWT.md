Yes, JWT tokens can be stolen from the local browser. This is because JWT tokens are typically stored in the browser's local storage or cookies. If a malicious actor can gain access to the browser's local storage or cookies, they can steal the JWT token and use it to impersonate the user.

Fiddler SSL is a tool that can be used to intercept and inspect HTTP traffic. This means that a malicious actor could use Fiddler SSL to intercept the JWT token as it is being transmitted between the client and the server.

There are a number of things that can be done to secure JWT tokens on the client side:

- Use secure cookies or local storage. Secure cookies and local storage are encrypted, which makes it more difficult for malicious actors to steal them.
- Use a JWT token signing algorithm that is resistant to tampering. The HMAC algorithm is a good choice for signing JWT tokens.
- Use a JWT token expiration time. This will prevent the token from being used after it has expired.
- Implement anti-CSRF measures. CSRF (Cross-Site Request Forgery) is a type of attack that can be used to steal JWT tokens. Anti-CSRF measures can help to protect against CSRF attacks.

By following these best practices, you can help to secure JWT tokens on the client side.

Here are some additional tips for securing JWT tokens:

- Only send the token over HTTPS.
- Use a short expiration time for the token.
- Don't store the token in the URL.
- Use a secure hashing algorithm to sign the token.
- Implement a refresh token system.