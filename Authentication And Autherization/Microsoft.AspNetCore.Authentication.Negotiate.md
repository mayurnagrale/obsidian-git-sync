This package is useful for windows domain user , it follows Negotiate, Kerberos or NTML protocols to authenticate requests.

When a user attempts to access your application, the authentication middleware will send a challenge to the user's browser. The user's browser will then send the user's credentials to the server. The server will use the Negotiate authentication handler to authenticate the user and either grant or deny access to the application.

Middleware 

services.AddAuthentication(NegotiateDefaults.AuthenticationScheme)
    .AddNegotiate();
