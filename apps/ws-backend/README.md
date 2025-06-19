# VecNote WebSocket Backend

Real-time WebSocket server for VecNote that enables live collaboration features.

## Features

- 🔄 **Real-time Collaboration**: Live drawing and editing synchronization
- 👥 **Multi-user Support**: Handle multiple users in the same drawing session
- 🏠 **Room Management**: Create and manage collaborative rooms
- 💬 **Live Chat**: Real-time messaging within drawing rooms
- 🔐 **Authentication**: Secure WebSocket connections
- 📊 **Presence**: Track online users and cursor positions

## WebSocket Events

### Client → Server
- `join-room` - Join a collaborative room
- `leave-room` - Leave the current room
- `draw-event` - Send drawing data
- `cursor-move` - Send cursor position
- `chat-message` - Send chat message
- `user-selection` - Send selected elements

### Server → Client
- `room-joined` - Confirmation of room join
- `user-joined` - New user joined the room
- `user-left` - User left the room
- `draw-update` - Receive drawing updates
- `cursor-update` - Receive cursor positions
- `chat-update` - Receive chat messages
- `users-list` - Current room users

## Getting Started

1. Copy environment variables:
   ```bash
   cp .env.example .env
   ```

2. Update the `.env` file with your configuration

3. Install dependencies (from project root):
   ```bash
   pnpm install
   ```

4. Run the WebSocket server:
   ```bash
   pnpm dev
   ```

The WebSocket server will start on `ws://localhost:8080`

## Environment Variables

See `.env.example` for all available configuration options.

## Connection Flow

1. Client connects to WebSocket server
2. Server authenticates the connection
3. Client joins a room using `join-room` event
4. Server adds client to room and broadcasts user list
5. All drawing events are synchronized across room participants
6. Client leaves room on disconnect or explicit `leave-room` event

## Scaling

For production deployments with multiple server instances, consider using Redis adapter for WebSocket scaling.
