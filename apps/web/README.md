# VecNote Web Frontend

This is the frontend application for VecNote, a collaborative drawing and diagramming platform built with [Next.js](https://nextjs.org).

## Features

- 🎨 Interactive drawing canvas with comprehensive tool set
- 🔄 Real-time collaboration with WebSocket integration
- 📱 Responsive design that works on desktop and mobile
- 🎯 Modern UI with smooth animations and gestures
- 💾 Seamless integration with backend APIs for data persistence

## Getting Started

First, run the development server:

```bash
pnpm dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see VecNote in action.

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/app/building-your-application/optimizing/fonts) to automatically optimize and load custom fonts for the best user experience.

## Architecture

The VecNote frontend includes:

- **Canvas Component**: Core drawing and diagramming functionality
- **Toolbar**: Drawing tools, shapes, and formatting options  
- **Real-time Engine**: WebSocket client for live collaboration
- **Authentication**: User login and session management
- **Room Management**: Create and join collaborative sessions

## Learn More

To learn more about the technologies used:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API
- [Canvas API](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API) - drawing functionality
- [WebSocket API](https://developer.mozilla.org/en-US/docs/Web/API/WebSocket) - real-time communication

## Deploy on Vercel

The easiest way to deploy VecNote is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out the [Next.js deployment documentation](https://nextjs.org/docs/app/building-your-application/deploying) for more details.
