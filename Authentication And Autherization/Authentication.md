Types of authentication in Asp.net mvc core
 - cookie-based authentication
 - token-based authentication
 - OAuth
 - OpenID Connect

Authentication Schemes:
 - A scheme represents a specific way of authenticating users, such as cookie-based authentication, JWT (JSON Web Tokens) authentication, etc.
 - You can use one or multiple authentication schemes in your application based on your requirements.
Authentication Middleware Execution:
Authentication Providers:
Authentication Controllers and Actions:
User Identity:
- After successful authentication, the middleware creates an instance of `ClaimsPrincipal` representing the authenticated user.
- This object contains information about the user, such as their claims, roles, and identity-related data.

User Authentication and Logout:
- `SignInAsync`
- `SignOutAsync`
using Microsoft.AspNetCore.Authentication.Cookies

builder.Service.AddAuthentication(
	CookieAuthenticationDefault.AuthenticationScheme).AddCookie(
	option=>{ option.LoginPath = "/Access/Login";
	option.ExpireTimeSpam = TimeSpam.FromMinutes(20);
	}
);

app.useAuthenticaiton();


