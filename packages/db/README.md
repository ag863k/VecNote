# @repo/db

Database schema and operations for VecNote using Prisma ORM.

## Features

- 🗄️ **PostgreSQL Database**: Production-ready database setup
- 🔄 **Prisma ORM**: Type-safe database operations
- 📊 **Migrations**: Version-controlled database schema changes
- 🔒 **Security**: Proper indexing and constraints

## Database Schema

### Tables
- `User` - User accounts and profiles
- `Room` - Collaborative drawing rooms
- `Chat` - Chat messages within rooms

### Relationships
- Users can admin multiple rooms
- Rooms belong to one admin user
- Chat messages belong to users and rooms

## Getting Started

1. Set up your PostgreSQL database (we recommend [Neon](https://neon.tech/))

2. Copy the environment file:
   ```bash
   cp .env.example .env
   ```

3. Update the `DATABASE_URL` in `.env` with your database connection string

4. Run the initial migration:
   ```bash
   npx prisma migrate dev
   ```

5. Generate the Prisma client:
   ```bash
   npx prisma generate
   ```

## Available Scripts

- `prisma migrate dev` - Run migrations in development
- `prisma migrate deploy` - Deploy migrations to production
- `prisma generate` - Generate Prisma client
- `prisma studio` - Open Prisma Studio GUI
- `prisma db seed` - Run database seeding (if configured)

## Usage in Code

```typescript
import { prisma } from '@repo/db';

// Create a user
const user = await prisma.user.create({
  data: {
    email: 'user@example.com',
    name: 'John Doe',
    password: 'hashedPassword'
  }
});

// Find rooms
const rooms = await prisma.room.findMany({
  include: {
    admin: true,
    chats: true
  }
});
```

## Environment Variables

See `.env.example` for database configuration options.

## Migrations

Migration files are located in `prisma/migrations/` and have descriptive names:
- `20250112150913_create_vecnote_core_tables` - Initial schema
- `20250112153819_make_user_photo_optional` - Photo field changes
- `20250112155013_add_unique_email_constraint` - Email uniqueness
