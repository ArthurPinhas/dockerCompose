# Docker Compose Configuration for Service Deployment

This repository contains a Docker Compose configuration file for deploying multiple services using Docker containers.

## Services Overview

### it-tools

**Description**: This service runs a container providing a collection of IT tools and utilities, facilitating tasks such as network diagnostics, system monitoring, and troubleshooting. It exposes port 8080 on the host for accessing the tools.

### plex

**Description**: The Plex service enables users to deploy and manage a Plex Media Server, a versatile platform for organizing, streaming, and accessing multimedia content.

### adguard_home

**Description**: The AdGuard Home service offers network-wide ad blocking and privacy protection by deploying the AdGuard Home application. It provides advanced filtering capabilities to block ads, trackers, and malicious websites, enhancing browsing security and privacy for all devices connected to the network.

### watchtower

**Description**: Watchtower automates the process of updating Docker containers to their latest versions. It continuously monitors the Docker registry for changes to container images and automatically updates running containers with the latest versions.

### homepage

The Homepage service deploys the latest image from `ghcr.io/gethomepage/homepage`. It sets up environment variables, ports, and volumes for configuration and data persistence. It is also labeled to enable automatic updates using Watchtower.

### hbbs and hbbr

The HBBs and HBBR services deploy the latest RustDesk Server Docker image from `rustdesk/rustdesk-server`. They each have their respective configurations for command, volumes, network mode, and restart policy.

### portainer

The Portainer service deploys the latest Portainer Community Edition Docker image from `portainer/portainer-ce`. It exposes port 9443 on the host and mounts volumes for data persistence. It restarts automatically unless stopped.

## Usage

1. Clone or download this repository to your local machine.
2. Navigate to the directory containing the `docker-compose.yml` file.
3. Run the following command to start the services:

   `docker-compose up -d`
