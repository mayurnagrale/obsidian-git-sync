namespace Indentity_Auth.Data
{
    public class AuthDbContext : DbContext
    {
        public AuthDbContext(DbContextOptions options) : base(options)
        { }
        public DbSet<User> Users { get; set; }
    }
}

Middleware
builder.Services.AddDbContext<AuthDbContext>(Options =>
    Options.UseSqlServer(builder.Configuration.GetConnectionString("AuthConnectionString")));

Connection String
"ConnectionStrings": {
    "AuthConnectionString": "Data Source=LAPTOP-T42EBUN6;Initial Catalog=AuthDb;Integrated Security=True;TrustServerCertificate=True;"
  }