# Modern Full-Stack SaaS Application

A production-ready, enterprise-grade SaaS application template built with cutting-edge technologies.

## 🚀 What's Included

### Backend (ASP.NET Core 8)
- Clean Architecture with CQRS pattern
- Microservices-ready design
- Entity Framework Core with PostgreSQL
- JWT + OAuth2 authentication
- SignalR for real-time features
- GraphQL + REST API
- Comprehensive error handling
- Structured logging with Serilog
- Unit & integration tests

### Frontend (React 18 + TypeScript)
- Modern React with Hooks
- Type-safe with TypeScript
- Vite for blazing-fast builds
- Tailwind CSS for styling
- React Router for navigation
- TanStack Query for data fetching
- Zustand for state management
- React Hook Form + Zod validation
- Comprehensive test coverage

### Infrastructure
- Docker & Docker Compose
- PostgreSQL database
- Redis for caching
- RabbitMQ for messaging
- GitHub Actions CI/CD
- Health checks on all services

## 📊 Project Stats
- **Backend**: ~100% type-safe C#
- **Frontend**: 100% TypeScript
- **Test Coverage**: 80%+
- **Code Quality**: SonarQube ready

## 🛠 Tech Stack Overview

| Layer | Technology |
|-------|------------|
| **Frontend Framework** | React 18 + TypeScript |
| **Frontend Build** | Vite |
| **Styling** | Tailwind CSS |
| **Backend Framework** | ASP.NET Core 8 |
| **Database** | PostgreSQL 15 |
| **Caching** | Redis |
| **Message Queue** | RabbitMQ |
| **ORM** | Entity Framework Core |
| **API Styles** | REST + GraphQL |
| **Real-time** | SignalR |
| **Testing Backend** | xUnit + TestContainers |
| **Testing Frontend** | Vitest + React Testing Library |
| **CI/CD** | GitHub Actions |

## 🚀 Quick Start

### Prerequisites
- Docker & Docker Compose
- .NET 8 SDK
- Node.js 18+

### Setup

\`\`\`bash
# Clone and setup
git clone <repo>
cd modern-fullstack-saas

# Start infrastructure
docker-compose up -d

# Backend
cd backend
dotnet ef database update
dotnet run

# Frontend (in new terminal)
cd frontend
npm install
npm run dev
\`\`\`

**Backend API**: https://localhost:5001
**Frontend**: http://localhost:5173

## 📁 Project Structure

\`\`\`
modern-fullstack-saas/
├── backend/
│   ├── src/
│   │   ├── Core/          # Domain + Application layers
│   │   ├── Infrastructure/
│   │   ├── API/           # Web API
│   │   └── Services/      # Microservices
│   ├── tests/
│   └── docker-compose.yml
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── hooks/
│   │   ├── store/
│   │   ├── services/
│   │   └── types/
│   └── public/
├── .github/
│   └── workflows/         # CI/CD
└── README.md
\`\`\`

## ✨ Key Features

- ✅ **Production-Ready**: Built with industry best practices
- ✅ **Type-Safe**: Both backend (C#) and frontend (TypeScript)
- ✅ **Scalable**: Microservices architecture
- ✅ **Well-Tested**: Comprehensive test coverage
- ✅ **Modern Stack**: Latest frameworks and tools
- ✅ **CI/CD Ready**: GitHub Actions workflows included
- ✅ **Containerized**: Docker setup for easy deployment
- ✅ **Documentation**: Code and architecture well-documented

## 📚 Documentation

- [Backend Setup](./backend/README.md)
- [Frontend Setup](./frontend/README.md)
- [Architecture Overview](./ARCHITECTURE.md)
- [API Documentation](./docs/API.md)

## 🧪 Testing

\`\`\`bash
# Backend tests
cd backend && dotnet test

# Frontend tests
cd frontend && npm run test
\`\`\`

## 🐳 Docker

\`\`\`bash
# Start all services
docker-compose up -d

# View logs
docker-compose logs -f

# Stop services
docker-compose down
\`\`\`

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Open a Pull Request

## 📄 License

MIT License - see LICENSE file for details

## 👨‍💻 Author

[Your Name] - Senior Full-Stack Developer

Connect on [LinkedIn](https://linkedin.com/in/joshivignesh) | Check out [Medium](https://medium.com/@joshi.vignesh)
