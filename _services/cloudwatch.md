---
title: 'CloudWatch'
date: 2024-01-08
weight: 8
---

CloudWatch and CloudWatch Logs powered by [Moto](https://github.com/getmoto/moto). Monitor metrics and manage log groups locally.

## Features

- CloudWatch Metrics API
- CloudWatch Logs API
- Log group and log stream management
- Put and get metric data
- Compatible with AWS SDK CloudWatch operations

## Quick Start

```bash
# Start CloudWatch and Logs
docker compose up -d cloudwatch logs

# Create a log group
aws --endpoint=http://localhost:5052 logs create-log-group \
    --log-group-name /app/my-service

# List log groups
aws --endpoint=http://localhost:5052 logs describe-log-groups

# List metrics
aws --endpoint=http://localhost:5051 cloudwatch list-metrics
```

## Access

- **CloudWatch API**: `http://localhost:5051`
- **CloudWatch Logs API**: `http://localhost:5052`
