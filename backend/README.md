# Modern FullStack SaaS - Backend

ASP.NET Core 8 Backend API with microservices architecture

## Tech Stack
- **Runtime**: .NET 8
- **Framework**: ASP.NET Core 8
- **Database**: PostgreSQL
- **ORM**: Entity Framework Core with Code-First
- **Architecture**: Clean Architecture + Microservices
- **Patterns**: DDD, CQRS, Repository Pattern
- **Real-time**: SignalR
- **Authentication**: JWT + OAuth2
- **API**: REST + GraphQL
- **Validation**: FluentValidation
- **Logging**: Serilog
- **Messaging**: RabbitMQ
- **Caching**: Redis

## Project Structure
```
backend/
├── src/
│   ├── Core/                 # Domain & Application layer
│   │   ├── Domain/          # Business logic, entities
│   │   └── Application/     # Use cases, DTOs, Services
│   ├── Infrastructure/       # External services, DB, etc.
│   ├── API/                 # Web API layer
│   └── Services/            # Microservices
├── tests/                   # Unit & Integration tests
├── docker-compose.yml       # Local development environment
└── Directory.Build.props    # Global build properties
```

## Getting Started

### Prerequisites
- .NET 8 SDK
- Docker & Docker Compose
- PostgreSQL 15+

### Setup
\`\`\`bash
cd backend
dotnet restore
docker-compose up -d
dotnet ef database update
dotnet run
\`\`\`

API runs on `https://localhost:5001`

## Key Features
- ✅ Microservices-ready architecture
- ✅ Clean separation of concerns
- ✅ Comprehensive error handling
- ✅ Async/await throughout
- ✅ Dependency Injection
- ✅ Unit tests with xUnit
- ✅ Integration tests with TestContainers
- ✅ Swagger/OpenAPI documentation
- ✅ Health checks
- ✅ Structured logging

## Database

Using Entity Framework Core with PostgreSQL:
\`\`\`bash
# Add migration
dotnet ef migrations add MigrationName

# Update database
dotnet ef database update
\`\`\`

## Testing
\`\`\`bash
dotnet test
\`\`\`
