# VecNote HTTP Backend

REST API server for VecNote that handles authentication, data persistence, and file management.

## Features

- 🔐 **User Authentication**: JWT-based authentication system
- 💾 **Data Persistence**: Room and user data management
- 📁 **File Management**: Handle uploads and media files
- 🛡️ **Security**: Rate limiting, input validation, and CORS protection
- 📊 **Database**: Prisma ORM with PostgreSQL

## API Endpoints

### Authentication
- `POST /api/auth/register` - User registration
- `POST /api/auth/login` - User login
- `POST /api/auth/logout` - User logout
- `GET /api/auth/me` - Get current user

### Rooms
- `GET /api/rooms` - List user's rooms
- `POST /api/rooms` - Create new room
- `GET /api/rooms/:slug` - Get room details
- `PUT /api/rooms/:slug` - Update room
- `DELETE /api/rooms/:slug` - Delete room

### Users
- `GET /api/users/profile` - Get user profile
- `PUT /api/users/profile` - Update user profile
- `POST /api/users/avatar` - Upload user avatar

## Getting Started

1. Copy environment variables:
   ```bash
   cp .env.example .env
   ```

2. Update the `.env` file with your database URL and secrets

3. Install dependencies (from project root):
   ```bash
   pnpm install
   ```

4. Run the server:
   ```bash
   pnpm dev
   ```

The server will start on `http://localhost:3001`

## Environment Variables

See `.env.example` for all available configuration options.

## Database

This server uses the shared `@repo/db` package for database operations. Make sure to run database migrations before starting the server:

```bash
cd ../../packages/db
npx prisma migrate dev
```
