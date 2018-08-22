# Rosmery Security API

﻿dotnet ef migrations add [name] --context [DbContextName]
dotnet ef database update --context [DbContextName]

For Identity 2.1:
	dotnet ef migrations add SecurityDatabase --context SecurityDbContext
	dotnet ef database update --context SecurityDbContext

For IdentityServer4:
	dotnet ef migrations add InitialIdentityServerPersistedGrantDbMigration -c PersistedGrantDbContext
	dotnet ef migrations add InitialIdentityServerConfigurationDbMigration -c ConfigurationDbContext

	dotnet ef database update --context PersistedGrantDbContext
	dotnet ef database update --context ConfigurationDbContext

Migration files already exists so you need to execute only the update commands:
    Identity:       dotnet ef database update --context SecurityDbContext
    IdentityServer: dotnet ef database update --context PersistedGrantDbContext
	                dotnet ef database update --context ConfigurationDbContext