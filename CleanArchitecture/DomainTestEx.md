private const string ApplicationNamespace ="Application";
private const string InfrastructureNamespace ="Infrastructure";
private const string PresentationNamespace ="Presentation";
private const string WebNamespace ="Web";

[Fact]
public void domain_should_not_have_dependency_on_other_projects(){
	//Arrange
	
	var assembly = typeof(Domain.AssemblyReference).Assembly;

	var otherprojects = new []{
		ApplicationNamespace,
		InfrastructureNamespace,
		PresentationNamespace,
		WebNamespace
	};
	//Act
	
	var TestResult = Types
	.InAssembly(assembly)
	.ShouldNot()
	.HaveDependancyOnAll(otherprojects)
	.GetResult
	
	//Assert
	

	TestResult.IsSuccessful.Should().BeTrue();
}

//Similarly we can add tests for other projects as well

[Fact]
public void Application_should_not_have_dependency_on_other_projects(){
	//Arrange
	
	var assembly = typeof(Application.AssemblyReference).Assembly;

	var otherprojects = new []{
		InfrastructureNamespace,
		PresentationNamespace,
		WebNamespace
	};
	//Act
	
	var TestResult = Types
	.InAssembly(assembly)
	.ShouldNot()
	.HaveDependancyOnAll(otherprojects)
	.GetResult
	
	//Assert
	

	TestResult.IsSuccessful.Should().BeTrue();
}


[Fact]
public void Application_should_not_have_dependency_on_other_projects(){
	//Arrange
	
	var assembly = typeof(Application.AssemblyReference).Assembly;

	var otherprojects = new []{
		InfrastructureNamespace,
		PresentationNamespace,
		WebNamespace
	};
	//Act
	
	var TestResult = Types
	.InAssembly(assembly)
	.ShouldNot()
	.HaveDependancyOnAll(otherprojects)
	.GetResult
	
	//Assert
	

	TestResult.IsSuccessful.Should().BeTrue();
}

[Fact]
public void Infrastructure_should_not_have_dependency_on_other_projects(){
	//Arrange
	
	var assembly = typeof(Infrastructure.AssemblyReference).Assembly;

	var otherprojects = new []{
		PresentationNamespace,
		WebNamespace
	};
	//Act
	
	var TestResult = Types
	.InAssembly(assembly)
	.ShouldNot()
	.HaveDependancyOnAll(otherprojects)
	.GetResult
	
	//Assert
	

	TestResult.IsSuccessful.Should().BeTrue();
}

[Fact]
public void Presentation_should_not_have_dependency_on_other_projects(){
	//Arrange
	
	var assembly = typeof(Presentation.AssemblyReference).Assembly;

	var otherprojects = new []{
		InfrastructureNamespace,
		WebNamespace
	};
	//Act
	
	var TestResult = Types
	.InAssembly(assembly)
	.ShouldNot()
	.HaveDependancyOnAll(otherprojects)
	.GetResult
	
	//Assert
	

	TestResult.IsSuccessful.Should().BeTrue();
}


[Fact]

public void Handlers_Should_Have_dependency_on_domain(){
	
}