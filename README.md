# CodeSight – AI-Powered Code Intelligence System

CodeSight is an intelligent developer assistant that tracks, analyzes, and understands changes across large codebases.  
It leverages the Language Server Protocol (LSP), Model Context Protocol (MCP), and TypeSense to detect semantic diffs, suggest refactors, and maintain consistency across projects.

Built with the Better-T-Stack, CodeSight combines modern TypeScript technologies for scalable, full-stack development.

---

## Features

- **AI-Assisted Code Intelligence** – Detect semantic diffs, analyze dependencies, and suggest intelligent refactors.
- **LSP & MCP Integration** – Provides language-aware insights and cross-file consistency tracking.
- **TypeSense-Powered Search** – Enables real-time, typo-tolerant indexing for precise code navigation.
- **Type-Safe Fullstack Architecture** – Built with TypeScript, tRPC, and Prisma for end-to-end type safety.
- **Modern UI** – Built using Next.js, TailwindCSS, and shadcn/ui for a responsive developer interface.
- **Authentication** – Secure, session-based authentication implemented with Better-Auth.
- **PostgreSQL Database** – Robust, scalable relational data storage.
- **Monorepo Setup** – Managed with Turborepo for modular and optimized builds.

---

## Tech Stack

| Layer          | Technologies                          |
| -------------- | ------------------------------------- |
| Frontend       | Next.js, TailwindCSS, shadcn/ui       |
| Backend        | TypeScript, tRPC, LSP, MCP, TypeSense |
| Database       | PostgreSQL, Prisma ORM                |
| Authentication | Better-Auth                           |
| DevOps         | Docker, Turborepo                     |
| Language       | TypeScript                            |

---

## Getting Started

### 1. Install Dependencies

```bash
bun install
```

### 2. Set Up Database

This project uses PostgreSQL with Prisma.

1. Ensure PostgreSQL is installed and running.
2. Update your environment variables in apps/web/.env:

```bash
DATABASE_URL="postgresql://USER:PASSWORD@localhost:5432/codesight"
```

```bash
bun db:push
```

3. Generate the Prisma client and push the schema:

```bash
bun db:push
```

### 3. Run the Development Server

```bash
bun dev
```

Then, open http://localhost:3001
in your browser to view the application.

### Project Structure

```
codesight/
├── apps/
│ └── web/ # Fullstack Next.js application
├── packages/
│ ├── api/ # API layer with tRPC endpoints and business logic
│ ├── auth/ # Authentication configuration and logic
│ ├── db/ # Database schema and queries using Prisma
│ └── lsp/ # Language Server and MCP integration modules
```

## Available Scripts

- `bun dev`: Start all applications in development mode
- `bun build`: Build all applications
- `bun check-types`: Check TypeScript types across all apps
- `bun db:push`: Push schema changes to database
- `bun db:studio`: Open database studio UI
