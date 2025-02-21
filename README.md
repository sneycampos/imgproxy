# imgproxy with Caddy Reverse Proxy

This repository provides a Docker-based setup for deploying imgproxy, a fast and secure image processing server, with Caddy as a reverse proxy. Caddy handles automatic HTTPS and simplifies the reverse proxy configuration.

## Features

- ***imgproxy***: Processes images on-the-fly, supporting resizing, cropping, and format conversion. 
- ***Caddy***: Serves as a reverse proxy with automatic HTTPS using Let's Encrypt.

## Prerequisites

Docker: Ensure Docker and Docker Compose is installed and running on your system.

## Setup Instructions

**Clone the Repository**:

```bash
git clone https://github.com/sneycampos/imgproxy.git
cd imgproxy
```

**Configure Environment Variables**:

Copy the example environment file:

```bash
cp .env.example .env
```

Modify the `.env` file to set your Cloudflare API Key.
```env
CLOUDFLARE_API_TOKEN=your-cf-api-token
```


**Review and Modify Configuration Files**:
- **Caddyfile**: Defines the reverse proxy rules and site configurations.
- **Dockerfile**: Specifies the imgproxy image and build instructions.
- **compose.yml**: Manages the containerized services.



**Start the Containers**:

```bash
docker compose up -d
```
