# Holberton School - Softy Pinko Docker Project 🐳

<div align="center">
  <img src="https://www.docker.com/wp-content/uploads/2022/03/Moby-logo.png" alt="Docker Logo" width="200"/>
</div>

## 📑 Table of Contents
- [Description](#-description)
- [Project Structure](#-project-structure)
- [Prerequisites](#-prerequisites)
- [Installation](#-installation)
- [Architecture](#-architecture)
  - [Frontend (Web Service)](#frontend-web-service)
  - [Backend (API Service)](#backend-api-service)
  - [Proxy (Routing Service)](#proxy-routing-service)
- [Tasks Details](#-tasks-details)
- [Useful Commands](#-useful-commands)
- [Contributing](#-contributing)
- [Author](#-author)
- [License](#-license)
- [Acknowledgements](#-acknowledgements)

## 📝 Description
This project demonstrates the implementation of a modern web application architecture using Docker and Docker Compose. The "Softy Pinko" application is divided into several containerized components that work together to provide a complete solution.

## 🧱 Project Structure

The project is organized into several progressive tasks, each introducing a new Docker concept:

- **Task 1**: Setup of a static web server with Nginx
- **Task 2**: Creation of a backend API server with Python Flask
- **Task 3**: Container orchestration with Docker Compose
- **Task 4**: Multi-service environment configuration
- **Task 5**: Implementation of a proxy server for centralized access
- **Task 6**: Using Docker networks for better isolation

## 🔧 Prerequisites

- Docker (version 19.03 or higher)
- Docker Compose (version 1.25 or higher)
- Git

## 📦 Installation

1. Clone this repository:
```bash
git clone https://github.com/yourusername/holbertonschool-softy-pinko-docker.git
cd holbertonschool-softy-pinko-docker
```

2. Navigate to the task of your choice:
```bash
cd task6  # For the complete implementation
```

3. Build and launch the containers:
```bash
docker-compose up --build
```

4. Access the application in your browser:
```
http://localhost:80
```

## 🏗️ Architecture

### Frontend (Web Service)
- Based on Nginx
- Serves static HTML, CSS, and JavaScript files
- Exposed on port 9000 (internal)

### Backend (API Service)
- Python application with Flask
- Provides RESTful API endpoints
- Exposed on port 5252 (internal)

### Proxy (Routing Service)
- Nginx server configured as a reverse proxy
- Routes requests to the frontend or backend based on URL
- Only entry point exposed externally (port 80)

## 📊 Architecture Diagram

```
Client -> Proxy (Port 80) -> | -> Frontend (Port 9000)
                            | -> Backend (Port 5252)
```

## 📋 Tasks Details

### Task 1: Static Web Server
- Configuration of an Nginx container to serve static content

### Task 2: API Server
- Setting up a Flask server to provide dynamic data

### Task 3: Basic Docker Compose
- Service orchestration with a simple docker-compose.yml file

### Task 4: Multi-Services
- Configuration of multiple independent services with Docker Compose

### Task 5: Proxy Server
- Addition of a proxy server to centralize access to services

### Task 6: Docker Networks
- Advanced configuration with Docker networks for secure isolation

## 💻 Useful Commands

```bash
# Build and start containers
docker-compose up --build

# Start containers in background
docker-compose up -d

# Stop containers
docker-compose down

# View logs
docker-compose logs

# Access a specific container
docker-compose exec service_name bash
```

## 🤝 Contributing

Contributions to this project are welcome. To contribute:

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 👨‍💻 Author

- [Your Name](https://github.com/Pmichel74)

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgements

- Holberton School for the project structure and guidelines
- Docker community for their excellent documentation