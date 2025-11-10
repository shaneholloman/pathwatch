> ⚠️ PathWatch is currently in active development.

<img width="2928" height="1550" alt="image" src="https://github.com/user-attachments/assets/cbac1492-cc9f-4d53-8cc7-1c6f30bb0f10" />


# PathWatch

API monitoring and analytics platform built with a modern monorepo architecture.

## 🏗️ Project Structure

This is a monorepo managed with [Turborepo](https://turbo.build/repo) and workspaces:

```
pathwatch/
├── apps/
│   ├── collector/      # Data collection service (Bun + Elysia)
│   ├── console/        # Web dashboard (React + Vite)
│   └── query/          # Query API service (Bun + Elysia)
└── tinybird/           # Analytics data pipeline (Tinybird)
```

## 🚀 Getting Started

### Prerequisites

- Node.js >= 18.0.0
- Bun (for collector and query apps)
- pnpm, npm, or bun

### Installation

Install all dependencies across the monorepo:

```bash
bun install
```

### Development

Run all apps in development mode:

```bash
bun run dev
```

Run individual apps:

```bash
bun run collector:dev   # Run collector service
bun run console:dev     # Run web console
bun run query:dev       # Run query service
```

### Building

Build all apps:

```bash
bun run build
```

### Testing

Run tests across all packages:

```bash
bun run test
```

## 📦 Workspaces

### apps/collector

Data collection service that ingests API monitoring data.

### apps/console

Web-based dashboard for visualizing and managing API monitoring data.

### apps/query

Query API service for retrieving and analyzing monitoring data.

### tinybird

Analytics data pipeline configuration and deployment scripts.

## 🛠️ Scripts

- `bun run dev` - Start all apps in development mode
- `bun run build` - Build all apps
- `bun run test` - Run all tests
- `bun run lint` - Lint all packages
- `bun run format` - Format code with Prettier
- `bun run clean` - Clean all build artifacts and node_modules

## 📝 License

Distributed under the terms of the [GNU General Public License v3.0](LICENSE).
