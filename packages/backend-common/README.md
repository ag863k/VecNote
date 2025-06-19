# @repo/backend-common

Shared backend utilities and middleware for VecNote server applications.

## Contents

- **Middleware**: Common Express.js middleware
- **Utilities**: Backend-specific utility functions
- **Authentication**: JWT token handling
- **Validation**: Request validation helpers
- **Error Handling**: Standardized error responses

## Middleware

### Authentication
- `authenticateToken` - Verify JWT tokens
- `requireAuth` - Protect routes that require authentication

### Security
- `rateLimiter` - Rate limiting middleware
- `corsMiddleware` - CORS configuration
- `helmet` - Security headers

### Validation
- `validateRequest` - Request body validation
- `sanitizeInput` - Input sanitization

### Logging
- `requestLogger` - HTTP request logging
- `errorLogger` - Error logging

## Usage

```typescript
import { 
  authenticateToken, 
  rateLimiter, 
  validateRequest 
} from '@repo/backend-common';

// In Express.js routes
app.use(rateLimiter);
app.use(corsMiddleware);

app.get('/protected', authenticateToken, (req, res) => {
  res.json({ user: req.user });
});

app.post('/api/rooms', 
  authenticateToken,
  validateRequest(roomSchema),
  createRoom
);
```

## Utilities

### JWT Handling
```typescript
import { generateTokens, verifyToken } from '@repo/backend-common';

const tokens = generateTokens(userId);
const decoded = verifyToken(accessToken);
```

### Error Handling
```typescript
import { ApiError, handleError } from '@repo/backend-common';

throw new ApiError(400, 'Invalid input');
app.use(handleError);
```

## Building

```bash
pnpm build
```

This package is automatically built when you run the build command from the project root.
