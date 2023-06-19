# Robusta fake

- Book management fake

- Note: migration method use for docker and container when build we can not use dotnet ef migrations add ..
- so we should use migration method
- second  use env variable ASPNETCORE_ENVIRONMENT = "development"

Sprint (1 week)

- Sprint 1:
  - build skeleton project: connect with postgresql, rest api, etc
  - seed data
- Sprint 2:
  - add docker config : fail
  - use fluent configuration
  -  
  <!-- - Separate file configuration -->
  - enhance code base
- Sprint 3:
  - add test project.
  - optimize move and copy data seed type json correct destination
  - service test and unit tests
  - add identity user
    - jwt token
    - policy base.
- Sprint 4:
  - review code
  - release

## Architecture

- application
  - api
    - ApplicationLogic
      - Repositories
      - Services
        - WriteService
        - ReadService
    - Core
      - Configuration
      - Constants ??
      - Entities
      - Enum
      - Extensions
      - Interfaces
      - Messaging ??
      - Retry ??
      - Utilities - string helpers
    - Infrastructure
      - Postgres
      - SNS(message Snspublisher.cs) ??
    - Presentation
      - Authentication
      - Constants ??
      - Controllers
      - Filters
      - Mappers
      - Validation
    - appsettings.json
    - Program.cs
  - Migrations
  - Models

## Technologies

- net v7.0
- postgresql
- docker
- serilog
- redis
- newrelics
- Splunk
- Nginx
- Hangfire          == separate demo
- NetMQ (optional)  == separate demo


## Dependencies

- AutoMapper.Extensions.Microsoft.DependencyInjection  
- FluentValidation  
- FluentValidation.AspNetCore  
- Microsoft.AspNetCore.Authentication.JwtBearer  
- Microsoft.AspNetCore.OpenApi  
- Microsoft.EntityFrameworkCore.Design  
- Microsoft.EntityFrameworkCore.InMemory  
- Microsoft.EntityFrameworkCore.SqlServer  
- Microsoft.EntityFrameworkCore.Tools  
- Newtonsoft.Json  
- Serilog.AspNetCore  
- Swashbuckle.AspNetCore  
- Npgsql.EntityFrameworkCore.PostgreSQL
- Microsoft.AspNetCore.Identity.EntityFrameworkCore