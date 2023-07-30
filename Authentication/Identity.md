Install EF
Add authentication to Program.cs
Create and Implement Register page
Create and Implement Login page
Change Navigation Menu in Layout
Add Authorization in Home and Privacy Page
Create and Implement Logout


Create and Implement Register page
<div class="container mt-5">
	<div class="row justify-content-center align-items=-enter">
		<div class="col-sm-12 col-md-12 col-lg-4">
			<h1 class="mb-3">Register</h1>

			<form method="post">
				<div asp-validation-summery="All" class="text-danger"></div>
				<div class="mb-3">
					<label></label>
					<input>
					<span>
				</div>
			</form>
		</div>
	</div>
</div>


Active Azure Directory For Managing users

Autherisation
Program.cs

void AddAuthorizationPolicies(IServiceCollection service){
	service.AddAutherisation(options=>
	{
		options.AddPolicy("SalesPerson", policy=>policy.RequireClaim("EmployeeNumber"));
	})
}