# Pragmeter Setup

This repository contains the `docker-compose.yml` and `.env` files required to run the Pragmeter platform using Docker.

## Services

The following services are included in the setup:

- **db** – PostgreSQL 16 database  
- **api** – FastAPI backend (runs on port 8000)  
- **be** – Business logic backend (runs on port 8008)  
- **fe** – Frontend (Vite app, runs on port 3001)  
- **redis** – Redis 7 (used for caching and background jobs)
- **traefik** – Reverse proxy (use secure connection with https:// in local environment)

## Requirements

- Docker (20.x or newer)  
- Docker Compose v2  

## Quick Start

1. Clone the repository:
   ```bash
   git clone https://github.com/Pragmeter-Team/setup.git
   cd setup

## Adjust the .env file if needed. Example:

IMAGE_TAG=2025.09.25
DOMAIN=app.pragmeter.com
POSTGRES_DB=PrgDB
POSTGRES_USER=prgadmin
LE_RESOLVER=le-dns01
ACME_EMAIL=office@pragmeter.com
VITE_API_URL=http://pragmeter:7000
CF_DNS_API_TOKEN=xxxxxxxxxxxxxxxxxxxxxxxxxxxxxx

## Start the stack

docker compose up -d
