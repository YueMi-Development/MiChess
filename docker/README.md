# MiChess Docker Setup

This directory contains Docker configuration for running the MiChess application with chess engines.

## Quick Start

```bash
# Start all services
docker-compose up -d

# View logs
docker-compose logs -f

# Stop services
docker-compose down
```

## Services

| Service | Port | Description |
|---------|------|-------------|
| web | 8000 | Laravel web application |
| engine-normal | 9001 | Chess engine (Normal mode) |
| db | 3306 | MySQL database |
| redis | 6379 | Redis cache |

## First Time Setup

1. Start the containers:
   ```bash
   docker-compose up -d
   ```

2. Run migrations:
   ```bash
   docker-compose exec web php artisan migrate
   ```

3. Visit http://localhost:8000

## Adding More Engines

To add engines for additional modes (e.g., Chess960), add more service entries:

```yaml
engine-chess960:
  build:
    context: ./Engines
    dockerfile: Dockerfile
  ports:
    - "9002:9002"
  environment:
    - ENGINE_MODE=chess960
    - ENGINE_PORT=9002
```

## Configuration

### Web Application
- Edit `Website/.env` for application settings
- The Docker environment variables are set in `docker-compose.yml`

### Chess Engines
- Engines auto-generate their `config.yml` on first run
- To pre-configure, mount a custom config:
  ```yaml
  volumes:
    - ./my-engine-config.yml:/app/config/config.yml
  ```

## Development

For local development with file sync:

```bash
docker-compose up -d
```

Changes to PHP files are reflected immediately through the volume mount.
Changes to Rust files require rebuilding the engine:
```bash
docker-compose build engine-normal
docker-compose restart engine-normal
```
