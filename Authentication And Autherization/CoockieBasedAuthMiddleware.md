using Microsoft.AspNetCore.Authentication.Cookies

builder.Service.AddAuthentication(
	CookieAuthenticationDefault.AuthenticationScheme).AddCookie(
	option=>{ option.LoginPath = "/Access/Login";
	option.ExpireTimeSpam = TimeSpam.FromMinutes(20);
	}
);

app.useAuthenticaiton();