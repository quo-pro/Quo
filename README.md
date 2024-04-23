# Welcome to Quo 👋

#### [Live preview](https://quo-pro.vercel.app/)

A social media platform designed specifically for literature enthusiasts ✍️.
Developed as part of a technical assessment, this project not only serves as a functional prototype but also as a stepping stone towards a scalable and comprehensive social media solution.

### Key Features

- **User Authentication**: Simplified login mechanism using NextAuth, supporting extended sessions of up to 30 days without traditional credentials.
- **Real-Time Notifications**: Implemented with WebSockets to notify users instantly of friend requests and status updates.
- **Scalable Architecture**: Designed to transition into microservices, facilitating independent scaling of functionalities like user management and notifications.
- **Secure API**: Utilizes request interceptors on the Next.js server side to authenticate API calls, ensuring data integrity and security.
- **PWA Support**: Basic installability setup.

### Project Structure

#### Frontend
- **Technologies**: Next.js, React Query, Shadcn + Tailwind CSS, Socket.io
- **Repository**: [Quo Pro Frontend on GitHub](https://github.com/quo-pro/quo-pro-frontend)

### Backend
- **Technologies**: NestJS, MongoDB, Socket.io
- **Deployment**: Hosted on Railway
- **API Documentation**: [Swagger API Docs](https://quo-pro-backend-production.up.railway.app/api/v1/api-docs)
- **Repositories**:
  - [Quo Pro Backend](https://github.com/quo-pro/quo-pro-backend)
  - [Quo Pro Commons](https://github.com/quo-pro/commons) - shared types and constants.
  - [Quo Pro Database Connect](https://github.com/quo-pro/database-connect) - database schemas and mongoDB connection.

## Security Measures

- **Session Management**: Leverages Next.js's capabilities for robust session and cookie management.
- **API Security**: Ensures that all API endpoints are secured with authentication checks before processing requests.

## Reflection 🥱

One of the main challenges I encountered was managing real-time notifications efficiently, especially considering a scenario where a user could potentially have billions of followers. Initially, the thought of emitting notifications to such a vast number of followers seemed daunting. However, through research and exploration of Socket.IO documentation, I discovered the potential of using rooms (channels) to broadcast updates efficiently.

## Planned Enhancements 🔌

- **Implement a channel-based notification system** to reduce server load and allow users to manage their notification preferences effectively.
- **Enhance PWA capabilities** to improve mobile user experience and enable offline functionality.

## Cloning and Setup Instructions

To get started with Quo, you can clone the entire repository along with its submodules using the following command:

- `/backend` - Manages server-side operations with NestJS, WebSockets, and Express.
- `/frontend` - Contains the user interface, developed with React, Next.js, React Query, and Shadcn UI Library.

```bash
git clone --recurse-submodules https://github.com/quo-pro/Quo
```

```bash
cd backend
npm install
npm run start:dev
```

```bash
cd frontend
npm install
npm run start
```