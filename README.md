# ROSMERY SECURITY

This is an example of security using Identity and IdentityServer together.

## Migrations
Migration files already exists so you need to execute only the update commands on the ApiCore project

1. Open the Command Prompt and execute the following commands:

 - dotnet ef database update --context SecurityDbContext
 - dotnet ef database update --context PersistedGrantDbContext
 - dotnet ef database update --context ConfigurationDbContext

## Run the App
Steps to execute the example:
1. Create an User (http://localhost:5001/api/account/register)
2. Login with the created User (http://localhost:5001/api/account/login)
3. Copy the token and set the Authorization header with the token in a new request
(Headers: [{ "Authorization": "Bearer [put_token_here]"}])
4. Try to access to get your UserInfo (http://localhost:5001/identity)
5. Try to create new endpoint so you can test the entire features.
