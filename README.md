# Microservices-NetCore-Dapper-SQLServer
Microservices communication developed with .Net Core and database connection with Dapper and SQL Server.

## Technologies:

- .Net Core 2.2
- JWT Authorization
- Dapper
- SQL Server
- Swagger
- FluentValidation
- AutoMapper

## To run this project

- Run the script located at "/Docs/script.sql" to create a SQL Server database. 
- In this project, the connection string is set in the APITestRegister's appsettings.json as it follows:
  `Server=localhost;Database=TestDB;Trusted_Connection=True;`

- Set the Issuer, Audience and Secret of your JWT inside the appsettings.json of both solutions:

![appsettings.json](/Docs/appsettings.json.PNG)

- The APITestRegister's URL must be informed in the APITestGateway's appsettings.json:

![routes](/Docs/routes.PNG)

- APITestGateway's swagger:

![swagger-0](/Docs/swagger-0.PNG)

- To access the APITestRegister's methods is necessary to pass through the APITestGateway, but firstly an authorization token must be created:

![swagger-1](/Docs/swagger-1.PNG)

- The parameter "route" must have the pattern "Controller_Method". For example: the route "user_login" will access the "Login" method in the "UserController" of the APITestRegister.
- The parameters sent in the request must be the same as the ones the APITestRegister expects to receive.

![swagger-2](/Docs/swagger-2.PNG)

- APITestRegister's swagger:

![swagger-3](/Docs/swagger-3.PNG)
