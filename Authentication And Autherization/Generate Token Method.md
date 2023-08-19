using Microsoft.IdentityModel.Tokens;

public class JwtTokenGenerator
{
    public static string GenerateToken(string username, string password)
    {
        // Create a security token claims set.
        ClaimsIdentity claimsIdentity = new ClaimsIdentity(
            new Claim("username", username),
            new Claim("password", password)
        );

        // Create a security token handler.
        JwtSecurityTokenHandler jwtSecurityTokenHandler = new JwtSecurityTokenHandler();

        // Create a JWT token.
        JwtSecurityToken token = jwtSecurityTokenHandler.CreateToken(
            claimsIdentity,
            new JwtHeader(),
            new JwtClaimsSet(),
            new SigningCredentials(new SymmetricSecurityKey(Encoding.UTF8.GetBytes("secret")))
        );

        // Return the token.
        return token.EncodeToString();
    }
}

Steps: 
1. Install the Microsoft.IdentityModel.Tokens: https://www.nuget.org/packages/Microsoft.IdentityModel.Tokens NuGet package.
2. Create a JWT token by using the `JwtSecurityTokenHandler` class.
3. Send the token to the client.
4. The client can then use the token to authenticate with the server.
5. The server can verify the token by using the `JwtSecurityTokenHandler` class.


This code creates a JWT token with two claims: the username and the password. The token is then encoded and returned.

The client can then use this token to authenticate with the server. The server can verify the token by using the `JwtSecurityTokenHandler` class. Here is an example of how to verify a JWT token in C#:

using Microsoft.IdentityModel.Tokens;

public class JwtTokenValidator
{
    public static bool VerifyToken(string token)
    {
        // Create a security token handler.
        JwtSecurityTokenHandler jwtSecurityTokenHandler = new JwtSecurityTokenHandler();

        // Try to decode the token.
        try
        {
            JwtSecurityToken securityToken = jwtSecurityTokenHandler.ReadToken(token);

            // Verify the token.
            jwtSecurityTokenHandler.ValidateToken(securityToken, new TokenValidationParameters());

            // The token is valid.
            return true;
        }
        catch (SecurityTokenValidationException)
        {
            // The token is invalid.
            return false;
        }
    }
}
