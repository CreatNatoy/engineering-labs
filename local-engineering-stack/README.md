# Local Engineering Stack

Minimal local infrastructure stack using Docker Compose.

## Architecture

Windows 11  
→ WSL2 (Ubuntu 24.04)  
→ Docker Desktop  
→ Docker Network (bridge)  
→ Services:
   - PostgreSQL 16
   - pgAdmin 4

## Services

### PostgreSQL
- Image: postgres:16
- Port: 5432
- Persistent volume: postgres_data

### pgAdmin
- Image: dpage/pgadmin4:8
- Port: 5050
- Connects to Postgres via Docker network hostname: `postgres`

## How to Run

```bash
docker compose up -d
