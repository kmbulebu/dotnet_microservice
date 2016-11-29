# Overview
This is a sample REST api microservice written in C# using the .NET Core Framework. It tries its
best to adhere to the principles of the 12 factor app.

# Related

* [.NET Core](https://www.microsoft.com/net/core)
* [ASP.NET Core](https://docs.microsoft.com/en-us/aspnet/core/)
* [EntityFramework Core](https://docs.microsoft.com/en-us/ef/)
* [ASP.NET Configuration](https://github.com/aspnet/Configuration)
* [12 Factor App](https://12factor.net/)

# Files

## project.json
Project configuration and dependency management.

## project.lock.json
Dependencies as they were resolved during last `dotnet restore` execution.

## appsettings.json
Configuration defaults used by our application. Can be amended or replaced with configuration passed via environment variables.

## Dockerfile
Docker build file. Line by line instructions to building a docker image for this application.

## docker-compose.yml
Docker Compose orchestration. Runs this application's docker image with configuration 
and a database.

## Program.cs
Main entry point. Starts up web server with Startup.cs callbacks.

## Startup.cs
Application lifecycle callbacks. Reads configuration files and performs database migration.

## Migrations/
Classes generated by `dotnet ef migrations add`. At least one is provided to create the
database schema. More may be added with time to update the schema of a live system.

## Controllers/WidgetsController.cs
Web MVC controller for our REST api. Maps REST API urls to .NET class methods.

## Data/WidgetsContext.cs
Provides accessor methods to assign Entity classes to a database.

## Entity/Widget.cs
Our 'Widget' identity. Maps to a single relational database table. Simple fields are mapped
to database columns. 

## obj/
Intermediate compiled objects.

## bin/
Compiled, published, and packaged output from `dotnet build`, `dotnet publish`, or `dotnet pack`.

## .vscode/
If using Visual Studio Code, these files customize the IDE experience for this project.

# Useful Commands

## Download dependencies
`dotnet restore`

## Compile the application
`dotnet build`

## Run app only
`dotnet run`

## Package
`dotnet publish`

## Run app and database
`docker-compose up --build --force-recreate`

## Build docker image
`docker build .`

## Remove database migration files
`dotnet ef migrations remove -f`

## Create new migration
`dotnet ef migrations add name_of_migration`