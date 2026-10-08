# AEGISQ — Docker Deployment

Unified orchestration for the AEGISQ security platform.

## Services

| Service | Container | Source | Description |
|---------|-----------|--------|-------------|
| **detector** | aegisq-detector | `aegisq` | Batch threat detection pipeline |
| **api** | aegisq-api | `aegisq` | REST API on :8000 |
| **frontend** | aegisq-frontend | `aegisq-miniapp` | Telegram Mini-App dashboard |

## Quick Start

```bash
git clone https://github.com/alexhuhter313-debug/aegisq-deploy.git
cd aegisq-deploy

git clone https://github.com/alexhuhter313-debug/aegisq.git
git clone https://github.com/alexhuhter313-debug/aegisq-miniapp.git

docker compose up -d --build
```

## API Endpoints

| Endpoint | Method | Description |
|----------|--------|-------------|
| `/health` | GET | Health check |
| `/detect` | POST | Run detection on feature data |
| `/report` | GET | Latest detection report |

## Requirements
- Docker Engine 24+
- Docker Compose v2+
