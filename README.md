# Effective Mobile — DevOps Test

Simple web application deployed via Docker Compose with Nginx reverse proxy.

## Architecture
## Stack
- Python http.server (backend)
- Nginx (reverse proxy)
- Docker Compose

## Quick Start

```bash
git clone https://github.com/zholarys/effective-mobile
cd effective-mobile
docker compose up -d
```

## Verify

```bash
curl http://localhost
# Expected: Hello from Effective Mobile!
```

## How it works

Nginx listens on port 80 and proxies all requests to the backend service
on port 8080. The backend is not exposed to the host — only accessible
within the Docker network.
