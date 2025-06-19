# VecNote

A collaborative drawing and diagramming application built with modern web technologies. VecNote provides real-time collaboration features for creating diagrams, sketches, and visual notes.

## Features

- 🎨 **Drawing Tools**: Comprehensive set of drawing and shape tools
- 🔄 **Real-time Collaboration**: Live collaborative editing with multiple users
- 💾 **Persistent Storage**: Save and load your diagrams
- 📱 **Responsive Design**: Works seamlessly across desktop and mobile devices
- 🚀 **Modern Tech Stack**: Built with Next.js, TypeScript, and WebSockets

## Getting Started

Clone the repository and install dependencies:

```sh
git clone <your-repo-url>
cd VecNote
pnpm install
```

## Architecture

This VecNote application includes the following packages/apps:

### Apps and Packages

- `web`: VecNote frontend - [Next.js](https://nextjs.org/) application with drawing canvas and UI
- `http-backend`: REST API server for authentication, data persistence, and file management
- `ws-backend`: WebSocket server for real-time collaboration features
- `@repo/ui`: Shared React component library for consistent UI across applications
- `@repo/common`: Shared TypeScript types and utilities
- `@repo/db`: Database schema and operations using Prisma
- `@repo/backend-common`: Shared backend utilities and middleware
- `@repo/eslint-config`: ESLint configurations for consistent code quality
- `@repo/typescript-config`: Shared TypeScript configurations

Each package/app is 100% [TypeScript](https://www.typescriptlang.org/) for type safety and better developer experience.

### Tech Stack

- **Frontend**: Next.js 14, React, TypeScript, Canvas API
- **Backend**: Node.js, Express.js, WebSocket
- **Database**: PostgreSQL with Prisma ORM
- **Real-time**: WebSocket connections for live collaboration
- **Development**: Turborepo for monorepo management

### Development Tools

This VecNote project includes:

- [TypeScript](https://www.typescriptlang.org/) for static type checking
- [ESLint](https://eslint.org/) for code linting
- [Prettier](https://prettier.io) for code formatting

### Build

To build all VecNote apps and packages:

```bash
cd VecNote
pnpm build
```

### Development

To start the development environment:

```bash
cd VecNote
pnpm dev
```

This will start:
- Frontend at `http://localhost:3000`
- HTTP API at `http://localhost:3001`
- WebSocket server at `ws://localhost:8080`

### Database Setup

1. Set up your PostgreSQL database (we recommend [Neon](https://neon.tech/))
2. Create environment files with your database connection:
   - Create `.env` in the project root with `DATABASE_URL="your-connection-string"`
   - Create `.env` in `packages/db/` with the same `DATABASE_URL`
3. Run migrations: `cd packages/db && npx prisma migrate dev`

## Security

**Important Security Notes:**

- **Environment Variables**: Never commit `.env` files to version control. Create your own `.env` files locally.
- **Secrets Management**: All API keys, passwords, and secrets should be stored in environment variables.
- **Database**: Use strong passwords and secure connection strings for production databases.
- **JWT Secrets**: Generate strong, unique secrets for JWT tokens in production.
- **CORS**: Configure CORS properly for production deployments.

The project includes comprehensive `.gitignore` files to prevent accidental exposure of sensitive information.

## Useful Links

Learn more about the technologies used in VecNote:

- [Next.js Documentation](https://nextjs.org/docs) - Frontend framework
- [Prisma Documentation](https://www.prisma.io/docs) - Database ORM
- [Turborepo Documentation](https://turbo.build/repo/docs) - Monorepo management
- [TypeScript Documentation](https://www.typescriptlang.org/docs) - Type safety
- [WebSocket API](https://developer.mozilla.org/en-US/docs/Web/API/WebSocket) - Real-time communication
- [Canvas API](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API) - Drawing functionality
