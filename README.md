# AEGISQ — Docker Deployment

Unified Docker orchestration for the AEGISQ security platform.

## Services

| Service | Container | Description |
|---------|-----------|-------------|
| **detector** | aegisq-detector | AI-powered threat detection engine (from aegisq-prototype) |
| **fortress** | aegisq-fortress | Fortress Command Suite — recon, forensics, quantum crypto (from shadow313) |
| **frontend** | aegisq-frontend | Telegram Mini-App dashboard (from aegisq-miniapp) |

## Quick Start

```bash
# 1. Clone this repo
git clone https://github.com/alexhuhter313-debug/aegisq-deploy.git
cd aegisq-deploy

# 2. Clone the sub-repos
git clone https://github.com/alexhuhter313-debug/aegisq-prototype.git
git clone https://github.com/alexhuhter313-debug/shadow313.git
git clone https://github.com/alexhuhter313-debug/aegisq-miniapp.git

# 3. Build and run everything
docker compose up -d --build

# 4. Check logs
docker compose logs -f

# 5. Stop
docker compose down
```

## Requirements

- Docker Engine 24+
- Docker Compose v2+
