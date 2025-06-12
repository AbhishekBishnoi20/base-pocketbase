# Docker PocketBase Setup

A streamlined Docker setup for running [PocketBase](https://pocketbase.io/) - an open source backend in 1 file with realtime database, authentication, file storage and admin dashboard.

## 🚀 Features

- Dockerized PocketBase instance
- Automatic container health checks
- Persistent data storage
- Easy deployment configuration
- Latest Alpine-based lightweight image

## 📋 Prerequisites

- Docker
- Docker Compose

## 🛠️ Installation

1. Clone this repository:
```bash
git clone https://github.com/AbhishekBishnoi20/base-pocketbase
cd base-pocketbase
```

2. Start the PocketBase container:
```bash
docker-compose up -d
```

The PocketBase instance will be available at `http://localhost:8080`

## 📁 Project Structure

```
.
├── docker-compose.yml    # Docker Compose configuration
├── Dockerfile           # Docker image definition
└── README.md           # This file
```

## ⚙️ Configuration

### Environment Variables

The current setup uses the following default configurations:
- Port: 8080
- Data persistence volume: pb_data

### Docker Compose Configuration

The `docker-compose.yml` file includes:
- Automatic container restart policy
- Health checks
- Volume mounting for data persistence
- Port mapping

## 🔧 Customization

### Custom Migrations

To include custom migrations, uncomment the following line in the Dockerfile:
```dockerfile
# COPY ./pb_migrations /pb/pb_migrations
```

### Custom Hooks

To include custom hooks, uncomment the following line in the Dockerfile:
```dockerfile
# COPY ./pb_hooks /pb/pb_hooks
```

## 🚦 Health Checks

The container includes built-in health checks that:
- Run every 30 seconds
- Test the PocketBase health endpoint
- Timeout after 5 seconds
- Retry 3 times before marking as unhealthy

## 📝 License

MIT License

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!
