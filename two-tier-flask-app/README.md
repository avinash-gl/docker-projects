# 2 Tier FLask App

A simple two-tier web application using **Flask** for the frontend/backend and **MySQL** as the database, all containerized using **Docker** and managed via **Docker Compose**.

## Project Overview

This project demonstrates a basic two-tier architecture:
- **Tier 1 (App Layer):** Python Flask web application
- **Tier 2 (Data Layer):** MySQL database

Everything runs in isolated containers to simulate a real-world deployment.

##  Architecture

```text
+-------------------+         +--------------------+
|                   |         |                    |
|   Flask Web App   | <-----> |      MySQL DB      |
|     (Python)      |         |   (Containerized)  |
|                   |         |                    |
+-------------------+         +--------------------+
         |                             |
         +-------- Docker Compose -----+
```

## Usage

1. Clone the Repository

```bash
https://github.com/avinash-gl/2tier-flask-app-docker.git
cd 2tier-flask-app-docker
```

2. Build and run using Docker compose 

```bash
docker-compose up --build
```

3. Access the Flask app: Go to http://localhost:5000 in your browser.

## Cleanup 

Stop and remove all containers including volumes.

```bash
docker compose down -v
```