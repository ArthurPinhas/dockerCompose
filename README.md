# Docker Compose Configuration for Service Deployment

This repository contains a Docker Compose configuration file for deploying multiple services using Docker containers.

## Services

### it-tools

This service runs a tool container based on the latest image from `corentinth/it-tools`. It exposes port 8080 on the host and restarts automatically unless stopped.

### plex

The Plex service deploys the latest Plex Media Server Docker image from `plexinc/pms-docker`. It sets up environment variables, network mode, and volumes for data persistence. This service is labeled to enable automatic updates using Watchtower.

### adguard_home

The AdGuard Home service deploys the latest AdGuard Home Docker image from `adguard/adguardhome`. It configures network ports, environment variables, and volumes for data persistence. It is also labeled to enable automatic updates using Watchtower.

### watchtower

Watchtower is deployed to automatically update Docker containers to their latest versions. It mounts the Docker socket and sets up environment variables for configuration. It is labeled to enable self-updates.

### homepage

The Homepage service deploys the latest image from `ghcr.io/gethomepage/homepage`. It sets up environment variables, ports, and volumes for configuration and data persistence. It is also labeled to enable automatic updates using Watchtower.

## Usage

1. Clone or download this repository to your local machine.
2. Navigate to the directory containing the `docker-compose.yml` file.
3. Run the following command to start the services:

   `docker-compose up -d`
