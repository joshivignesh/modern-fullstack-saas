# Modern Full-Stack SaaS

A full stack SaaS application template built with ASP.NET Core 8 and React 18 + TypeScript. Designed around Clean Architecture and microservices patterns, with PostgreSQL, Redis, RabbitMQ, and a complete CI/CD pipeline.

---

## Stack

| Layer | Technology |
|-------|-----------|
| Backend | ASP.NET Core 8, C# |
| Architecture | Clean Architecture — Domain, Application, Infrastructure, API layers |
| Database | PostgreSQL 15 + Entity Framework Core |
| Caching | Redis |
| Messaging | RabbitMQ |
| Auth | JWT + OAuth2 |
| API | REST + GraphQL |
| Real-time | SignalR |
| Logging | Serilog |
| Frontend | React 18 + TypeScript |
| Build | Vite |
| Styling | Tailwind CSS |
| State | Zustand |
| Data fetching | TanStack Query (React Query) |
| Forms | React Hook Form + Zod |
| Testing (backend) | xUnit + TestContainers |
| Testing (frontend) | Vitest + React Testing Library |
| CI/CD | GitHub Actions |
| Infra | Docker Compose |

---

## Getting Started

### Prerequisites

- [.NET 8 SDK](https://dotnet.microsoft.com/download)
- [Node.js 18+](https://nodejs.org)
- [Docker Desktop](https://www.docker.com/products/docker-desktop)

### 1. Start infrastructure

```bash
docker-compose up -d
```

This starts PostgreSQL, Redis, and RabbitMQ locally. Health checks are wired on all three — the app won't connect until they're ready.

### 2. Run the backend

```bash
cd backend
dotnet restore
dotnet ef database update
dotnet run
# API → https://localhost:5001
# Swagger → https://localhost:5001/swagger
```

### 3. Run the frontend

```bash
cd frontend
npm install
npm run dev
# App → http://localhost:5173
```

---

## Project Structure

```
modern-fullstack-saas/
├── backend/
│   ├── Directory.Build.props        ← Global build config (nullable, warnings as errors)
│   └── src/
│       ├── Core/
│       │   ├── Domain/              ← Entities, value objects, domain events
│       │   └── Application/         ← Use cases, DTOs, service interfaces
│       ├── Infrastructure/          ← EF Core, Redis, RabbitMQ, external APIs
│       ├── API/                     ← Controllers, middleware, Swagger
│       └── Services/                ← Individual microservices
├── frontend/
│   └── src/
│       ├── components/              ← Reusable UI
│       ├── pages/                   ← Route-level components
│       ├── hooks/                   ← Custom React hooks
│       ├── store/                   ← Zustand state slices
│       ├── services/                ← API service layer
│       └── types/                   ← Shared TypeScript types
├── .github/workflows/ci.yml         ← Build, lint, test on every push
└── docker-compose.yml               ← PostgreSQL, Redis, RabbitMQ
```

---

## Architecture

### Backend — Clean Architecture

The backend follows Clean Architecture with a strict dependency rule — inner layers never reference outer layers.

```
Domain        ← no dependencies
Application   ← depends on Domain only
Infrastructure← depends on Application (implements interfaces)
API           ← depends on Application (calls use cases)
```

CQRS separates reads from writes. Commands mutate state; queries return data. Each use case is a single class with a single responsibility.

### Frontend — Feature-first structure

Components are kept small and focused. TanStack Query manages server state — loading, caching, refetching, and error states. Zustand handles client-only state. Zod validates all form input before it reaches the API.

---

## Infrastructure

### Docker Compose

Three services, all with health checks:

| Service | Port | Purpose |
|---------|------|---------|
| PostgreSQL 15 | 5432 | Primary database |
| Redis 7 | 6379 | Caching, session storage |
| RabbitMQ 3.12 | 5672 / 15672 | Async messaging, management UI |

```bash
# Start
docker-compose up -d

# Logs
docker-compose logs -f

# Stop and remove volumes
docker-compose down -v
```

### CI/CD

GitHub Actions runs on every push to `main` and `develop`:

- **Backend** — restore, build, test
- **Frontend** — type-check, lint, test, build

Both jobs run in parallel. A failing test blocks the merge.

---

## Testing

```bash
# Backend
cd backend
dotnet test

# Frontend
cd frontend
npm run test         # Vitest headless
npm run test:ui      # Vitest with browser UI
```

Backend integration tests use TestContainers — a real PostgreSQL instance spins up in Docker for each test run, then tears down cleanly.

---

## Environment Variables

```env
# frontend/.env.local
VITE_API_URL=https://localhost:5001
VITE_API_TIMEOUT=30000
```

---

## Docs

- [Backend setup and architecture](./backend/README.md)
- [Frontend setup and structure](./frontend/README.md)

---

## Author

Vignesh Joshi — [GitHub](https://github.com/joshivignesh) · [LinkedIn](https://linkedin.com/in/joshivignesh)
