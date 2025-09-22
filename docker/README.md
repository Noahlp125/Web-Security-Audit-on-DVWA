# 🐳 Docker Compose — DVWA Lab Environment

This directory contains the `docker-compose.yml` file used to deploy a lab environment with **Damn Vulnerable Web Application (DVWA)** and related services.  
The goal is to have a controlled environment for **web auditing, pentesting, and vulnerability analysis** practice.

## 📂 Files
- `docker-compose.yml` — defines the services and containers.

## 🚀 Prerequisites
- Docker installed → [Instructions](https://docs.docker.com/get-docker/)  
- Docker Compose installed → [Instructions](https://docs.docker.com/compose/install/)  

Check installation:
```bash
docker --version
docker compose version

# ▶️ Usage

1. Clone this repository or navigate to the folder containing the file:
git clone <repo-url>
cd dvwa-docker

2. Start the containers in detached mode:
docker compose up -d

3. Access DVWA in your browser:
http://localhost:8080

4. To stop the environment:
docker compose down

#⚙️ Configuration

1. The docker-compose.yml file defines:

DVWA: vulnerable application for testing.

MySQL/MariaDB database: backend for DVWA.

Environment variables set in the YAML for default credentials.

⚠️ Note: This environment is for educational purposes only. Never expose DVWA to the internet or production networks.


