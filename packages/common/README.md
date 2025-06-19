# @repo/common

Shared TypeScript types and utilities used across the VecNote application.

## Contents

- **Types**: Common TypeScript interfaces and types
- **Utilities**: Shared utility functions
- **Constants**: Application-wide constants
- **Validators**: Input validation schemas

## Usage

```typescript
import { User, Room, DrawingEvent } from '@repo/common/types';
import { validateEmail, formatDate } from '@repo/common/utils';
```

## Types

### Core Types
- `User` - User account information
- `Room` - Collaborative room data
- `DrawingEvent` - Drawing/editing events
- `ChatMessage` - Chat message structure

### API Types
- `ApiResponse<T>` - Standardized API response format
- `AuthTokens` - JWT token structure
- `PaginatedResponse<T>` - Paginated data responses

### WebSocket Types
- `WSMessage<T>` - WebSocket message format
- `RoomState` - Real-time room state
- `UserPresence` - User online status and cursor position

## Building

```bash
pnpm build
```

This package is automatically built when you run the build command from the project root.
