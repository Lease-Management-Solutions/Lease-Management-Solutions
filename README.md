# Lease-Management-Solutions

## Project Structure

The project follows the structure below:

```bash
📂 Lease-Management-Solutions/
├── 📜 .gitignore
├── 📜 .env (Environment variables configuration)
├── 📜 docker-compose.yml (Defines and manages the containers: MongoDB, Backend, Frontend)
├── 📂 Lease-Management-Frontend/
│   ├── 📜 Dockerfile (Configures the Frontend container)
├── 📂 Lease-Management-Backend/
│   ├── 📜 Dockerfile (Configures the Backend container)
```

## Overview

This project utilizes Docker to containerize its services:

MongoDB: Database container, managed via `docker-compose.yml`.

Backend (Node.js + Express): Configured using a `Dockerfile` inside `Lease-Management-Backend/`.

Frontend (Next.js): Configured using a `Dockerfile` inside `Lease-Management-Frontend/`.

## Getting Started

To run the project, ensure you have Docker installed and running. Follow these steps:

- Clone the repositories for the backend and frontend into their respective directories:
```bash
git clone https://github.com/your-username/Lease-Management-Backend.git backend
```
```bash
git clone https://github.com/your-username/Lease-Management-Frontend.git frontend
```
- Navigate to the root directory:
```bash
cd Lease-Management-Solutions
```
- Start the containers using Docker Compose:
```bash
docker-compose up --build
```

This will initialize the MongoDB, Backend, and Frontend containers. The application will be accessible at:

- Frontend: `http://localhost:3000`

- Backend: `http://localhost:2000`

- MongoDB: Exposed internally for backend communication

## Additional Notes

All environment variables should be configured in a `.env` file before running the project.

To stop the containers, use:
```bash
docker-compose down
```