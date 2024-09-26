# Fullstack Go and Next.js App
![image](https://github.com/user-attachments/assets/d9653a6d-c0fb-4dbd-8944-815ea661d8a9)

This repository contains a fullstack application with a Go backend, Next.js frontend, and PostgreSQL database, all dockerized for easy deployment and development.

## Table of Contents

- [Overview](#overview)
- [Prerequisites](#prerequisites)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
- [API Endpoints](#api-endpoints)
- [Docker Compose Configuration](#docker-compose-configuration)
- [Development](#development)
- [Contributing](#contributing)
- [License](#license)

## Overview

This application is a simple user management system with a Go backend API and a Next.js frontend. It uses PostgreSQL as the database to store user information.

### Features

- RESTful API for user management (CRUD operations)
- Dockerized services for easy deployment
- CORS enabled for frontend-backend communication
- PostgreSQL database for data persistence

## Prerequisites

- Docker and Docker Compose
- Go (for local development)
- Node.js and npm (for local frontend development)

## Project Structure

```
.
├── backend/
│   ├── main.go
│   └── go.dockerfile
├── client/
│   └── next.dockerfile
├── docker-compose.yml
└── README.md
```

## Getting Started

1. Clone this repository:
   ```
   git clone <repository-url>
   cd <repository-name>
   ```

2. Start the application using Docker Compose:
   ```
   docker-compose up --build
   ```

3. Access the application:
   - Frontend: http://localhost:3000
   - Backend API: http://localhost:8000

## API Endpoints

The backend provides the following API endpoints:

- `GET /api/go/users`: Get all users
- `POST /api/go/users`: Create a new user
- `GET /api/go/users/{id}`: Get a user by ID
- `PUT /api/go/users/{id}`: Update a user
- `DELETE /api/go/users/{id}`: Delete a user

## Docker Compose Configuration

The `docker-compose.yml` file defines three services:

1. `nextapp`: Next.js frontend application
2. `goapp`: Go backend API
3. `db`: PostgreSQL database

To start all services:

```
docker-compose up
```

To stop all services:

```
docker-compose down
```

## Development


### Backend (Go)

The backend is a Go application using the following packages:

- `github.com/gorilla/mux` for routing
- `github.com/lib/pq` as the PostgreSQL driver

To run the backend locally:

```
cd backend
go run main.go
```

### Frontend (Next.js)

The frontend is a Next.js application. To run it locally:

```
cd client
npm install
npm run dev
```

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License.
