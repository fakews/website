---
title: 'Cognito'
date: 2024-01-06
weight: 6
---

Local Cognito implementation powered by [cognito-local](https://github.com/antimatter-studios/cognito-local). Test user authentication and user pool management without AWS.

## Features

- User Pool creation and management
- User registration and authentication
- Token generation (ID, Access, Refresh)
- Persistent data storage to disk
- Compatible with AWS Cognito SDK operations

## Quick Start

```bash
# Start Cognito
docker compose up -d cognito

# List user pools
aws --endpoint=http://localhost:9229 cognito-idp list-user-pools --max-results 10
```

## Access

- **Cognito API**: `http://localhost:9229`
