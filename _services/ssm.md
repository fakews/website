---
title: 'SSM (Systems Manager Parameter Store)'
date: 2024-01-07
weight: 7
---

Local SSM Parameter Store powered by [ssm-local](https://github.com/antimatter-studios/ssm-local). Store and retrieve configuration parameters locally.

## Features

- Parameter Store API compatibility
- String, StringList, and SecureString parameter types
- Parameter versioning
- Persistent data storage
- Path-based parameter hierarchy

## Quick Start

```bash
# Start SSM
docker compose up -d ssm

# Put a parameter
aws --endpoint=http://localhost:9230 ssm put-parameter \
    --name "/app/config/db_host" \
    --value "localhost" \
    --type String

# Get a parameter
aws --endpoint=http://localhost:9230 ssm get-parameter \
    --name "/app/config/db_host"
```

## Access

- **SSM API**: `http://localhost:9230`
