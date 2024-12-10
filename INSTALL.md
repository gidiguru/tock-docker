## Tock Installation Guide

### Prerequisites
1. Install Docker and Docker Compose on your system
2. Git installed on your system
3. At least 4GB of RAM available
4. MongoDB (will be installed via Docker)

### Installation Steps

1. Clone the repository locally:
```bash
git clone https://github.com/gidiguru/tock-docker.git
cd tock-docker
```

2. Create a development environment:
```bash
# Switch to the development branch
git checkout setup-guide

# Start the Tock platform using Docker Compose
docker-compose up -d
```

3. Access Tock Studio:
- Once the containers are running, open your web browser
- Navigate to http://localhost:80
- The default admin credentials are:
  - Username: admin@app.com
  - Password: password

4. Verify Installation:
- Check if all services are running:
```bash
docker-compose ps
```

### Common Issues and Solutions

1. If MongoDB fails to start:
```bash
docker-compose down
docker volume rm tock-docker_mongodb_data
docker-compose up -d
```

2. If ports are already in use:
- Edit the docker-compose.yml file to change the conflicting ports
- Restart the services with `docker-compose down && docker-compose up -d`

### Next Steps

1. Create your first bot in Tock Studio
2. Setup NLP models
3. Configure channels (Messenger, WhatsApp, etc.)
4. Start development with the Tock SDK

For more detailed information, visit the official documentation at https://doc.tock.ai/tock/en/
