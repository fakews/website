---
title: 'IAM (Identity & Access Management)'
date: 2024-01-05
weight: 5
---

IAM service powered by [Moto](https://github.com/getmoto/moto) via Motocker. Create users, manage roles, and test IAM policies locally.

## Features

- User creation and management
- Role and policy support
- Group management
- Access key management
- Compatible with AWS SDK IAM operations

## Quick Start

```bash
# Start IAM
docker compose up -d iam

# Create a user
aws --endpoint=http://localhost:5050 iam create-user --user-name testuser

# List users
aws --endpoint=http://localhost:5050 iam list-users
```

## Access

- **IAM API**: `http://localhost:5050`
