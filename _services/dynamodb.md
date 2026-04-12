---
title: 'DynamoDB'
date: 2024-01-02
weight: 2
---

Official [Amazon DynamoDB Local](https://hub.docker.com/r/amazon/dynamodb-local/) running in Docker. Full API compatibility for developing and testing DynamoDB-based applications.

## Features

- Official Amazon DynamoDB Local image
- Full DynamoDB API support
- Create tables, add items, query and scan
- Supports Global Secondary Indexes and Local Secondary Indexes
- Compatible with all AWS SDKs

## Quick Start

```bash
# Start DynamoDB
docker compose up -d dynamodb

# Create a table
aws --endpoint=http://localhost:8000 dynamodb create-table \
    --table-name Users \
    --attribute-definitions AttributeName=UserId,AttributeType=S \
    --key-schema AttributeName=UserId,KeyType=HASH \
    --billing-mode PAY_PER_REQUEST

# List tables
aws --endpoint=http://localhost:8000 dynamodb list-tables
```

## Access

- **DynamoDB API**: `http://localhost:8000`
- **Shell**: `http://localhost:8000/shell/`
